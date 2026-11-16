# xmeta 0.6.2

## Improvements

- Make sorted, paged queries faster for large folders. Ordering by supported system columns, such as creation time, name, size and path, now happens before loading custom properties or building attachment values for rows outside the result page.
- Keep exact filtering, ordering and pagination. Custom-property sorts, expressions, alternate collations, non-default NULL placement and non-UTF-8 databases continue to use SQLite's sorter.

Every query still reads the current filesystem. No persistent index or cross-query cache is created, and existing properties and folder schemas require no migration.
