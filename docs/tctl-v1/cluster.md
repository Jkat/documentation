---
id: cluster
title: tctl v1.16 cluster command reference
sidebar_label: cluster
description: How to use the tctl v1.16 cluster command
toc_max_heading_level: 4
---

<!-- THIS FILE IS GENERATED. DO NOT EDIT THIS FILE DIRECTLY -->

import Tabs from '@theme/Tabs';
import TabItem from '@theme/TabItem';

The `tctl cluster` command enables [Temporal Cluster](/clusters#) operations.

- [`tctl cluster health`](#health)
- [`tctl cluster get-search-attributes`](#get-search-attributes)

## get-search-attributes

The `tctl cluster get-search-attributes` command lists all [Search Attributes](/visibility#search-attribute) that can be used in the `--query` modifier of the [`tctl workflow list`](/tctl-v1/workflow#list) command and the `--search_attr_key` and `--search_attr_value` modifiers of the [`tctl workflow run`](/tctl-v1/workflow#run) and [`tctl workflow start`](/tctl-v1/workflow#start) commands.

**Example:**

```bash
tctl cluster get-search-attributes
```

The command has no modifiers.

Example output:

```text
+-----------------------+----------+
|         NAME          |   TYPE   |
+-----------------------+----------+
| BinaryChecksums       | Keyword  |
| CloseTime             | Int      |
| CustomBoolField       | Bool     |
| CustomDatetimeField   | Datetime |
| CustomDoubleField     | Double   |
| CustomIntField        | Int      |
| CustomKeywordField    | Keyword  |
| CustomNamespace       | Keyword  |
| CustomStringField     | String   |
| ExecutionStatus       | Int      |
| ExecutionTime         | Int      |
| Operator              | Keyword  |
| RunId                 | Keyword  |
| StartTime             | Int      |
| TaskQueue             | Keyword  |
| TemporalChangeVersion | Keyword  |
| WorkflowId            | Keyword  |
| WorkflowType          | Keyword  |
+-----------------------+----------+
```

The admin version of this command displays default and custom Search Attributes separately, and also shows the underlying Elasticsearch index schema and system Workflow status.

## health

The `tctl cluster health` command checks the health of the [Frontend Service](/concepts/what-is-a-temporal-cluster/#frontend-service).

`tctl cluster health`

The command has no modifiers.
