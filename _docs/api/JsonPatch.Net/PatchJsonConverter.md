---
layout: "page"
title: "PatchJsonConverter Class"
bookmark: "PatchJsonConverter"
permalink: "/api/JsonPatch.Net/:title/"
order: "10.09.003"
---
**Namespace:** Json.Patch

**Inheritance:**
`PatchJsonConverter`
 🡒 
`WeaklyTypedJsonConverter<JsonPatch>`
 🡒 
`JsonConverter<JsonPatch>`
 🡒 
`JsonConverter`
 🡒 
`object`

**Implemented interfaces:**

- IWeaklyTypedJsonConverter

Provides JSON conversion logic for **Json.Patch.JsonPatch**.

## Properties

| Name | Type | Summary |
|---|---|---|
| **HandleNull** | bool |  |
| **Type** | Type |  |

## Methods

### Read(ref Utf8JsonReader reader, Type typeToConvert, JsonSerializerOptions options)

Reads and converts the JSON to type **Json.Patch.JsonPatch**.

#### Declaration

```c#
public override JsonPatch Read(ref Utf8JsonReader reader, Type typeToConvert, JsonSerializerOptions options)
```

| Parameter | Type | Description |
|---|---|---|
| reader | ref Utf8JsonReader | The reader. |
| typeToConvert | Type | The type to convert. |
| options | JsonSerializerOptions | An object that specifies serialization options to use. |


#### Returns

The converted value.

### Write(Utf8JsonWriter writer, JsonPatch value, JsonSerializerOptions options)

Writes a specified value as JSON.

#### Declaration

```c#
public override void Write(Utf8JsonWriter writer, JsonPatch value, JsonSerializerOptions options)
```

| Parameter | Type | Description |
|---|---|---|
| writer | Utf8JsonWriter | The writer to write to. |
| value | JsonPatch | The value to convert to JSON. |
| options | JsonSerializerOptions | An object that specifies serialization options to use. |


