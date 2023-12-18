# Workflows & Events: Deep Dive

## Event Activity Types & Filters

<p align="center"><img src ="images/event-activity-filter.png" /></p>

Each GitHub Action event can have activities or filters based on its type. Activities and filters allow us to configure a GitHub Action event in more detail.

If you decide to use types and filters, you'll have to expand each types like so -

```yaml
on:
  pull_request:
    types: 
      - opened
  workflow_dispatch:
  push:
    paths:
        - "**.js"
```

:warning: For a detailed example, you can have a look at `section-02-types-filters.yaml` workflow.

GitHub actions allows you to push a workflow based on many filters like - `paths`, `path-ignore`, `branches`, `branches-ignore` etc.

