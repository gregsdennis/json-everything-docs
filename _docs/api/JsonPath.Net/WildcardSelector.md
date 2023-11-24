---
layout: "page"
title: "WildcardSelector Class"
bookmark: "WildcardSelector"
permalink: "/api/JsonPath.Net/:title/"
0.08.029"
---
**Namespace:** Json.Path

**Inheritance:**
`WildcardSelector`
 🡒 
`object`

**Implemented interfaces:**

- ISelector
- IHaveShorthand

Represents a wildcard selector, `[*]` or `.*`.

## Methods

### BuildString(StringBuilder builder)

Builds a string using a string builder.

#### Declaration

```c#
public void BuildString(StringBuilder builder)
```

| Parameter | Type | Description |
|---|---|---|
| builder | StringBuilder | The string builder. |


### Evaluate(Node match, JsonNode rootNode)

Evaluates the selector.

#### Declaration

```c#
public IEnumerable<Node> Evaluate(Node match, JsonNode rootNode)
```

| Parameter | Type | Description |
|---|---|---|
| match | Node | The node to evaluate. |
| rootNode | JsonNode | The root node (typically used by filter selectors, e.g. `$[?@foo < $.bar]`) |


#### Returns

A collection of nodes.
            
Semantically, this is a nodelist, but leaving as IEnumerable&lt;Node&gt; allows for deferred execution.

### ToString()

Returns a string that represents the current object.

#### Declaration

```c#
public override string ToString()
```


#### Returns

A string that represents the current object.

