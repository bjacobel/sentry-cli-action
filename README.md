### **ARCHIVED.** Use [the official Sentry action](https://blog.sentry.io/2020/07/30/automate-release-management-with-the-sentry-release-github-action/) instead.

# sentry-cli action
Uses the [Docker image published by Sentry](https://hub.docker.com/r/getsentry/sentry-cli) to run `@sentry/cli` commands without any brew, node, etc dependencies.

## Inputs

### `args`

The command string you would pass to sentry-cli if it was installed locally

## Example usage

```yaml
uses: bjacobel/sentry-cli-action@master
with:
  args: releases -o SentryOrgName -p SentryProjectName new ${{ github.sha }}
env:
  SENTRY_AUTH_TOKEN: ${{ secrets.SENTRY_AUTH_TOKEN }}
```
