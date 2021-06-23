# Hidden Lua
Lesser known Lua features a described here. There's nothing "hidden" about it, they all are well documented.
It's very incomplete.

## Local Variable Attributes
There are two attributes: <const> and <close>.

<const> attribute makes the local somewhat immutable. Reassignment on a <const> throws error.
```lua
    local PI <const> = 3.14
    local NAME <const> = "Iron"
    local TILE_SIZE <const> = 16
    
    PI = 34.1 -- Error!
```

<close> behaves somewhat like RAII.
```lua
    do
        local file <close> = io.open()
    end
```
## Weird Long String and Comments
You can put any number of equal signs between the square brackets.
```lua
    --[=[
        I am legal.
    ]=]
    --[===[
        Legal.
    ]===]
    ---[=====[
        Legal.
    ]=====]
    
    local msg = [===[
        I am legal too.
    ]===]
    
    --[=[
        Illegal!
    ]===]
```
