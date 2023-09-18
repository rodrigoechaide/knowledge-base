# sts cheat sheet

```text
# Assume a role with "assume-role" action
aws sts assume-role --role-arn <role-to-assume-arn> --role-session-name <session_name>

# Assume a role with "assume-role-with-web-identity" action
aws sts assume-role-with-web-identity --role-arn <role-to-assume-arn> --role-session-name <session_name> --web-identity-token <location_identity_token_file> --duration <lease_duration_in_seconds>

```
