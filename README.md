# gha-php-cpd

## Description
Run PHP copy/paste detector with custom PHP image.

## Inputs
| Key                   | Required | Default                       | Description                                                                                    |
|-----------------------|----------|-------------------------------|------------------------------------------------------------------------------------------------|
| **php-image**         | **true** | `''`                          | PHP image to use (fully qualified image address. ex: quay.io/adoreme/nginx-fpm-alpine:v0.0.1). |
| **report-path**       | **true** | `./build/reports/php-cpd.xml` | Report file path (where copy/paste detector results will be saved).                            |

## Outputs
**N/A**

## Notes
ℹ This action doesn't handle docker registry authentication (e.g. for private images).
You can run [docker/login-action@v1](https://github.com/docker/login-action) before this step.

ℹ It uses [pcpd-github-action](https://github.com/adore-me/pcpd-github-action) for publishing **CPD** results.

### Example of step configuration and usage:

```yaml
steps:
  - name: 'Run CPD'
    uses: adore-me/gha-php-cpd@master
```
