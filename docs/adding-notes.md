# Adding notes

This workspace is intentionally simple: every published note is a Markdown file under `docs/`.

## Add a new note

1. Create a topic directory when one does not already exist.
2. Add a focused `.md` file inside that directory.
3. Use a clear title and lead with the main takeaway.
4. Link the new note in `_sidebar.md`.
5. Add a card to `README.md` when it should appear on the home page.

## Keep notes useful

- Prefer one question or concept per note.
- Use headings to make scanning easy.
- Link to primary sources when a claim depends on an external fact.
- Revisit the note when the underlying technology or recommendation changes.

## Publish a release

When a batch of changes is ready, update `version.json` and add a matching entry to the [changelog](changelog.md).
