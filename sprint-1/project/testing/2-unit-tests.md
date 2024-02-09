# Unit tests

Unit tests focus on verifying the behavior of a **single, isolated piece of code**,
usually a function or method. Unit tests are supposed to be small and fast, only
testing the specific thing you want to test. Mocking can help make sure you're
only testing the unit that's undergoing testing.

## 1. Acceptance Criteria

1. Every bug can be reproduced with a unit test that isolates the buggy unit.
1. Every bug has been fixed

## 2. Implementation Details

Check the demo posted on Toledo and compare it with the behavior of your backend to uncover the bugs.

The bugs can all be found in the `ScheduleService` class, so you should have one test class that
isolates only the `ScheduleService` and doesn't rely on any other backend code.

Be sure to [consult our references](../../reference/testing/1%20-%20testing.md)!
