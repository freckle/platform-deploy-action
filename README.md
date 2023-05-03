**Archived**: users should move to PlatformCLI v3 and
`setup-platform-action@v7`, then just call `platform deploy`.

# Platform Deploy Action

GitHub Action to deploy using the [Freckle Platform CLI][platform].

[platform]: https://github.com/freckle/platform

**NOTE**: This action is public so that we can use it outside of its own
repository, but the tooling it installs and uses is private. It is of no use
outside Freckle.

## Usage

```yaml
jobs:
  image:
    runs-on: ubuntu-latest
    steps:
      - uses: aws-actions/configure-aws-credentials@v1
        with:
          # ...
      - uses: actions/checkout@v2
      - uses: freckle/platform-deploy-action@v4
        with:
          slack-webhook: ${{ secrets.SLACK_WEBHOOK_URL }}
```

## Environment

None.

## Inputs

See `action.yml`.

---

[LICENSE](./LICENSE)
