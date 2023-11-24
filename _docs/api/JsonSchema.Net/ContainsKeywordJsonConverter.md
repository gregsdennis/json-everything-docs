---
layout: "page"
title: "ContainsKeywordJsonConverter Class"
bookmark: "ContainsKeywordJsonConverter"
permalink: "/api/JsonSchema.Net/:title/"
0.01.016"
---
**Namespace:** Json.Schema

**Inheritance:**
`ContainsKeywordJsonConverter`
 🡒 
`JsonConverter<ContainsKeyword>`
 🡒 
`JsonConverter`
 🡒 
`object`

JSON converter for **Json.Schema.ContainsKeyword**.

## Properties

| Name | Type | Summary |
|---|---|---|
| **HandleNull** | bool |  |

## Methods

### Read(ref Utf8JsonReader reader, Type typeToConvert, JsonSerializerOptions options)

Reads and converts the JSON to type **Json.Schema.ContainsKeyword**.

#### Declaration

```c#
public override ContainsKeyword Read(ref Utf8JsonReader reader, Type typeToConvert, JsonSerializerOptions options)
```

| Parameter | Type | Description |
|---|---|---|
| reader | ref Utf8JsonReader | The reader. |
| typeToConvert | Type | The type to convert. |
| options | JsonSerializerOptions | An object that specifies serialization options to use. |


#### Returns

The converted value.

### Write(Utf8JsonWriter writer, ContainsKeyword value, JsonSerializerOptions options)

Writes a specified value as JSON.

#### Declaration

```c#
public override void Write(Utf8JsonWriter writer, ContainsKeyword value, JsonSerializerOptions options)
```

| Parameter | Type | Description |
|---|---|---|
| writer | Utf8JsonWriter | The writer to write to. |
| value | ContainsKeyword | The value to convert to JSON. |
| options | JsonSerializerOptions | An object that specifies serialization options to use. |


