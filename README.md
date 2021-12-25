# web-run-test-plan-action

[![GitHub License](https://img.shields.io/badge/license-MIT-lightgrey.svg)](https://raw.githubusercontent.com/autifyhq/web-run-test-plan-action/main/LICENSE)

## Inputs

| PARAMETER | DESCRIPTION | REQUIRED | DEFAULT | TYPE |
| --- | --- | --- | --- | --- |
| **autify_for_web_api_token** | Autify for Web API Token
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
        uses: autifyhq/web-run-test-plan-action@main
        with:
          autify_for_web_api_token: ${{ secrets.AUTIFY_FOR_WEB_API_TOKEN }}
          test_plan_id: ${{ secrets.TEST_PLAN_ID }}
```