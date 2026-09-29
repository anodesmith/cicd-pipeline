# Day 4 - Continuous Integration / Deployment Pipeline

> Day 4 of 14 in the **Zero to Production Infrastructure & Security** series.

CI/CD pipeline that lints Bash, builds container images, and runs tests on every push.

| | |
|---|---|
| **Day** | 4 of 14 |
| **Status** | Under construction |
| **Verification** | `docker build -t pipeline-selftest:ci .` |
| **Tags** | `ci-cd`  `github-actions`  `docker`  `gitlab-ci`  `automation` |

## Focus

- Workflow trigger design
- Multi-stage Docker builds
- Automated test and lint gates
- Container image layer optimisation

## Status

Implementation lands during the Day 4 build session. Until then this
repository holds the agreed structure only - there is no placeholder code here
pretending to work.

The nightly pipeline appends the real verification result to [STATUS.md](STATUS.md).

## Layout

```
04-cicd-pipeline/
  README.md        this file
  LICENSE          MIT
  STATUS.md        machine-written verification record
  .gitignore       shared from the series root
  .gitattributes   forces LF endings so bash scripts run on Windows
```

## Verify

```bash
docker build -t pipeline-selftest:ci .
```

The nightly job at 22:00 runs this command, records the result and
exit code in STATUS.md, then tags and pushes the repository.

## Licence

MIT. See [LICENSE](LICENSE).