# helm

## useful commands

```bash
# List helm releases
helm ls

# Check release history
helm history <release_name>

# List added repositories
helm repo list

# Add helm repository
helm repo add <name> <url> <flags>

# Search charts in repository (This will show only the latest version of each chart)
helm search repo <repo_name>

# Search charts in a repository (This will show all charts available versions)
helm search repo <repo_name> [-l/--versions]

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
```

**Note:** If `--version` is not specified information about the latest version is retrieved.
