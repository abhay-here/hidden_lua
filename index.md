# Lua Tutorial for Programmers
A simple and short Lua 5.4 tutorial covering every aspect of Lua. Made for programmers.

## Variables
### Global Variables
This is how you declare a global variable.

```lua
    age = 56
    name = "Dalton"
    is_here = false
```

### Local Variables
Variables are global by default. To make them local, use the local keyword. These all are local variables. Lexically scoped.

```lua
    local name = "Joey"
    local is_alive = true
```

### Constant Variables
You can also make locals constant. Reassigning a local constant variable throws an error. You cannot make global variables constant.
```lua
    local NAME <const> = "John"
    local PI <const> = 3.14

    PI = 4 -- Error!
```

`<const>` is actually an attribute that you can apply to a local variable. There is one more attribute `<close>`. It is somewhat like RAII. Explanation ahead.

### Mutiple assignment
You can assign multiple variables at once. They can all be global or local.
```lua
    x, y = 45, 54
    local a, b, c = 1, 2, 3
```

---

**TIP**: Locals are faster than globals.

---

## Data Types
There are eight data types in Lua: nil, boolean, number, string, function, userdata, thread, and table.

`nil` represents the absense of any useful value like `null` in other languages.

Only `nil` and `false` are falsy and everything else including `""` and `0` are considered as true.

A boolean can be `true` or `false`. All lowercase.

A number can be an integer or a decimal number. It may be positive or negative.
```lua
    384
    -2347
    
    12.35
    -65.385

    -- Hexadecimal numbers. Case insensitive.
    0xfffeee
    0Xaaa
    0xFaB
    0XFFFF
    0xaaa.cdc

    8.1e2    -- equals 8.1 * 10 ^ 2
    134e-4   -- equals 134 * 10 ^ -4
    5e5      -- equals 5 * 10 ^ 5
```

Number seperators are not supported so numbers like `1_000_000` are invalid.
