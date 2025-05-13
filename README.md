# 42ByteLabs GitHub Repository

## Reusable Workflows

### Cargo

Full end-to-end Rust workflow to make it easier to build and publish Rust crates.

<details>
<summary>Cargo Build Workflow</summary>
  
```yaml
name: Build and Test

on:
  push:
    branches: ["main"]
  pull_request:
    branches: ["main"]

env:
  CARGO_TERM_COLOR: always

jobs:
  build:
    # https://github.com/42ByteLabs/.github/blob/main/.github/workflows/cargo.yml
    uses: 42ByteLabs/.github/.github/workflows/cargo.yml@main
    secrets: inherit
    permissions:
      contents: read
      actions: read
      security-events: write
    with:
      # [optional] Selected features
      features: ""
      # [optional] Running Examples
      examples: "true"
```
</details>

