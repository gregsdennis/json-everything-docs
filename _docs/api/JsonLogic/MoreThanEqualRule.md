---
layout: "page"
title: "MoreThanEqualRule Class"
bookmark: "MoreThanEqualRule"
permalink: "/api/JsonLogic/:title/"
order: "9.10.27"
---
**Namespace:** Json.Logic.Rules

**Inheritance:**
`MoreThanEqualRule`
 🡒 
`Rule`
 🡒 
`object`

Handles the `&gt;=` operation.

## Methods

### Apply(JsonNode data, JsonNode contextData)

Applies the rule to the input data.

#### Declaration

```c#
public override JsonNode Apply(JsonNode data, JsonNode contextData)
```

| Parameter | Type | Description |
|---|---|---|
| data | JsonNode | The input data. |
| contextData | JsonNode | Optional secondary data.  Used by a few operators to pass a secondary<br>    data context to inner operators. |


#### Returns

The result of the rule.

