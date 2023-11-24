---
layout: page
title: JsonPointer.Net
icon: fas fa-tag
order: "9.10"
---
# [3.2.0](https://github.com/gregsdennis/json-everything/pull/564) {#release-pointer-3.2.0}

[#549](https://github.com/gregsdennis/json-everything/issues/549) - Expose JSON converters for all types to support JSON source generation.

# [3.1.0](https://github.com/gregsdennis/json-everything/pull/509) {#release-pointer-3.1.0}

Enhanced support for creating pointers via Linq expressions.

- Added support for the Linq method `.Last()` to generate a `-` segment which indicates the index beyond the last item in an array.
- Added support for `[JsonPropertyName]` attribute.
- Added support for custom naming transformations.

# [3.0.3](https://github.com/gregsdennis/json-everything/pull/509) {#release-pointer-3.0.3}

Improved performance for `JsonPointer.ToString()` by caching the string representation so that it's only generated once.

# [3.0.2](https://github.com/gregsdennis/json-everything/pull/492) {#release-pointer-3.0.2}

Memory and performance improvements.

# [3.0.1](https://github.com/gregsdennis/json-everything/pull/425) {#release-pointer-3.0.1}

[#408](https://github.com/gregsdennis/json-everything/issues/408) - Fixed an issue where an empty string segment fails for array values.  Thanks to [@mbj2011](https://github.com/mbj2011) for finding and reporting this.

# [3.0.0](https://github.com/gregsdennis/json-everything/pull/326) {#release-pointer-3.0.0}

Updated model to more correctly represent a basic JSON Pointer.

- URL encoding is merely a formatting concern
- Removed `UrlEmpty`
- `Parse()` and `TryParse()` are still tolerant of URL encoded pointers and will decode automatically
- Removed `Source` property as `ToString()` is the default method for getting a string
- Renamed `JsonPointerKind` to `JsonPointerStyle` to reflect the formatting nature of its purpose
- Added `ToString(JsonPointerKind)` to support outputting in URL encoded format

Added implicit cast from `int` to `PointerSegment`.  Previously, only a cast from `uint` existed, but typing `int`s is easier.

# 2.2.1 (no PR) {#release-pointer-2.2.1}

[#288](https://github.com/gregsdennis/json-everything/issues/288) - Just bumping version to allow dependent packages to pick up the latest Json.More.Net by default, which is transitively pulled via this package.

# [2.2.0](https://github.com/gregsdennis/json-everything/pull/243) {#release-pointer-2.2.0}

Updated System.Text.Json to version 6 in order to add `JsonNode` support.

The API is shaped a bit differently for `JsonNode` than the existing API for `JsonElement`.  Specifically, it exposes

```c#
bool TryEvaluate(JsonNode node, out JsonNode? result)
```

instead of the `Evaluate()` call you've all come to know and love.

This is because .Net decided to do a [silly thing](https://github.com/dotnet/runtime/issues/66948#issuecomment-1080148457) and represent JSON null using .Net null.  This decision means that a null returned here cannot be distinguished between not existing and existing with a value of JSON null.

`RelativeJsonPointer` is now implemented! ...for `JsonNode`.

# [2.1.0](https://github.com/gregsdennis/json-everything/pull/185) {#release-pointer-2.1.0}

[#184](https://github.com/gregsdennis/json-everything/issues/184) - [@JanKnipp](https://github.com/JanKnipp) added array (e.g. `int[]`) support to Linq expression construction of pointers.

# [2.0.0](https://github.com/gregsdennis/json-everything/pull/179) {#release-pointer-2.00}

[#171](https://github.com/gregsdennis/json-everything/issues/171) - Updated `JsonPointer`, `PointerSegment`, and `RelativeJsonPointer` from struct to class since it holds by-reference data anyway.  Removes parameterless constructor for these types.  These changes make them better immutable models.

# [1.4.0](https://github.com/gregsdennis/json-everything/pull/162) {#release-pointer-1.4.0}

- Added implicit casts from `int` and `string` to `PointerSegment`
- Added params overload for `JsonPointer.Create()`.

# [1.3.3](https://github.com/gregsdennis/json-everything/pull/130) {#release-pointer-1.3.3}

[#123](https://github.com/gregsdennis/json-everything/pull/123) - Removed a copy/paste error that shows up while deserializing relative pointers.  Thanks to [@bastiaantenklooster](https://github.com/bastiaantenklooster) for finding this and creating a PR to fix it.

# [1.3.2](https://github.com/gregsdennis/json-everything/pull/75) {#release-pointer-1.3.2}

Added support for nullable reference types.

# [1.3.1](https://github.com/gregsdennis/json-everything/pull/61) {#release-pointer-1.3.1}

Signed the DLL for strong name compatibility.

# [1.3.0](https://github.com/gregsdennis/json-everything/pull/58) {#release-pointer-1.3.0}

Added support pointer creation using lambda expressions, e.g. `x => x.foo[5].bar` to create `/foo/5/bar`.

# [1.2.0](https://github.com/gregsdennis/json-everything/pull/52) {#release-pointer-1.2.0}

Added support for array index manipulation in Relative JSON Pointer 2 (spec updated alongside JSON Schema Draft 2020-12).

# [1.1.2](https://github.com/gregsdennis/json-everything/pull/45) {#release-pointer-1.1.2}

Added debug symbols to package.  No functional change.

# [1.1.1](https://github.com/gregsdennis/json-everything/pull/12) {#release-pointer-1.1.1}

Updated reference to Json.More<nsp>.Net.

# [1.1.0](https://github.com/gregsdennis/json-everything/pull/7) {#release-pointer-1.1.0}

Added `JsonPointerKind` enumeration.

Added `JsonPointer.Kind` property.

Added optional parameters to `JsonPointer.Parse()` and `JsonPointer.TryParse()`.

# 1.0.0 {#release-pointer-1.0.0}

Initial release.
