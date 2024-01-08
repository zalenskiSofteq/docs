---
acl_categories:
- '@slow'
- '@scripting'
arguments:
- display_text: script
  name: script
  type: string
arity: 3
command_flags:
- noscript
- stale
complexity: O(N) with N being the length in bytes of the script body.
description: Loads a server-side Lua script to the script cache.
group: scripting
hidden: false
hints:
- request_policy:all_nodes
- response_policy:all_succeeded
linkTitle: SCRIPT LOAD
since: 2.6.0
summary: Loads a server-side Lua script to the script cache.
syntax_fmt: SCRIPT LOAD script
syntax_str: ''
title: SCRIPT LOAD
---
Load a script into the scripts cache, without executing it.
After the specified command is loaded into the script cache it will be callable
using [`EVALSHA`](/commands/evalsha) with the correct SHA1 digest of the script, exactly like after
the first successful invocation of [`EVAL`](/commands/eval).

The script is guaranteed to stay in the script cache forever (unless `SCRIPT
FLUSH` is called).

The command works in the same way even if the script was already present in the
script cache.

For more information about [`EVAL`](/commands/eval) scripts please refer to [Introduction to Eval Scripts](/topics/eval-intro).