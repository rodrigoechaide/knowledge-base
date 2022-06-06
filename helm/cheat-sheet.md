# helm cheat sheet

```text
# List helm releases
helm ls

# Check release history
helm history <release_name>

# List added repositories
helm repo list

# Add helm repository
helm repo add <name> <url> <flags>

# Add a private helm repository
helm repo add <name> <url> --username <username> --password <password>

# Search charts in repository (This will show only the latest version of each chart)
helm search repo <repo_name>

# Search charts in repository (This will show all the versions of all available charts in the repository)
helm search repo <repo_name> [-l/--versions]

# Search a chart in all existing repositories (This will show only the latest version of each chart)
helm search repo [<chart_name>/<keyword>]

# Search a chart in all existing repositories (This will show all charts available versions)
helm search repo [<chart_name>/<keyword>] [-l/--versions]

# Show chart definition
helm show chart <repo_name>/<chart_name> --version <chart_version>

# Show chart readme
helm show readme <repo_name>/<chart_name> --version <chart_version>

# Show the chart values
helm show values <repo_name>/<chart_name> --version <chart_version>

# Show the chart crds
helm show crds <repo_name>/<chart_name> --version <chart_version>

# Show all chart information
helm show all <repo_name>/<chart_name> --version <chart_version>

# Pull and uncompress a chart to have it locally
helm pull <repo_name>/<chart_name> --untar --version <chart_version>

# Get k8s manifest of a helm release
helm get manifest <release_name>

# Update helm dependencies
helm dependency update <chart-path>

# Make a template of a chart with custom values
helm template <chart-path> -f <values-path-1> -f <values-path-2> -f <values-path-n> > result.yaml

# Run installation with debug and dry-run flags (This will output the rendered templates)
helm install --debug --dry-run <release-name> <chart-path>
```

**Note:** If `--version` is not specified information about the latest version is retrieved.
