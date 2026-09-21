# READ ME

*This repo contains the Lisnoti font files.*

Lisnoti (/lɪzˈnəʊtiː/) is a proportional sans serif font designed for general use
but with consideration also given to making it work

- in maths, science and actuarial contexts, and
- for writing computer code.

Lisnoti is available in regular, italic, bold and bold-italic variants in OpenType (`.ttf`) and web (`.woff2`) formats under the [SIL Open Font Licence (OFL)](https://openfontlicense.org/). The current release is **version 2.000** (September 2026).

If you're interested in why Lisnoti exists, please see [this article](https://timgord.com/2024-01/lisnoti-a-proportional-font-that-works-for-coding-too/).

![Lisnoti font card](LisnotiCard.svg)

## Installing Lisnoti

If you want to install Lisnoti on machines for local use then the OpenType font files are zipped [here](https://github.com/Lisnoti/Lisnoti/raw/refs/heads/main/Lisnoti-OpenType.zip).

If you want to use Lisnoti for your website then [this page sets out how to do this](https://lisnoti.com/index.html#using-lisnoti-for-websites). The `web/` folder holds the font cut into slices by script and use (Latin, Greek, Cyrillic, maths, symbols and so on) with a stylesheet, `lisnoti.css`, that loads only the slices a page needs; the whole-font `.woff2` files are there for anyone who prefers one file per style. All of it is in `Lisnoti.zip`.

There is also an older variant, 'Lisnoti Code WS', in which the space character is 40% wider. It is built from Lisnoti 1.002 and will be replaced by a proper coding family, Lisnoti Code, which is in preparation. Its files are still [here](https://github.com/Lisnoti/Lisnoti/raw/refs/heads/main/LisnotiCodeWS-OpenType.zip) in the meantime.

## Feedback

If you have comments on Lisnoti, please use [the GitHub repo discussions page](https://github.com/Lisnoti/Lisnoti/discussions).

Please bear in mind that I am not a typography expert, just a frustrated user.

## Key features

> ![NOTE]
> The symbol lines below are pictures, set in Lisnoti, since GitHub renders this readme in its own font. The same characters are set live at [lisnoti.com](https://lisnoti.com/index.html#key-features).

Lisnoti is derived from [Noto's sans serif fonts](https://fonts.google.com/noto/), but with the following adaptions:

1. Reliable distinction of upper case `I`, lower case `l` and one `1`, and of upper case `O` and zero `0`, in every style:

    <picture><source media="(prefers-color-scheme: dark)" srcset="images/distinct-dark.svg"><img alt="Il1 O0 in regular, italic, bold and bold italic" src="images/distinct.svg" height="21"></picture>

1. Consistent arithmetic, comparison, logic, set, *n*-ary and other maths operators, all sitting on one maths axis, e.g.

    - arithmetic (*NB Noto Sans gets the minus sign wrong*):<br><picture><source media="(prefers-color-scheme: dark)" srcset="images/ops-arithmetic-dark.svg"><img alt="− × ÷ ± ∓ ∞" src="images/ops-arithmetic.svg" height="21"></picture>
    - comparison:<br><picture><source media="(prefers-color-scheme: dark)" srcset="images/ops-comparison-dark.svg"><img alt="≤ ≠ ≥ ≈ ≡ ≢ ∝" src="images/ops-comparison.svg" height="21"></picture>
    - logic:<br><picture><source media="(prefers-color-scheme: dark)" srcset="images/ops-logic-dark.svg"><img alt="¬ ∧ ∨ ⊻ ⊤ ⊥ ⊦" src="images/ops-logic.svg" height="21"></picture>
    - set:<br><picture><source media="(prefers-color-scheme: dark)" srcset="images/ops-set-dark.svg"><img alt="∩ ∪ ∈ ∉ ⊂ ⊃ ⊆ ⊇ ∅" src="images/ops-set.svg" height="21"></picture>
    - *n*-ary:<br><picture><source media="(prefers-color-scheme: dark)" srcset="images/ops-nary-dark.svg"><img alt="∑ ∏ ∐ ⋀ ⋁ ⋂ ⋃ ⨀ ⨁ ⨂" src="images/ops-nary.svg" height="21"></picture>
    - other:<br><picture><source media="(prefers-color-scheme: dark)" srcset="images/ops-other-dark.svg"><img alt="∫ ∂ √ Δ ∇ ∀ ∃" src="images/ops-other.svg" height="21"></picture>

1. An OpenType `MATH` table, so Lisnoti can be chosen as the equation font in Word and loaded by `unicode-math` in LuaLaTeX: fractions, radicals, big operators with limits, stretchy brackets and accents are all set from the font's own data.

1. Greek and Cyrillic letters -- maths and logic make frequent use of Greek letters and occasionally Cyrillic ones too.

1. Consistently formatted digit and -- if available -- Roman letter sub and superscripts (with kerning):

    <picture><source media="(prefers-color-scheme: dark)" srcset="images/scripts-example-dark.svg"><img alt="x² + y² = r², f⁽ⁿ⁾(x), aᵢⱼ, H₂O, xₙ₊₁" src="images/scripts-example.svg" height="21"></picture>

    - superscript:<br><picture><source media="(prefers-color-scheme: dark)" srcset="images/superscript-dark.svg"><img alt="x⁰¹²³⁴⁵⁶⁷⁸⁹⁽⁾⁺⁻ᵃᵇᶜᵈᵉᶠᵍʰⁱʲᵏˡᵐⁿᵒᵖ𐞥ʳˢᵗᵘᵛʷˣʸᶻᴬᴮꟲᴰᴱꟳᴳᴴᴵᴶᴷᴸᴹᴺᴼᴾꟴᴿᵀᵁⱽᵂx" src="images/superscript.svg" height="21"></picture>
    - subscript:<br><picture><source media="(prefers-color-scheme: dark)" srcset="images/subscript-dark.svg"><img alt="x₀₁₂₃₄₅₆₇₈₉₍₎₊₋ₐₑₕᵢⱼₖₗₘₙₒₚᵣₛₜᵤᵥ₝ₓ₞₟x" src="images/subscript.svg" height="21"></picture>

1. A reasonable selection of symbols, including

    - squares, diamonds, rectangles, triangles, circles and stars:<br><picture><source media="(prefers-color-scheme: dark)" srcset="images/shapes-dark.svg"><img alt="■□▪▫▬▭▮▯▰▱▲△▴▵▶▷▸▹►▻▼▽▾▿◀◁◂◃◄◅◆◇◊○◌●◦◯◻◼◽◾⚪⚫⚬★☆" src="images/shapes.svg" height="21"></picture>
    - lots of arrows:<br><picture><source media="(prefers-color-scheme: dark)" srcset="images/arrows-dark.svg"><img alt="←↑→↓↔↕ ↖↗↘↙ ⇄ ⇅ ⇵ ⇆ ⇋⇌ ⇐ ⇒⇔ ⇦⇧⇨⇩ ￩￪￫￬" src="images/arrows.svg" height="21"></picture>
    - ticks and crosses:<br><picture><source media="(prefers-color-scheme: dark)" srcset="images/ticks-dark.svg"><img alt="☐☑☒ ✓✔✕✖✗✘" src="images/ticks.svg" height="21"></picture>
    - box drawing:<br><picture><source media="(prefers-color-scheme: dark)" srcset="images/box-drawing-dark.svg"><img alt="─│┌┐└┘├┤┬┴┼╭╮╯╰╱╲╳╴╵╶╷" src="images/box-drawing.svg" height="21"></picture>
    - game characters:<br><picture><source media="(prefers-color-scheme: dark)" srcset="images/games-dark.svg"><img alt="♔♕♖♗♘♙♚♛♜♝♞♟ ♠♡♢♣♤♥♦♧" src="images/games.svg" height="21"></picture>
    - currency:<br><picture><source media="(prefers-color-scheme: dark)" srcset="images/currency-dark.svg"><img alt="$ £ € ¥ ₹ ₽ ₩ ৳ ฿ ₿" src="images/currency.svg" height="21"></picture>
    - misc but useful:<br><picture><source media="(prefers-color-scheme: dark)" srcset="images/misc-dark.svg"><img alt="⌂☸ ♩♪♫♬♭♮♯ ♀♂⚢⚣⚤⚥⚦⚧⚨⚩⚭⚮⚯⚲ ⌘ ␣ ☉ ♿ 円圓" src="images/misc.svg" height="21"></picture>

1. All the operators [parsed by Julia](https://github.com/JuliaLang/julia/blob/master/src/julia-parser.scm) (which is itself a good test of a technical font).

1. [Unicode mathematical alphanumeric symbols](https://en.wikipedia.org/wiki/Mathematical_Alphanumeric_Symbols):

    <picture><source media="(prefers-color-scheme: dark)" srcset="images/alphanumerics-dark.svg"><img alt="𝐀𝐴𝑨 𝒜𝒲𝓐 𝔄 𝔸 𝕬 𝖠𝗔𝘈𝘼 𝙰" src="images/alphanumerics.svg" height="21"></picture>

    The script capitals come in both roundhand (the default, `\mathscr`) and chancery (`\mathcal`) styles:

    <picture><source media="(prefers-color-scheme: dark)" srcset="images/script-roundhand-dark.svg"><img alt="the script capitals A to Z, roundhand" src="images/script-roundhand.svg" height="21"></picture>

    <picture><source media="(prefers-color-scheme: dark)" srcset="images/script-chancery-dark.svg"><img alt="the script capitals A to Z, chancery" src="images/script-chancery.svg" height="21"></picture>

    The chancery forms are reached by Unicode's variation sequence (the capital followed by U+FE00) or by the `ss01` feature, which is what `unicode-math` uses: `\setmathfont{Lisnoti}[range=\mathcal, StylisticSet=1]`.

1. The other standardised variation sequences of the maths blocks, each shown here after its base: the cups and caps with serifs, the circled operators with a white rim, the subsets with the stroke through both lower members, the relations with a slanted equals, the empty set and the zero with a slash (the only zero in the font without a dot, and only reachable this way):

    <picture><source media="(prefers-color-scheme: dark)" srcset="images/variation-sequences-dark.svg"><img alt="∩ ∩︀ ∪ ∪︀ ⊓ ⊓︀ ⊔ ⊔︀ ⊕ ⊕︀ ⊗ ⊗︀ ⊜ ⊜︀ ⊊ ⊊︀ ⊋ ⊋︀ ≨ ≨︀ ⪬ ⪬︀ ∅ ∅︀ 0 0︀" src="images/variation-sequences.svg" height="21"></picture>

(If you want all the above but with a monospaced font, then take a look at [Julia Mono](https://juliamono.netlify.app/).)

## What changed in 2.000

Lisnoti 2.000 is a rebuild of the font from scratch, with every glyph, advance, kern and anchor checked against the 1.002 release as it went. In summary:

- The base is [Noto Sans](https://fonts.google.com/noto/specimen/Noto+Sans) 2.015 (1.002 was built on 2.013) and the maths donor is [Noto Sans Math](https://fonts.google.com/noto/specimen/Noto+Sans+Math) 3.000, Khaled Hosny's 2024 redesign, which brought the `MATH` table, a lower maths axis that the arithmetic and comparison operators all share, and some 2,500 more glyphs, the stretchy size variants and assembly parts among them.
- The *n*-ary operators, the radical sign and its size variants, the tick and cross family, the colon-equals family and the diameter sign are drawn or derived by rule so that they agree with one another and with the maths donor's stroke.
- Mark anchors and the sub and superscript kerning are built for every glyph Lisnoti changes, rather than inherited.
- The standardised variation sequences of Unicode's maths blocks are carried, and the chancery script capitals are also on `ss01`.
- The user-selectable alternates that undo Lisnoti's point (a slashed or dotless zero, an unserifed `I`, oldstyle or proportional figures) are gone: the default digits are lining and tabular, and every zero carries the dot unless a document asks for the slashed form by variation sequence.
- The web fonts are sliced by script and use, as Google Fonts serves Noto, so a Latin-only page fetches about 27 KB rather than 400 KB.
- WOFF ('WOFF 1') files are no longer produced on the basis that every browser now in use supports WOFF2.
