# Component Tests

## 1. Acceptance Criteria

1. Every bug can be reproduced with a component test
1. Every bug has been fixed

## 2. Implementation Details

By component test, we mean a test that tests one component as a whole. In our case we want to test the entire backend
component. We're using the term component test for this because that's what these kinds of tests are often called
in distributed applications. These are also sometimes referred to as "REST API End-to-End tests", (broad) integration tests
or system tests.

What *we*'re looking for in a component test is a test that actually runs a full backend
(`@SpringBootTest(webEnvironment = SpringBootTest.WebEnvironment.RANDOM_PORT)`) and performs real
(non-mocked) HTTP requests. We want to test every layer of our backend, so there's generally no
mocking involved in these kinds of tests.

Just like with database integration tests, you will need to be particularly careful that your tests can run independently
of each other, and that any modifications to the database are rolled back.

[Consult the provided references](../../reference/testing/1%20-%20testing.md) and do
some of your own research and experimentation.
