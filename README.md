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
    env:
      AWS_ACCESS_KEY_ID: ${{ secrets.AWS_ACCESS_KEY_ID }}
      AWS_SECRET_ACCESS_KEY: ${{ secrets.AWS_SECRET_ACCESS_KEY }}
      AWS_DEFAULT_REGION: us-east-1
      SLACK_WEBHOOK_URL: ${{ secrets.SLACK_WEBHOOK_URL }}
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v2
      - uses: freckle/platform-deploy-action@main
```

## Environment

- `AWS_*`: AWS configuration for the target account
- `SLACK_WEBHOOK_URL`: where to notify of deployment outcome

## Inputs

See `action.yml`.

---

[LICENSE](./LICENSE)
