---
layout: "page"
title: "ConstraintExtensions Class"
bookmark: "ConstraintExtensions"
permalink: "/api/JsonSchema.Net/:title/"
0.01.014"
---
**Namespace:** Json.Schema

**Inheritance:**
`ConstraintExtensions`
 🡒 
`object`

Convenience extensions for building constraints and processing evaluations.

## Methods

### GetKeywordConstraint(this IEnumerable\<KeywordConstraint\> constraints)

Gets a constraint from a keyword with the given type.

#### Declaration

```c#
public static KeywordConstraint GetKeywordConstraint(this IEnumerable<KeywordConstraint> constraints)
```

| Parameter | Type | Description |
|---|---|---|
| constraints | IEnumerable\<KeywordConstraint\> | The set of constraints. |


#### Returns

The keyword evaluation, if it exists.

### GetKeywordEvaluation(this KeywordEvaluation evaluation)

Gets an evaluation from a keyword with the given type.

#### Declaration

```c#
public static KeywordEvaluation GetKeywordEvaluation(this KeywordEvaluation evaluation)
```

| Parameter | Type | Description |
|---|---|---|
| evaluation | KeywordEvaluation | The source evaluation. |


#### Returns

The keyword evaluation, if it exists.

