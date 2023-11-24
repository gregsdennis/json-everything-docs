---
layout: "page"
title: "JsonPathExtensions Class"
bookmark: "JsonPathExtensions"
permalink: "/api/JsonPath.Net/:title/"
0.08.011"
---
**Namespace:** Json.Path

**Inheritance:**
`JsonPathExtensions`
 🡒 
`object`

Provides extended functionality for **Json.Path.JsonPath**.

## Methods

### AsJsonPointer(this JsonPath path)

Renders a Singular Path as a JSON Pointer.

#### Declaration

```c#
public static string AsJsonPointer(this JsonPath path)
```

| Parameter | Type | Description |
|---|---|---|
| path | JsonPath | A JSON Path which is a Singular Path. |


#### Returns

A string containing a JSON Pointer.

