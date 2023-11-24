---
layout: "page"
title: "MinLengthKeyword Class"
bookmark: "MinLengthKeyword"
permalink: "/api/JsonSchema.Net/:title/"
0.01.107"
---
**Namespace:** Json.Schema

**Inheritance:**
`MinLengthKeyword`
 🡒 
`object`

**Implemented interfaces:**

- IJsonSchemaKeyword

Handles `minLength`.

## Fields

| Name | Type | Summary |
|---|---|---|
| **Name** | string | The JSON name of the keyword. |

## Properties

| Name | Type | Summary |
|---|---|---|
| **Value** | uint | The minimum expected string length. |

## Constructors

### MinLengthKeyword(uint value)

Creates a new **Json.Schema.MinLengthKeyword**.

#### Declaration

```c#
public MinLengthKeyword(uint value)
```

| Parameter | Type | Description |
|---|---|---|
| value | uint | The minimum expected string length. |


## Methods

### GetConstraint(SchemaConstraint schemaConstraint, IReadOnlyList\<KeywordConstraint\> localConstraints, EvaluationContext context)

Builds a constraint object for a keyword.

#### Declaration

```c#
public KeywordConstraint GetConstraint(SchemaConstraint schemaConstraint, IReadOnlyList<KeywordConstraint> localConstraints, EvaluationContext context)
```

| Parameter | Type | Description |
|---|---|---|
| schemaConstraint | SchemaConstraint | The **Json.Schema.SchemaConstraint** for the schema object that houses this keyword. |
| localConstraints | IReadOnlyList\<KeywordConstraint\> | The set of other **Json.Schema.KeywordConstraint**s that have been processed prior to this one. Will contain the constraints for keyword dependencies. |
| context | EvaluationContext | The **Json.Schema.EvaluationContext**. |


#### Returns

A constraint object.

