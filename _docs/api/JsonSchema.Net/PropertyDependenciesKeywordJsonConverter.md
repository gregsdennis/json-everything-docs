---
layout: "page"
title: "PropertyDependenciesKeywordJsonConverter Class"
bookmark: "PropertyDependenciesKeywordJsonConverter"
permalink: "/api/JsonSchema.Net/:title/"
0.01.130"
---
**Namespace:** Json.Schema

**Inheritance:**
`PropertyDependenciesKeywordJsonConverter`
 🡒 
`JsonConverter<PropertyDependenciesKeyword>`
 🡒 
`JsonConverter`
 🡒 
`object`

JSON converter for **Json.Schema.PropertyDependenciesKeyword**.

## Properties

| Name | Type | Summary |
|---|---|---|
| **HandleNull** | bool |  |

## Methods

### Read(ref Utf8JsonReader reader, Type typeToConvert, JsonSerializerOptions options)

Reads and converts the JSON to type **Json.Schema.PropertyDependenciesKeyword**.

#### Declaration

```c#
public override PropertyDependenciesKeyword Read(ref Utf8JsonReader reader, Type typeToConvert, JsonSerializerOptions options)
```

| Parameter | Type | Description |
|---|---|---|
| reader | ref Utf8JsonReader | The reader. |
| typeToConvert | Type | The type to convert. |
| options | JsonSerializerOptions | An object that specifies serialization options to use. |


#### Returns

The converted value.

### Write(Utf8JsonWriter writer, PropertyDependenciesKeyword value, JsonSerializerOptions options)

Writes a specified value as JSON.

#### Declaration

```c#
public override void Write(Utf8JsonWriter writer, PropertyDependenciesKeyword value, JsonSerializerOptions options)
```

| Parameter | Type | Description |
|---|---|---|
| writer | Utf8JsonWriter | The writer to write to. |
| value | PropertyDependenciesKeyword | The value to convert to JSON. |
| options | JsonSerializerOptions | An object that specifies serialization options to use. |


