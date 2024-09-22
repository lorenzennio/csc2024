# Tools and Techniques

- A larger project may need a different approach
- “If you only have a screwdriver, nails are pretty useless” - Don Briggs

## Testing

- Each function -> test
- Alternating between writing tests and code keeps the work incremental
- What makes a good test?
  - Best to test functionality that you understand, but can imagine failing
- How big should a test be?
  - A unit test is a unit of failure
  - Make lots of small tests to check what still works

## Memory

- Read/write incorrectly
- Memory management mistakes
  - Deallocation of (currently) unowned memory
    - Freeing something twice results in later overwrites
  - Memory leaks
    - Forgetting to free something results in unusable memory
- A leak is a mistake of omission, not commission
- Memory tools: Validity tests / Leak checkers
- Isolate your own code for initial checks

## Version control

- Which commit broke it? `git bisect`
- `squash` and `rebase` (squashing info kept in reflog)
- Merging PRs:
  - Merge commit
  - **Squash and merge**
  - **Rebase**
- Integrate early and often!