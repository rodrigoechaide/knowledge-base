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

# Search charts in an added repository
helm search repo <repo_name>

# Show chart definition
helm show chart <chart_name> --version <chart_version>

# Show chart readme
helm show readme <chart_name> --version <chart_version>

# Show the chart values
helm show values <chart_name> --version <chart_version>

# Show the chart crds
helm show crds <chart_name> --version <chart_version>

# Show all chart information
helm show all <chart_name> --version <chart_version>

# Pull and uncompress a chart to have it locally
helm pull <chart_name> --untar --version <chart_version>
```

**Note:** If `--version` is not specified information about the latest version is retrieved.
