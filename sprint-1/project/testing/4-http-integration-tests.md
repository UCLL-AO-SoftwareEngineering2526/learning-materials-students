# HTTP integration tests

## 1. Acceptance Criteria

There should be HTTP integration tests (happy and unhappy cases) for at least two endpoints.

## 2. Implementation Details

By HTTP integration tests, we mean tests that only test how API requests are handled by our controllers.
We don't involve the rest of the backend, like the service layer, though, so be sure to mock your service
classes!

[Consult the provided references](../../reference/testing/1%20-%20testing.md) and do
some of your own research and experimentation. Looking into the `@WebMvcTest` annotation
is a good starting point.
