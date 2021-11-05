---
layout: "cloud"
page_title: "Monitoring - Terraform Cloud Agents - Terraform Cloud and Terraform Enterprise"
---

# Monitoring

When running Terraform Cloud Agents, it may be useful to monitor some of its output.

## Flash Messages

Flash Messages are a type of log that HashiCorp may send to agents from time to time. These messages may be used to communicate important or breaking changes to the agent. Flash Messages will be emitted when HashiCorp adds a new one, or when starting up an agent for the first time. Their output looks something like:

```
2021-09-22T15:20:59.269Z [WARN]  core.notice: A breaking change is incoming.
```

Flash Messages are version specific, and may only apply to the specific version of the agent you are running.

Adding monitoring and alerting for these `core.notice` messages may help you operate Terraform Cloud Agents more easily.