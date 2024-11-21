# Proto Plugins

Collection of plugins for the runtime/tool version manager [proto](https://moonrepo.dev/proto).

## Plugins

| Name | Category | Description | Plugin Status | Install |
| ---- | -------- | ----------- | ------------- | ---------- |
| [trivy](https://github.com/aquasecurity/trivy) | tool | Comprehensive and versatile security scanner | Alpha | proto plugin add trivy [https://raw.githubusercontent.com/malte-behrendt/proto-plugins/main/trivy/plugin.toml](https://raw.githubusercontent.com/malte-behrendt/proto-plugins/main/trivy/plugin.toml) |

## Contributing

PRs with new plugins are welcome!

### Non-WASM plugin

1. Create a subfolder with plugin's name
2. Add a `plugin.<toml|json|yaml>` file as outlined in the [official docs](https://moonrepo.dev/docs/proto/non-wasm-plugin)
3. Manually (for now) test it:
   1. `proto plugin add <PLUGIN_NAME> source:./plugin.toml`
   2. `proto list-remote <PLUGIN_NAME>`
   3. `proto install trivy latest`