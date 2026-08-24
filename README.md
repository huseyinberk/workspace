# Workspace

A small, versioned collection of engineering notes, reading takeaways, and technical references. The published documentation lives in the `docs/` directory.

## Current notes

- [Couchbase Magma](docs/couchbase/magma.md) — notes on a storage engine designed for larger, write-heavy workloads.
- [Clean Code · Chapter 1](docs/cleanCode/chapter1.md) — practical takeaways on writing code that is easier to read and change.

## Repository layout

```text
docs/
├── README.md       # documentation home page
├── _sidebar.md     # navigation for the documentation site
├── couchbase/      # data-systems notes
└── cleanCode/      # engineering-practice notes
```

## Adding a note

1. Add a Markdown file under the topic that fits best in `docs/`.
2. Link it from `docs/_sidebar.md` so it is discoverable.
3. Add a short card to `docs/README.md` when the note should appear on the home page.

Keeping notes small, focused, and linked from the sidebar makes the archive useful as it grows.
