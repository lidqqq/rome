# `noUnsafeFinally.test.ts`

**DO NOT MODIFY**. This file has been autogenerated. Run `rome test packages/@romejs/js-compiler/lint/rules/noUnsafeFinally.test.ts --update-snapshots` to update.

## `disallow unsafe usage of break, continue, throw and return`

### `0`

```

 unknown:8:12 lint/noUnsafeFinally ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

  ✖ Unsafe usage of ReturnStatement.

     6 │             throw err;
     7 │         } finally {
   > 8 │             return 1;
       │             ^^^^^^^^^
     9 │         }
    10 │       }

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

✖ Found 1 problem

```

### `0: formatted`

```
function greet1() {
  try {
    throw new Error('Try');
  } catch (err) {
    throw err;
  } finally {
    return 1;
  }
}

greet1();

```

### `1`

```

 unknown:8:12 lint/noUnsafeFinally ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

  ✖ Unsafe usage of BreakStatement.

     6 │             throw err;
     7 │         } finally {
   > 8 │             break;
       │             ^^^^^^
     9 │         }
    10 │       }

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

✖ Found 1 problem

```

### `1: formatted`

```
function greet2() {
  try {
    throw new Error('Try');
  } catch (err) {
    throw err;
  } finally {
    break;
  }
}

greet2();

```

### `2`

```

 unknown:8:12 lint/noUnsafeFinally ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

  ✖ Unsafe usage of ContinueStatement.

     6 │             throw err;
     7 │         } finally {
   > 8 │             continue;
       │             ^^^^^^^^^
     9 │         }
    10 │       }

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

✖ Found 1 problem

```

### `2: formatted`

```
function greet3() {
  try {
    throw new Error('Try');
  } catch (err) {
    throw err;
  } finally {
    continue;
  }
}

greet3();

```

### `3`

```

 unknown:8:12 lint/noUnsafeFinally ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

  ✖ Unsafe usage of ThrowStatement.

     6 │             throw err;
     7 │         } finally {
   > 8 │             throw new Error("Finally");
       │             ^^^^^^^^^^^^^^^^^^^^^^^^^^^
     9 │         }
    10 │       }

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

✖ Found 1 problem

```

### `3: formatted`

```
function greet4() {
  try {
    throw new Error('Try');
  } catch (err) {
    throw err;
  } finally {
    throw new Error('Finally');
  }
}

greet4();

```
