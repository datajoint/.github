# Datajoint Github Actions Workflow

## Github Actions Workflow Triggers
- before release
```
name: <Github Actions Workflow Name>
on:
  pull_request:
  push:
    branches:
      - '**'
    tags-ignore:
      - '**'
  workflow_dispatch:
```

- depending on a prior workflow run, most of the time for security purpose
```
name: <Github Actions Workflow Name>
on:
  workflow_run:
    workflows: ["<Dependent Workflow Name>"]
    types:
      - completed
```

- tag to release
```
name: <Github Actions Workflow Name>
on:
  push:
    tags:
      - '*.*.*'
      - 'test*.*.*'
```

## Reusable Workflow Callers
- mkdocs
```
jobs:
  call_mkdocs_release:
    uses: datajoint/.github/.github/workflows/mkdocs_release.yaml@main
    permissions: 
      contents: write # give github actions permission to push gh-pages branch
```

- context check(optional: mostly for debugging github actions workflows)
```
jobs:
  call_context_check:
    uses: datajoint/.github/.github/workflows/context_check.yaml@main
```

