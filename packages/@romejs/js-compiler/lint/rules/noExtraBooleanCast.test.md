# `noExtraBooleanCast.test.ts`

**DO NOT MODIFY**. This file has been autogenerated. Run `rome test packages/@romejs/js-compiler/lint/rules/noExtraBooleanCast.test.ts --update-snapshots` to update.

## `disallow unnecessary boolean casts`

### `0`

```

 unknown:2:8 lint/noExtraBooleanCast ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

  ✖ Redundant double negation.

  > 2 │     if (Boolean(foo)) {
      │         ^^^^^^^^^^^^
    3 │       return foo;
    4 │     }

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

✖ Found 1 problem

```

### `0: formatted`

```
if (Boolean(foo)) {
  return foo;
}

```

### `1`

```

 unknown:2:11 lint/noExtraBooleanCast ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

  ✖ Redundant double negation.

  > 2 │     while (!!foo) {
      │            ^^^^^
    3 │       return foo;
    4 │     }

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

✖ Found 1 problem

```

### `1: formatted`

```
while (!!foo) {
  return foo;
}

```

### `2`

```

 unknown:6:13 lint/noExtraBooleanCast ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

  ✖ Redundant double negation.

    4 │     do {
    5 │         1+1;
  > 6 │     } while (Boolean(x));
      │              ^^^^^^^^^^
    7 │     

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

✖ Found 1 problem

```

### `2: formatted`

```
let x = 1;

do {
  1 + 1;
} while (Boolean(x));

```

### `3`

```

 unknown:2:11 lint/noExtraBooleanCast ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

  ✖ Redundant double negation.

  > 2 │     for (; !!foo; ) {
      │            ^^^^^
    3 │       return 1+1;
    4 │     }

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

✖ Found 1 problem

```

### `3: formatted`

```
while (!!foo) {
  return 1 + 1;
}

```
