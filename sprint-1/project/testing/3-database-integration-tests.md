# Database integration tests

Some repository classes have more complex queries that may require some testing to
verify that they're working correctly.

In our database integration tests we only want to specifically check how
our backend interacts with the database, preferably testing only one specific
query.

## 1. Acceptance Criteria

There should be tests (happy and unhappy cases) for every non-trivial query in
`ScheduleRepository`. The non-trivial queries are those methods that are explicitly
specified in the interface.

## 2. Implementation Details

[Consult the provided references](../../reference/testing/1%20-%20testing.md) and do
some of your own research and experimentation. Looking into the `@DataJpaTest` annotation
is a good starting point.

Make sure your database integration tests can run independently of each other!
