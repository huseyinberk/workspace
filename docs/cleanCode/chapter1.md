# Clean Code · Chapter 1

<p class="note-meta">August 2026</p>

> Code is read far more often than it is written.

## The central idea

Clean code is not merely code that works. It is code that another engineer can understand, change, and verify without unnecessary friction.

A useful baseline:

- Use names that make intent obvious.
- Keep functions small and focused on one responsibility.
- Prefer straightforward control flow over cleverness.
- Remove duplication only when the shared abstraction is truly clearer.
- Leave a file easier to read than you found it.

## A practical test

Before shipping a change, ask:

1. Can a teammate explain the intent without reading every implementation detail?
2. Is the smallest meaningful unit of behaviour easy to test?
3. Would a failure point to a clear place to investigate?

If the answer is no, improve the shape of the code before adding more code.
