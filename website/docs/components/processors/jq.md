---
title: jq
type: processor
---

<!--
     THIS FILE IS AUTOGENERATED!

     To make changes please edit the contents of:
     lib/processor/jq.go
-->


Transforms and filters messages using jq queries.


import Tabs from '@theme/Tabs';

<Tabs defaultValue="common" values={[
  { label: 'Common', value: 'common', },
  { label: 'Advanced', value: 'advanced', },
]}>

import TabItem from '@theme/TabItem';

<TabItem value="common">

```yaml
# Common config fields, showing default values
jq:
  query: .
```

</TabItem>
<TabItem value="advanced">

```yaml
# All config fields, showing default values
jq:
  query: .
  raw: false
  raw_output: false
  slurp: false
```

</TabItem>
</Tabs>

Works by taking all parts of a message and passing them through gojq. The
resulting objects from gojq become the new message parts.

Query syntax is described in [jq's documentation][jq-docs].

[jq-docs]: https://stedolan.github.io/jq/manual/

## Fields

### `query`

The jq query to filter and transform messages with.


Type: `string`  
Default: `"."`  

### `raw`

Whether to process the input as a raw string instead of as JSON.


Type: `bool`  
Default: `false`  

### `raw_output`

Whether to emit string results as raw bytes instead of as JSON.


Type: `bool`  
Default: `false`  

### `slurp`

Whether to query all parts as an array instead of querying individual inputs. Per-part metadata is not available if true.


Type: `bool`  
Default: `false`  

