# Overview

This repository contains multiple callable workflows that allow sharing the
most common actions between projects without having to remember to copy and
paste them and keep them updated constantly.

This repository *does not* contain composite actions. Each of those are instead
placed into their own repository and in some cases called by the workflows
found here.

For security reasons, [renovatebot](https://github.com/renovatebot/renovate) is
used to keep workflows locked to a specific commit version as recommended for
security hardening.

# Usage

Per documentation found [here][1], calling workflows from elsewhere looks like
the following:

```yaml
jobs:
  actionlint:
    uses: bruxisma/actions/.github/workflows/actionlint.yml@main
  node.audit:
    uses: bruxisma/actions/.github/workflows/node.audit.yml@main
    with:
      audit-level: severe
```

[1]: https://docs.github.com/en/actions/using-workflows/reusing-workflows#calling-a-reusable-workflow
