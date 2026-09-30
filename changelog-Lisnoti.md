# Changelog for Lisnoti

<img src="images/lisnoti-card.svg" alt="Lisnoti font card" align="right" width="210">

> [!NOTE]
> The glyphs in this changelog are shown in the *local display font*, which
> means that *they may not look like the actual Lisnoti version*.



## [2.004] - 2026-09-29

### Changed

- The brackets `( ) [ ] { }` are now taken from Noto Sans Math, which increases their height to just above the ascenders of `b d f h k l` (instead of stopping at the height of the capitals). The drawings are Noto Sans Math's and now match other brackets in the font, e.g. `⟨ ⌈ ⌊ ⟦`. This also updates `⸨ ⸩ ⹕ ⹖ ⹗ ⹘` because these are built from `( ) [ ]`.
- The vertical line `|` now uses Noto Sans Math's narrower width.
- Lisnoti 2.001 to 2.003 declared East Asian support so that Microsoft Word would show the few full-width, half-width and East Asian characters in Lisnoti (`｛｝￩￪￫￬〒〰円圓`). But this caused line spacing and other issues in Word, and so has been reverted, which means Word will display those characters in another font. Most applications, including VS Code, Visual Studio and browsers, are unaffected and will still show these characters in Lisnoti.

### Fixed

- In Microsoft Word, line spacing is now correct and a separate '@Lisnoti' font is no longer listed in font menus. (See above change note in relation to East Asian support.)
- Equations rendered on web pages now show subscripts at one consistent height. Previously letters with descenders had lower subscripts, e.g. the `0` in `μ₀` sat below the one in `ε₀`. In LuaLaTeX, subscripts on single letters are unchanged, and a subscript on a tall bracketed expression such as `(a/b)₀` now sits a little higher, beside the bracket rather than below it.
- Every closing bracket is now the mirror image of its opening bracket, including the larger sizes used in equations. Previously `⁅ ⁆`, `⸨ ⸩`, `⹕ ⹖` and `⹗ ⹘`, the large sizes of `{ }`, and in bold `⸦ ⸧` and the pieces of very large round brackets, differed slightly between left and right.

## [2.003] - 2026-09-25

### Fixed

- Equations on web pages using `lisnoti.css` (the version of the web font split into subsets) now get large operators and stretchy brackets. Previously `⋃ ⋂ ∐ ⋀ ⋁ ⨀ ⨁ ⨂ ⨄ ⨆ ⅀ ∬ ∭ ∮` stayed at text size in display equations, and `⟨ ⟩ ⌈ ⌉ ⌊ ⌋ ⟦ ⟧ ⟪ ⟫` did not stretch around a fraction. The fix adds these characters, the horizontal brackets `⎴ ⎵ ⏜ ⏝ ⏞ ⏟` and seven stretchy accents to the Latin subset, which is the file a browser takes stretching information from. The monolithic version (`lisnoti-monolithic.css`) was never affected.
- Stray points left along straight edges when the bold faces were made have been removed. They could not be seen, but they could confuse software that looks for corners. The bold `>` and 68 other bold relations such as `≥ ≫ ⪈` were among those affected. The regular and italic faces had a few as well.

### Changed

- The stylesheet for the monolithic web fonts is renamed `lisnoti-monolithic.css` (previously `lisnoti-full.css`) to match its folder, `Lisnoti-woff2-monolithic`. lisnoti.com serves it under both names, so existing links keep working.

## [2.002] - 2026-09-25

### Changed

- The subset sign `⊂` and its relatives (41 glyphs, including `⊃ ⊆ ⊇ ⊄ ⊊ ⋐ ⟃ ⪽ ⪿ ⫅ ⫋ ⫏ ⫓`) have been redrawn as straight arms joined by a semicircle. Previously the arms started to curve well before the end, because the shape was a squashed version of a rounder one.
    - `⟈ ⟉` were larger than `⊂` and now match it.
    - In bold, the two cups of `⋐ ⋑` keep the same space between them as in regular.
    - The dot in `⪽ ⪾` and the ring in `⟃ ⟄` are no longer squashed.
- In bold and bold italic, the 23 miscellaneous symbols `⌂ ☸ ♀ ♂ ♩ ♪ ♫ ♬ ♭ ♮ ♯ ⚢ ⚣ ⚤ ⚥ ⚦ ⚧ ⚨ ⚩ ⚭ ⚮ ⚯ ⚲` now come from Noto Sans Symbols Bold instead of being thickened artificially from the regular. They match the weight of bold text better and keep their parts distinct. (The Noto `⚢` glyph was faulty and had to be repaired.)

### Fixed

Windows listed the bold italic style as 'Bold Bold Italic' (for example in Notepad). It is now 'Bold Italic'.

## [2.001] - 2026-09-24

### Fixed

Corrected the vertical alignment of `∞ ⧜ ⫙ ⟒` and the colon component of the `≔ ≕ ⩴` glyphs to match the maths axis (same as `=`).

The proportional to symbol, `∝`, was redrawn (based on the Noto Sans Math symbol), partly to help distinguish it from the Greek alpha `α`.

