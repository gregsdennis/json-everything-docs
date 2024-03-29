---
layout: page
title: JsonPatch.Net Basics
md_title: _JsonPatch.Net_ Basics
bookmark: JSON Patch
permalink: /patch/:title/
icon: fas fa-tag
order: "03.1"
---
[JSON Patch](https://tools.ietf.org/html/rfc6902) is a language for modifying JSON documents.  Like JSON Schema, it is also expressed in JSON.

## Syntax {#patch-syntax}

A patch consists of an array containing one or more operations.  Each operation may also contain one or more arguments.

An operation must be one of

- `add`
- `remove`
- `replace`
- `copy`
- `move`
- `test`

The arguments vary among them, though all must contain at least an `op` and a `path`.  ("Path" as used here is colloquial.  It's actually a JSON Pointer, not JSON Path.)

- `op` specifies the operation and must be one of the values above.
- `path` specifies the location within the JSON document which will receive changes.
- `from` specifies a source location within the JSON document from which to pull a value.
- `value` specifies an explicit value.

## Applying Patches {#patch-apply}

In _JsonPatch.Net_, a `JsonPatch` object can be deserialized directly from the JSON document string.

```c#
var patch = JsonSerializer.Deserialize<JsonPatch>(patchString);
```

`JsonPatch` operates on `JsonNode?` values.  To apply the patch, parse the document and pass the root element into the `.Apply()` method.

```c#
var doc = JsonNode.Parse(docString);
var result = patch.Apply(doc);
```

The result contains the altered document, either fully patched, or up to the point an error occurred along with an error message.

You can even apply a patch from one object to another!  They don't even need to be of the same type!!

```c#
var myPatchedObject = patch.Apply(myObject);
var myDifferentTypeObject = patch.Apply<MyObject, MyDifferentObject>(myObject);
```

## Inline Patching {#patch-inline}

The `JsonPatch` class can also be built in code using by creating a series of `PatchOperation`s through its static constructor methods.  There's one for each operation.

```c#
var patch = new JsonPatch(PatchOperation.Add("/foo/bar", "baz"),
                          PatchOperation.Test("/foo/biz", false));
```

That's it!

## Generating Patches {#patch-generation}

If you know what your start and end states are, but you want to find the differences, you can do that by generating a patch.

```c#
var start = JsonNode.Parse("[{\"test\":\"test123\"},{\"test\":\"test321\"},{\"test\":[1,2,3]},{\"test\":[1,2,4]}]");
// you can also build your data inline
var target = new JsonArray{
  new JsonObject { ["test"] = "test123" },
  new JsonObject { ["test"] = "test32132" },
  new JsonObject { ["test1"] = "test321" },
  new JsonObject { ["test"] = new JsonArray{ 1, 2, 3 } },
  new JsonObject { ["test"] = new JsonArray{ 1, 2, 3 } },
}

var patch = start.CreatePatch(target);
```

This results in the JSON Patch

```json
[
  {"op":"replace","path":"/1/test","value":"test32132"},
  {"op":"remove","path":"/2/test"},
  {"op":"add","path":"/2/test1","value":"test321"},
  {"op":"replace","path":"/3/test/2","value":3},
  {"op":"add","path":"/4","value":{"test":[1,2,3]}}
]
```

This patch can be tested on the first object and should generate the second.

Other related features:

- Generate reverse patches: `target.CreatePatch(start)`
- Generate patches between .Net objects: `myObject1.CreatePatch(myObject2)`

## Ahead of Time (AOT) compatibility {#aot}

_JsonPatch.Net_ v3 includes updates to support [Native AOT applications](https://learn.microsoft.com/en-us/dotnet/core/deploying/native-aot/).  In order to take advantage of this, there are a few things you'll need to do.

First, on your `JsonSerializerContext`, add the following attributes:

```c#
[JsonSerializable(typeof(JsonPatch))]
[JsonSerializable(typeof(PatchResult))]
```

It's recommended that you create a single `JsonSerializerOptions` object (or a few if you need different configurations) and reuse it rather than creating them ad-hoc.  When you create one, you'll need to configure its `TypeInfoResolverChain` with your serializer context:

```c#
var serializerOptions = new()
{
    TypeInfoResolverChain = { MySerializerContext.Default }
};
```

You're done.  Congratulations.
