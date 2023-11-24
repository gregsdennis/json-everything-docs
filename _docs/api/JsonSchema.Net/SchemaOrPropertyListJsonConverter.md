---
layout: "page"
title: "SchemaOrPropertyListJsonConverter Class"
bookmark: "SchemaOrPropertyListJsonConverter"
permalink: "/api/JsonSchema.Net/:title/"
0.01.154"
---
**Namespace:** Json.Schema

**Inheritance:**
`SchemaOrPropertyListJsonConverter`
 🡒 
`JsonConverter<SchemaOrPropertyList>`
 🡒 
`JsonConverter`
 🡒 
`object`

JSON converter for **Json.Schema.SchemaOrPropertyList**.

## Properties

| Name | Type | Summary |
|---|---|---|
| **HandleNull** | bool |  |

## Methods

### Read(ref Utf8JsonReader reader, Type typeToConvert, JsonSerializerOptions options)

Reads and converts the JSON to type **Json.Schema.SchemaOrPropertyList**.

#### Declaration

```c#
public override SchemaOrPropertyList Read(ref Utf8JsonReader reader, Type typeToConvert, JsonSerializerOptions options)
```

| Parameter | Type | Description |
|---|---|---|
| reader | ref Utf8JsonReader | The reader. |
| typeToConvert | Type | The type to convert. |
| options | JsonSerializerOptions | An object that specifies serialization options to use. |


#### Returns

The converted value.

### Write(Utf8JsonWriter writer, SchemaOrPropertyList value, JsonSerializerOptions options)

Writes a specified value as JSON.

#### Declaration

```c#
public override void Write(Utf8JsonWriter writer, SchemaOrPropertyList value, JsonSerializerOptions options)
```

| Parameter | Type | Description |
|---|---|---|
| writer | Utf8JsonWriter | The writer to write to. |
| value | SchemaOrPropertyList | The value to convert to JSON. |
| options | JsonSerializerOptions | An object that specifies serialization options to use. |


