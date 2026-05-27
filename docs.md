---
layout: page
title: Documentation
permalink: /docs/
---

## Overview

This page provides an in-depth reference for Minodu. If you're just starting out, read the [Getting Started](../getting-started) guide first.

---

## Configuration

Minodu is configured via a `minodu.config.*` file (or equivalent). Supported options:

| Option | Type | Default | Description |
|--------|------|---------|-------------|
| `option_a` | string | `"default"` | What this option controls. |
| `option_b` | boolean | `false` | What this flag enables. |
| `option_c` | number | `42` | What this value affects. |

---

## API Reference

### `minodu.doSomething(args)`

**Parameters**

| Name | Type | Required | Description |
|------|------|----------|-------------|
| `arg1` | string | ✅ | What arg1 is. |
| `arg2` | object | ❌ | Optional options object. |

**Returns** `Promise<Result>` — describe the return value.

**Example**

```js
const result = await minodu.doSomething("hello", { verbose: true });
console.log(result);
```

---

## Examples

### Example 1 — Basic usage

```bash
minodu run --input file.txt
```

### Example 2 — Advanced usage

```bash
minodu run --input file.txt --output out/ --flag
```

---

## Troubleshooting

**Problem:** Something doesn't work.  
**Solution:** Try this.

**Problem:** Another common error.  
**Solution:** Do this instead.
