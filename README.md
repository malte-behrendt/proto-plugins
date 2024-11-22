# Proto Plugins

Collection of plugins for the runtime/tool version manager [proto](https://moonrepo.dev/proto).

## Plugins

| Name | Category | Description | Plugin Status | Install |
| ---- | -------- | ----------- | ------------- | ---------- |
| [trivy](https://github.com/aquasecurity/trivy) | tool | Comprehensive and versatile security scanner | Alpha | proto plugin add trivy [https://raw.githubusercontent.com/malte-behrendt/proto-plugins/main/trivy/plugin.toml](https://raw.githubusercontent.com/malte-behrendt/proto-plugins/main/trivy/plugin.toml) |
| [syft](https://github.com/anchore/syft) | tool | Generator for Software Bill of Materials (SBOM) from container images and filesystems | Alpha | proto plugin add syft [https://raw.githubusercontent.com/malte-behrendt/proto-plugins/main/syft/plugin.toml](https://raw.githubusercontent.com/malte-behrendt/proto-plugins/main/syft/plugin.toml) |
| [cyclonedx-cli](https://github.com/CycloneDX/cyclonedx-cli) | tool | Tool for SBOM analysis, merging, diffs and format conversions | Alpha | proto plugin add cyclonedx-cli [https://raw.githubusercontent.com/malte-behrendt/proto-plugins/main/cyclonedx-cli/plugin.toml](https://raw.githubusercontent.com/malte-behrendt/proto-plugins/main/cyclonedx-cli/plugin.toml) |
| [ast-grep](https://github.com/ast-grep/ast-grep) | tool | CLI for code structural search, lint and rewriting | Alpha | proto plugin add ast-grep [https://raw.githubusercontent.com/malte-behrendt/proto-plugins/main/ast-grep/plugin.toml](https://raw.githubusercontent.com/malte-behrendt/proto-plugins/main/ast-grep/plugin.toml) |
| [comby](https://github.com/comby-tools/comby) | tool | Code rewrite tool for structural search and replace that supports almost every language. | Alpha | proto plugin add comby [https://raw.githubusercontent.com/malte-behrendt/proto-plugins/main/comby/plugin.toml](https://raw.githubusercontent.com/malte-behrendt/proto-plugins/main/comby/plugin.toml) |
| [grit](https://github.com/getgrit/gritql)  | tool | GritQL is a query language for searching, linting, and modifying code. | Alpha | proto plugin add grit [https://raw.githubusercontent.com/malte-behrendt/proto-plugins/main/grit/plugin.toml](https://raw.githubusercontent.com/malte-behrendt/proto-plugins/main/grit/plugin.toml) |
| [spacemod](https://github.com/untitaker/spacemod)  | tool | Text search-and-replace tool optimized towards refactoring code. | Alpha | proto plugin add spacemod [https://raw.githubusercontent.com/malte-behrendt/proto-plugins/main/spacemod/plugin.toml](https://raw.githubusercontent.com/malte-behrendt/proto-plugins/main/spacemod/plugin.toml) |

## Contributing

PRs with new plugins are welcome!

### Non-WASM plugin

1. Create a subfolder with plugin's name
2. Add a `plugin.<toml|json|yaml>` file as outlined in the [official docs](https://moonrepo.dev/docs/proto/non-wasm-plugin)
3. Manually (for now) test it:
   1. `proto plugin add <PLUGIN_NAME> source:./plugin.toml`
   2. `proto list-remote <PLUGIN_NAME>`
   3. `proto install <PLUGIN_NAME> latest`
