# Proto Plugins

Collection of plugins for the runtime/tool version manager [proto](https://moonrepo.dev/proto).

## Plugins

| Name | Category | Description | Plugin Status | Install |
| ---- | -------- | ----------- | ------------- | ---------- |
| [trivy](https://github.com/aquasecurity/trivy) | tool | Comprehensive and versatile security scanner | Alpha | proto plugin add trivy [https://raw.githubusercontent.com/malte-behrendt/proto-plugins/main/trivy/plugin.toml](https://raw.githubusercontent.com/malte-behrendt/proto-plugins/main/trivy/plugin.toml) |
| [syft](https://github.com/anchore/syft) | tool | Generator for Software Bill of Materials (SBOM) from container images and filesystems | Alpha | proto plugin add syft [https://raw.githubusercontent.com/malte-behrendt/proto-plugins/main/syft/plugin.toml](https://raw.githubusercontent.com/malte-behrendt/proto-plugins/main/syft/plugin.toml) |
| [cyclonedx-cli](https://github.com/CycloneDX/cyclonedx-cli) | tool | Tool for SBOM analysis, merging, diffs and format conversions | Alpha | proto plugin add cyclonedx-cli [https://raw.githubusercontent.com/malte-behrendt/proto-plugins/main/cyclonedx-cli/plugin.toml](https://raw.githubusercontent.com/malte-behrendt/proto-plugins/main/cyclonedx-cli/plugin.toml) |

## Contributing

PRs with new plugins are welcome!

### Non-WASM plugin

1. Create a subfolder with plugin's name
2. Add a `plugin.<toml|json|yaml>` file as outlined in the [official docs](https://moonrepo.dev/docs/proto/non-wasm-plugin)
3. Manually (for now) test it:
   1. `proto plugin add <PLUGIN_NAME> source:./plugin.toml`
   2. `proto list-remote <PLUGIN_NAME>`
   3. `proto install <PLUGIN_NAME> latest`
