lulip
=====

Line-level profiler for code running in LuaJIT

References
-----

- https://blog.cloudflare.com/cloudflares-new-waf-compiling-to-lua/
- https://blog.jgc.org/2013/04/lulip-line-level-profiler-for-code.html
- https://github.com/googlearchive/code-prettify

Usage
-----

```Lua
local profiler = require 'lulip'
local p = profiler:new()
p:dont('some-module')
p:maxrows(25)
p:start()

-- execute code here

p:stop()
p:dump(output_file_name)
```
