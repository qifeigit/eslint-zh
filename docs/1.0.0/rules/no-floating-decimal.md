---
title: Rule no-floating-decimal
layout: doc
---
<!-- Note: No pull requests accepted for this file. See README.md in the root directory for details. -->
# Disallow Floating Decimals (no-floating-decimal)

Float values in JavaScript contain a decimal point, and there is no requirement that the decimal point be preceded or followed by a number. For example, the following are all valid JavaScript numbers:

```js
var num = .5;
var num = 2.;
var num = -.7;
```

Although not a syntax error, this format for numbers can make it difficult to distinguish between true decimal numbers and the dot operator. For this reason, some recommend that you should always include a number before and after a decimal point to make it clear the intent is to create a decimal number.

## Rule Details

This rule is aimed at eliminating floating decimal points and will warn whenever a numeric value has a decimal point but is missing a number either before or after it.

The following patterns are considered warnings:

```js
var num = .5;
var num = 2.;
var num = -.7;
```

The following patterns are not considered warnings:

```js
var num = 0.5;
var num = 2.0;
```

## Compatibility

* **JSHint**: W008

## When Not To Use It

If you aren't concerned about misinterpreting floating decimal point values, then you can safely turn this rule off.

## Further Reading

* [A leading decimal point can be confused with a dot](http://jslinterrors.com/a-leading-decimal-point-can-be-confused-with-a-dot-a/)

## Version

This rule was introduced in ESLint 0.0.6.

## Resources

* [Rule source](https://github.com/eslint/eslint/tree/master/lib/rules/no-floating-decimal.js)
* [Documentation source](https://github.com/eslint/eslint/tree/master/docs/rules/no-floating-decimal.md)
