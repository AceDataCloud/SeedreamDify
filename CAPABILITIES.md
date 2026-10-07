# Seedream capability mapping

Compared with [MCPs at f0eed10abf31](https://github.com/AceDataCloud/MCPs/tree/f0eed10abf310824cb4c33d4944c63d3654ac95b/seedream) and the public API contract at PlatformBackend `fa94598267a82545fb1afed6ee26bafd6cbb9ca7`.

The table maps service operations to Dify tools. Different MCP helper functions may use the same action selector or structured JSON input.

| MCP function | Dify equivalent | Notes |
|---|---|---|
| `seedream_list_models` |  | Model/action selectors and the API reference; informational guidance does not submit a request. |
| `seedream_list_sizes` |  | Model/action selectors and the API reference; informational guidance does not submit a request. |
| `seedream_get_task` | `seedream_task_retrieve` | Set action=retrieve |
| `seedream_get_tasks_batch` | `seedream_tasks_retrieve_batch` | Set action=retrieve_batch |
| `seedream_generate_image` | `seedream_generate_image` |  |
| `seedream_edit_image` | `seedream_edit_image` |  |
| `seedream_decompose_image` | `seedream_decompose_image` |  |

## Parameter equivalents

- `seedream_get_tasks_batch`: `task_ids` → ids.
- `seedream_generate_image`: `response_format` → URL output for Dify media.
- `seedream_edit_image`: `response_format` → URL output for Dify media.

## Verification boundary

Contract examples and regression tests cover request validation, transport and task handling. Actual Dify browser cases are recorded separately in `tests/e2e-results.json` and `tests/e2e-audit.json` when available. A schema test is not a successful paid generation. Unsupported service availability and untested advanced combinations must not be described as passed.
