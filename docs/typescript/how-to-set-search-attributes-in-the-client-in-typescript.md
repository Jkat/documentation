---
id: how-to-set-search-attributes-in-the-client-in-typescript
title: How to set Search Attributes in the Client in TypeScript
sidebar_label: Use Search Attributes in the Client
description: Use Search Attributes in the Client
tags:
  - developer-guide
  - sdk
  - typescript
---

We can set [`WorkflowOptions.searchAttributes`](https://typescript.temporal.io/api/interfaces/client.WorkflowOptions#searchattributes) during `client.start()` or `client.execute()` and read with [`handle.describe()`](https://typescript.temporal.io/api/interfaces/client.WorkflowHandle#describe):

<!--SNIPSTART typescript-search-attributes-client -->
<!--SNIPEND-->

The type of `searchAttributes` is `Record<string, string[] | number[] | boolean[] | Date[]>`.