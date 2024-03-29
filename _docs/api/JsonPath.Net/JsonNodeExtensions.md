---
layout: "page"
title: "JsonNodeExtensions Class"
bookmark: "JsonNodeExtensions"
permalink: "/api/JsonPath.Net/:title/"
order: "10.08.008"
---
**Namespace:** Json.Path

**Inheritance:**
`JsonNodeExtensions`
 🡒 
`object`

Useful extensions for **System.Text.Json.Nodes.JsonNode**.

## Methods

### TryGetSingleValue(this JsonNode node, out JsonNode value)

Ensures a **System.Text.Json.Nodes.JsonNode** only represents a single value.

#### Declaration

```c#
public static bool TryGetSingleValue(this JsonNode node, out JsonNode value)
```

| Parameter | Type | Description |
|---|---|---|
| node | JsonNode |  |
| value | out JsonNode |  |


#### Returns

Within the context of this library, a **Json.Path.NodeList**
may be stored inside a **System.Text.Json.Nodes.JsonNode**.  Some operations, such as
expression addition, require that a single value is provided.

This method checks to see if the underlying value of a `JsonNode`
is a `NodeList`.  If not, it simply sets <paramref name="value" /> to the JsonNode
and returns true.  If the underlying value is a `NodeList` _and_ it only
contains a single value, it sets <paramref name="value" /> to that JsonNode and
return true.  Otherwise, it returns false.

#### Remarks

Though a bit complex, this method can be very important for functions
that require single values as inputs rather than nodelists since function
composition is possible (e.g. `min(max(@,0),10)`) and functions return nodelists.

### TryGetSingleValue(this NodeList nodeList, out JsonNode value)

Ensures a **Json.Path.NodeList** only represents a single value.

#### Declaration

```c#
public static bool TryGetSingleValue(this NodeList nodeList, out JsonNode value)
```

| Parameter | Type | Description |
|---|---|---|
| nodeList | NodeList |  |
| value | out JsonNode |  |


#### Returns

Within the context of this library, a **Json.Path.NodeList**
may be stored inside a **System.Text.Json.Nodes.JsonNode**.  Some operations, such as
expression addition, require that a single value is provided.

This method checks to see if the underlying value of a `JsonNode`
is a `NodeList`.  If not, it simply sets <paramref name="value" /> to the JsonNode
and returns true.  If the underlying value is a `NodeList` _and_ it only
contains a single value, it sets <paramref name="value" /> to that JsonNode and
return true.  Otherwise, it returns false.

#### Remarks

Though a bit complex, this method can be very important for functions
that require single values as inputs rather than nodelists since function
composition is possible (e.g. `min(max(@,0),10)`) and functions return nodelists.

### TryGetValue(this JsonNode node, out T value)


#### Declaration

```c#
public static bool TryGetValue(this JsonNode node, out T value)
```


#### Returns


