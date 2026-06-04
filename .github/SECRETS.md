# StudioDrave Org-Level Secrets

These secrets are set at the org level and available to all repos automatically.
Settings → Secrets and variables → Actions → New organization secret.

| Secret | Purpose | Required by |
|---|---|---|
| DOCS_PUSH_TOKEN | Trigger docs site rebuild | notify-docs.yml |
| DOCS_GITHUB_TOKEN | Read private repos during docs fetch | StudioDrave/docs |
| MAVEN_CENTRAL_USERNAME | Publish Android artifacts | drave-ui |
| MAVEN_CENTRAL_PASSWORD | Publish Android artifacts | drave-ui |
| SIGNING_KEY | GPG artifact signing | drave-ui |
| SIGNING_PASSWORD | GPG passphrase | drave-ui |

## DOCS_PUSH_TOKEN scopes
- `actions:write` on StudioDrave/docs (to trigger workflow_dispatch)
- `contents:read` on all source repos (to fetch docs)

## Recommendation
Create a `studiodrave-bot` machine account, add it to the org,
and generate the token from that account rather than a personal account.

## TODO
Add SSO secrets here once work emails and home server are configured.
