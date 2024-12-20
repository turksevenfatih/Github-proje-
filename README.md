# Github-proje-
Türkseven Fatih Programlama Dili Çalışmaları 
on:
  pull_request:
    branches: [main]
    paths:
      - 'readme.md'
jobs:
  lint:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4
        with:
          fetch-depth: 0
      - name: awesome-lint
        run: ./.github/workflows/repo_linter.sh
