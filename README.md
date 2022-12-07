# Swift Artifactbundle Builder

- build swift executable binary and upload to artifact

# Usage

```yml
strategy:
  matrix:
  os: [ ubuntu-latest, macos-latest ]

runs-on: ${{ matrix.os }}

steps:
- uses: actions/checkout@v3
- uses: swiftty/swiftpm-artifactbundle-builder@v1
  with:
    swift-version: '5.7'
    depth: 1
```

after build, use [swiftpm-artifactbundle-bundler](https://github.com/swiftty/swiftpm-artifactbundle-bundler) to make artifactbundle.
