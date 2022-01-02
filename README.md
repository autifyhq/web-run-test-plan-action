[integration-test-badge]: https://github.com/autifyhq/web-run-test-plan-action/actions/workflows/integration-test.yml/badge.svg
[integration-test-url]: https://github.com/autifyhq/web-run-test-plan-action/actions/workflows/integration-test.yml

[release-badge]: https://img.shields.io/github/v/release/autifyhq/web-run-test-plan-action.svg
[release-url]: https://github.com/autifyhq/web-run-test-plan-action/releases

[release-date-badge]: https://img.shields.io/github/release-date/autifyhq/web-run-test-plan-action.svg
[release-date-url]: https://github.com/autifyhq/web-run-test-plan-action/releases

[license-badge]: https://img.shields.io/badge/license-MIT-lightgrey.svg
[license-url]: https://raw.githubusercontent.com/autifyhq/web-run-test-plan-action/main/LICENSE

# Autify for Web Run Test Plan Action

[![Test][integration-test-badge]][integration-test-url]
[![Release][release-badge]][release-url]
[![Release date][release-date-badge]][release-date-url]
[![License][license-badge]][license-url]

## Inputs

| PARAMETER | DESCRIPTION | REQUIRED | DEFAULT | TYPE |
| --- | --- | --- | --- | --- |
| **autify_for_web_api_token** | Autify for Web API Token | Yes | - | string |
| **test_plan_id** | Test Plan ID that you want to run | Yes | - | string |
| **test_plan_api_base_url** | Test Plan API base URL | No | 'https://app.autify.com/api/v1/schedules/' | string |

## Outputs

| Name | Description |
| --- | --- |
| **response** | API response json |

## Usage Examples

> Runs a Test Plan on Autify for Web.

```yaml
name: "example"
on: [push]
jobs:
  test:
    runs-on: ubuntu-latest
    steps:
      - name: Funtional test
        id: functional-test
        uses: autifyhq/web-run-test-plan-action@v1.0.0
        with:
          autify_for_web_api_token: ${{ secrets.AUTIFY_FOR_WEB_API_TOKEN }}
          test_plan_id: ${{ secrets.TEST_PLAN_ID }}
```
