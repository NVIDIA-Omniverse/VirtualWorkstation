## [12.0.4] - 2020-12-20
### Fixed
- Fix crash introduced in `12.0.3` when processing strikethrough (`~~`) and similar plugins, #742.
- Avoid fenced token mutation, #745.

## [12.0.3] - 2020-12-07
### Changed
- `[](<foo<bar>)` is no longer a valid link.
- `[](url (xxx())` is no longer a valid link.
- `[](url\ xxx)` is no longer a valid link.
- Fix performance issues when parsing links (#732, #734), backticks, (#733, #736),
  emphases (#735), and autolinks (#737).
- Allow newline in `<? ... ?>` in an inline context.
- Allow `<meta>` html tag to appear in an inline context.


## [12.0.2] - 2020-10-23
### Security
- Three pipes (`|\n|\n|`) are no longer rendered as a table with no columns, #724.
