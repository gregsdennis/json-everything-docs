---
layout: "page"
title: "RecursiveRefKeyword Class"
bookmark: "RecursiveRefKeyword"
permalink: "/api/JsonSchema.Net/:title/"
0.01.139"
---
**Namespace:** Json.Schema

**Inheritance:**
`RecursiveRefKeyword`
 🡒 
`object`

**Implemented interfaces:**

- IJsonSchemaKeyword

Handles `$recursiveRef`.

## Fields

| Name | Type | Summary |
|---|---|---|
| **Name** | string | The JSON name of the keyword. |

## Properties

| Name | Type | Summary |
|---|---|---|
| **Reference** | Uri | The URI reference. |

## Constructors

### RecursiveRefKeyword(Uri value)

Creates a new **Json.Schema.RecursiveRefKeyword**.

#### Declaration

```c#
public RecursiveRefKeyword(Uri value)
```

| Parameter | Type | Description |
|---|---|---|
| value | Uri | The URI. |


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