Although Lisnoti contained the full-width, half-width and East Asian characters `｛ ｝￩￪￫￬〒〰円圓`, they were not displayed by Microsoft Word because it categorises them all as East Asian and will only use fonts that declare they support this in the OS/2 field `ulCodePageRange`. The relevant bits have been turned on[^codepage] for Lisnoti&#xA0;2.001 and Word now displays them in Lisnoti. (Reversed in [2.004](#2004---2026-09-29), because the declaration also made Word space lines too widely.)

[^codepage]: Technically the bits declare Korean support, which Lisnoti does not have. Word and other programs will still fall back to another font for any character Lisnoti lacks, so the only effect is that Word will now use Lisnoti for the characters it does have. (JuliaMono does the same.)

> [!TIP]
> If Word does not offer 'Lisnoti' as an equation font after upgrading from v1, close all Office programs and run this in a command prompt:
>
> ```
> reg delete "HKCU\Software\Microsoft\Office\16.0\Common\MathFonts" /v Lisnoti /f
> ```

## [2.000] - 2026-09-21

Lisnoti&#xA0;2.000 is a complete rebuild of the font:

### Changed

- The base is [Noto Sans](https://fonts.google.com/noto/specimen/Noto+Sans)&#xA0;v2.015 (previously v2.013).

- The maths donor is [Noto Sans Math](https://fonts.google.com/noto/specimen/Noto+Sans+Math)&#xA0;v3.000, Khaled Hosny's 2024 redesign:
    - This shifted the maths vertical alignment axis and redrew and added many glyphs.
    - Notwithstanding Noto's redesign, Lisnoti has itself redrawn the *n*-ary operators, radical sign, tick and cross family and a few other glyphs for consistency and aesthetics.
    - Lisnoti now incorporates an OpenType `MATH` table, built using the same pattern as Noto Sans Math but with Lisnoti glyph measurements. This means that **Lisnoti can now be used to typeset equations**.
- The web font files are now subset by script to optimise web page access. For instance, a Latin-only page downloads about 27&#xA0;KB per weight for Lisnoti&#xA0;2.000, against 350&#xA0;KB for the whole font previously, i.e. a reduction in download size of over 90%. (The previous monolithic approach is still available if required.)


### Added

- Three currency symbols were added, the last of which completes Lisnoti's coverage of the Unicode currency block, U+20A0 to U+20C1:
    - `৳` (U+09F3) Bangladeshi taka / Bengali rupee sign (from Noto Sans Bengali).
    - `฿` (U+0E3F) Thai baht sign (from Noto Sans Thai).
    - `⃁` (U+20C1) Saudi riyal sign (drawn from the Saudi Central Bank's published artwork).

### Removed

- WOFF ('WOFF&#xA0;1') files are no longer included on the basis that every browser now in use supports WOFF2.

## [1.001 to 1.002] - 2023 to 2025

The original Lisnoti, built by hand in [FontForge](https://fontforge.org/) from
[Noto Sans](https://fonts.google.com/noto/specimen/Noto+Sans) and four of its siblings.
v1.001 was first released in this repository in September 2023 and v1.002 was first released in January 2024 and then re-released four more times up to July 2025 under the same version number[^version-bumping].

[^version-bumping]: Using the same version for different releases of Lisnoti v1 was an oversight. In future, new releases will have higher version numbers.

These initial releases included the following core features of Lisnoti:

- **Clear visual distinction between easily confused characters.**
    - A tail was added to lower case `l` to distinguish it from upper case `I`.
    - A dot was added to the interior of zero `0` to distinguish it from upper case `O`.
    - Lower case alpha `α` was replaced with Noto Sans JP's, because Noto Sans's is too close to a roman `a` in italic.
    
    These changes were propagated e.g. to the `ﬂ` and `ﬄ` ligatures and accented forms. 

- **Real minus sign.** Noto Sans's italics have no minus sign `−` (U+2212) of their own (they use the hyphen!). Lisnoti provides true minus signs for all styles.

- **Consistent sub and superscripts.** Noto Sans's sub and superscripts are out of alignment with each other,
  so the roman ones were rebuilt from the full-size letters. Later Lisnoti versions added subscripts `w`, `y` and `z` due in Unicode&#xA0;18.0.

- **Maths symbol consistency.** The *n*-ary `⋀ ⋁ ⋂ ⋃` were redrawn based on `∏` to be visually distinct from their binary partners. `∩` and `∪` were made shorter for aesthetic reasons (and to match logical operators). Noto Sans Math's arrows were scaled up by 25%, because they were too small next to the other operators. `∝` and `∞` were enlarged and reshaped by hand.

- **Kerning for code.** `r`/`n` were separated so as not to be read as `m`. The aggressive Noto Sans `r`/`.` pair kerning was halved so that a full stop in `other.value` stays visible. Brackets of the same orientation were spaced apart. Combinations of `'` and `"` were separated so that `''` does not read as `"`.

- **Incorporate additional symbols.** In order to reduce risk of random font substitution, Lisnoti incorporated a selection of shapes, arrows, chess, ticks and box drawings from
  [Noto Sans Symbols](https://fonts.google.com/noto/specimen/Noto+Sans+Symbols),
  [Noto Sans Symbols 2](https://fonts.google.com/noto/specimen/Noto+Sans+Symbols+2) and
  [Noto Sans JP](https://fonts.google.com/noto/specimen/Noto+Sans+JP). Where no bold existed, it was created using emboldening.

