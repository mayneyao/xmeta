# xmeta 0.6.3

## Fixes

- Return SQL `NULL` in the `extension` column for directories and files without a suffix, so `extension IS NULL` finds both when filtering a folder table.
- Preserve SQLite's NULL ordering for sorted and paginated results.

Queries that matched an empty extension with `extension = ''` should use `extension IS NULL`. Existing properties and folder schemas require no migration.
