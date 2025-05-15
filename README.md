# Proto Plugins

Collection of plugins for the runtime/tool version manager [proto](https://moonrepo.dev/proto).

## Plugins

| Name | Category | Description | Plugin Status | Install |
| ---- | -------- | ----------- | ------------- | ---------- |
| [trivy](https://github.com/aquasecurity/trivy) | SCA/SBOM | Comprehensive and versatile security scanner | Alpha | proto plugin add trivy [https://raw.githubusercontent.com/malte-behrendt/proto-plugins/main/trivy/plugin.toml](https://raw.githubusercontent.com/malte-behrendt/proto-plugins/main/trivy/plugin.toml) |
| [syft](https://github.com/anchore/syft) | SCA/SBOM | Generator for Software Bill of Materials (SBOM) from container images and filesystems | Alpha | proto plugin add syft [https://raw.githubusercontent.com/malte-behrendt/proto-plugins/main/syft/plugin.toml](https://raw.githubusercontent.com/malte-behrendt/proto-plugins/main/syft/plugin.toml) |
| [cyclonedx-cli](https://github.com/CycloneDX/cyclonedx-cli) | SBOM | Tool for SBOM analysis, merging, diffs and format conversions | Alpha | proto plugin add cyclonedx-cli [https://raw.githubusercontent.com/malte-behrendt/proto-plugins/main/cyclonedx-cli/plugin.toml](https://raw.githubusercontent.com/malte-behrendt/proto-plugins/main/cyclonedx-cli/plugin.toml) |
| [ast-grep](https://github.com/ast-grep/ast-grep) | Code Replace | CLI for code structural search, lint and rewriting | Alpha | proto plugin add ast-grep [https://raw.githubusercontent.com/malte-behrendt/proto-plugins/main/ast-grep/plugin.toml](https://raw.githubusercontent.com/malte-behrendt/proto-plugins/main/ast-grep/plugin.toml) |
| [comby](https://github.com/comby-tools/comby) | Code Replace | Code rewrite tool for structural search and replace that supports almost every language. | Alpha | proto plugin add comby [https://raw.githubusercontent.com/malte-behrendt/proto-plugins/main/comby/plugin.toml](https://raw.githubusercontent.com/malte-behrendt/proto-plugins/main/comby/plugin.toml) |
| [grit](https://github.com/getgrit/gritql)  | Code Replace | GritQL is a query language for searching, linting, and modifying code. | Alpha | proto plugin add grit [https://raw.githubusercontent.com/malte-behrendt/proto-plugins/main/grit/plugin.toml](https://raw.githubusercontent.com/malte-behrendt/proto-plugins/main/grit/plugin.toml) |
| [spacemod](https://github.com/untitaker/spacemod)  | Code Replace | Text search-and-replace tool optimized towards refactoring code. | Alpha | proto plugin add spacemod [https://raw.githubusercontent.com/malte-behrendt/proto-plugins/main/spacemod/plugin.toml](https://raw.githubusercontent.com/malte-behrendt/proto-plugins/main/spacemod/plugin.toml) |
| [tf-summarize](https://github.com/dineshba/tf-summarize) | IaC Visualization | A command-line utility to print the summary of the terraform plan | Alpha | proto plugin add tf-summarize [https://raw.githubusercontent.com/malte-behrendt/proto-plugins/main/tf-summarize/plugin.toml](https://raw.githubusercontent.com/malte-behrendt/proto-plugins/main/tf-summarize/plugin.toml) |
| popeye | IaC Linter | Scans live Kubernetes clusters and reports potential issues with deployed resources and configurations | Alpha | proto plugin add popeye [https://raw.githubusercontent.com/malte-behrendt/proto-plugins/main/popeye/plugin.toml](https://raw.githubusercontent.com/malte-behrendt/proto-plugins/main/popeye/plugin.toml) |
| pluto | IaC Linter | Finds Kubernetes resources that have been deprecated | Alpha | proto plugin add pluto [https://raw.githubusercontent.com/malte-behrendt/proto-plugins/main/pluto/plugin.toml](https://raw.githubusercontent.com/malte-behrendt/proto-plugins/main/pluto/plugin.toml) |
| [Helm](https://github.com/helm/helm) | IaC | Package manager for Kubernetes manifests | Alpha | proto plugin add helm [https://raw.githubusercontent.com/malte-behrendt/proto-plugins/main/helm/plugin.toml](https://raw.githubusercontent.com/malte-behrendt/proto-plugins/main/helm/plugin.toml) |
| [just](https://github.com/casey/just) | Task Runner | Cross-platform command runner, allows writing recipes in arbitrary languages | Alpha | proto plugin add just [https://raw.githubusercontent.com/malte-behrendt/proto-plugins/main/just/plugin.toml](https://raw.githubusercontent.com/malte-behrendt/proto-plugins/main/just/plugin.toml) |
| [kubectl](https://github.com/kubernetes/kubectl) | | CLI for Kubernetes | Alpha | proto plugin add kubectl [https://raw.githubusercontent.com/malte-behrendt/proto-plugins/main/kubectl/plugin.toml](https://raw.githubusercontent.com/malte-behrendt/proto-plugins/main/kubectl/plugin.toml) |
| [shellcheck](https://github.com/koalaman/shellcheck) | SCA | Static analysis tool for shell scripts | Alpha | proto plugin add shellcheck [https://raw.githubusercontent.com/malte-behrendt/proto-plugins/main/shellcheck/plugin.toml](https://raw.githubusercontent.com/malte-behrendt/proto-plugins/main/shellcheck/plugin.toml) |
| [shfmt](https://github.com/mvdan/sh) | Formatter | Formats shell programs | Alpha | proto plugin add shfmt [https://raw.githubusercontent.com/malte-behrendt/proto-plugins/main/shfmt/plugin.toml](https://raw.githubusercontent.com/malte-behrendt/proto-plugins/main/shfmt/plugin.toml) |
| [Terraform](https://github.com/hashicorp/terraform) | IaC | Tool for building, changing, and versioning infrastructure | ALpha | proto plugin add terraform [https://raw.githubusercontent.com/malte-behrendt/proto-plugins/main/terraform/plugin.toml](https://raw.githubusercontent.com/malte-behrendt/proto-plugins/main/terraform/plugin.toml) |

## Contributing

PRs with new plugins are welcome!

### Non-WASM plugin

1. Create a subfolder with plugin's name
2. Add a `plugin.<toml|json|yaml>` file as outlined in the [official docs](https://moonrepo.dev/docs/proto/non-wasm-plugin)
3. Manually (for now) test it:
   1. `proto plugin add <PLUGIN_NAME> source:./plugin.toml`
   2. `proto versions <PLUGIN_NAME>`
   3. `proto install <PLUGIN_NAME> latest`
