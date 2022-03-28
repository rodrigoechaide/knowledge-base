# helm

## useful commands

```bash
# List helm releases
helm ls

# Check release history
helm history <release-name>

# Check added repositories
helm repo list

# Add helm repository
helm repo add <name> <url> <flags>

# Pull and uncompress a chart to have it kicakkt
helm pull <repo_name>/<chart_name> --untar
```
