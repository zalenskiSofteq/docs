---
acl_categories:
- '@slow'
- '@connection'
arity: 2
command_flags:
- loading
- stale
complexity: O(1)
description: Returns a count of commands.
group: server
hidden: false
linkTitle: COMMAND COUNT
since: 2.8.13
summary: Returns a count of commands.
syntax_fmt: COMMAND COUNT
syntax_str: ''
title: COMMAND COUNT
---
Returns [Integer reply](/docs/reference/protocol-spec#integers) of number of total commands in this Redis server.

## Examples

{{% redis-cli %}}
COMMAND COUNT
{{% /redis-cli %}}
