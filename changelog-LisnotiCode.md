# Changelog for Lisnoti Code

<img src="images/lisnoti-code-card.svg" alt="Lisnoti Code font card" align="right" width="210">

> [!NOTE]
> The glyphs in this changelog are shown in the *local display font*, which
> means that *they may not look like the actual Lisnoti Code version*.

## [0.902] - 2026-09-29

### Changed

- Inherited from the [Lisnoti 2.004 update](changelog-Lisnoti.md#2004---2026-09-29):
    - Taller brackets and symmetric bracket pairs.
    - Narrower `|`.
    - No longer declares support for East Asian characters, which fixes Word's line spacing but also means that Word shows Lisnoti Code's full-width, half-width and East Asian characters `｛ ｝￩￪￫￬〒〰円圓` in another font.
- More space round the thin punctuation `. , ; : ! ·`, the brackets `( ) [ ] { }` and the slashes `/ \`, 40&#xA0;units each side, so that a `;` or `:` is easy to spot and `a[i]` or `a/b` does not crowd.
- More room outside brackets for readability.
- Shorter `^` to be more consistent with most coding fonts.

## [0.901] - 2026-09-25

The first release of Lisnoti Code as a font family of its own. It is built from Lisnoti&#xA0;2.003 and replaces 'Lisnoti Code WS'. (Version 0.900 was a trial used only on [naxp.org](https://naxp.org) and was not released here.)

### Added

- Spaces that tell words from indentation, as a contextual alternate (`calt`). A space between two words keeps Lisnoti's own width, and a space in a run of spaces, or next to a box-drawing character, is 500&#xA0;units wide (an en space). With `calt` off, every space is 380&#xA0;units, between the two.
- Box-drawing characters as wide as the spaces beside them, so the output of `tree` and similar tools lines up.
- A hyphen drawn as a minus, because in code it usually is one. Between two letters, digits or underscores, as in `max-width` or `n-1`, it is shorter (`calt`).
- Standard ligatures (`liga`) for `==` `===` `!=` `!==`, `<=` `>=`, `->` `<-` `=>`, and Julia's pipes `|>` `<|` and their multi-bar forms. A ligature is used only when the whole run of operator characters matches it, so `<==` and `-->` stay as they are.
- Stylistic sets for choosing features one group at a time: `ss02` the short hyphen, `ss03` the equality ligatures, `ss04` the relation ligatures and `ss05` the arrow and pipe ligatures. `ss01` remains Lisnoti's chancery script capitals.
- Web fonts in the same two forms as Lisnoti: split into subsets with `lisnoti-code.css`, and one file per style with `lisnoti-code-monolithic.css`. The stylesheets switch `calt` off in WebKit (Safari, and every browser on an iPhone or iPad), which lays out the narrow and wide spaces at one width and draws them at another.

### Changed

- Everything else comes from Lisnoti&#xA0;2.003 rather than Lisnoti&#xA0;1.002: the character set, the drawings and the kerning. See the [Lisnoti changelog](changelog-Lisnoti.md).

### Removed

- The OpenType `MATH` table, and the glyphs only that table used. Use Lisnoti for equations.

### Deprecated

- 'Lisnoti Code WS' is superseded by Lisnoti Code. It stays in `font-LisnotiCodeWS (deprecated)/` for now.

## [Lisnoti Code WS] - 2024 to 2025

'Lisnoti Code WS' was an experimental variant of Lisnoti&#xA0;1.002 whose space was 40% wider, so that indentation stood out. It had no version number of its own.

- Added in July 2024.
- Withdrawn in May 2025.
- Restored in July 2025, with the updated arrows of Lisnoti&#xA0;1.002's last re-release.
