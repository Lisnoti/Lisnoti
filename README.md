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

*Please bear in mind that this readme file is not itself typeset in Lisnoti, and so the character representations you see below are **not** the same as if they were in Lisnoti. A more accurate depiction is available [here](https://lisnoti.com/index.html#key-features).*

Lisnoti is derived from [Noto's sans serif fonts](https://fonts.google.com/noto/), but with the following adaptions:

1. Reliable distinction of upper case `I` and lower case `l`, and upper case `O` and zero `0`.

1. Consistent arithmetic, comparison, logic, set, *n*-ary and other maths operators, all sitting on one maths axis, e.g.

    - arithmetic: `− × ÷ ± ∓ ∞` (*NB Noto Sans gets the minus sign wrong*)
    - comparison: `≤ ≠ ≥ ≈ ≡ ≢ ∝`
    - logic: `¬ ∧ ∨ ⊻ ⊤ ⊥ ⊦`
    - set: `∩ ∪ ∈ ∉ ⊂ ⊃ ⊆ ⊇ ∅`
    - *n*-ary: `∑ ∏ ∐ ⋀ ⋁ ⋂ ⋃ ⨀ ⨁ ⨂`
    - other: `∫ ∂ √ Δ ∇ ∀ ∃`

1. An OpenType `MATH` table, so Lisnoti can be chosen as the equation font in Word and loaded by `unicode-math` in LuaLaTeX: fractions, radicals, big operators with limits, stretchy brackets and accents are all set from the font's own data.

1. Greek and Cyrillic letters -- maths and logic make frequent use of Greek letters and occasionally Cyrillic ones too.

1. Consistently formatted digit and -- if available -- Roman letter sub and superscripts, with kerning so that `x²` and `f⁽ⁿ⁾` sit properly:

    - superscript: `⁰¹²³⁴⁵⁶⁷⁸⁹⁽⁾⁺⁻ᵃᵇᶜᵈᵉᶠᵍʰⁱʲᵏˡᵐⁿᵒᵖ𐞥ʳˢᵗᵘᵛʷˣʸᶻᴬᴮꟲᴰᴱꟳᴳᴴᴵᴶᴷᴸᴹᴺᴼᴾꟴᴿᵀᵁⱽᵂ𐞲`
    - subscript: `₀₁₂₃₄₅₆₇₈₉₍₎₊₋ₐₑₕᵢⱼₖₗₘₙₒₚᵣₛₜᵤᵥ₝ₓ₞₟`

1. A reasonable selection of symbols, including

    - squares, diamonds, rectangles, triangles, circles and stars: `■□▪▫▬▭▮▯▰▱▲△▴▵▶▷▸▹►▻▼▽▾▿◀◁◂◃◄◅◆◇◊○◌●◦◯◻◼◽◾⚪⚫⚬★☆`
    - lots of arrows: `←↑→↓↔↕ ↖↗↘↙ ⇄ ⇅ ⇵ ⇆ ⇋⇌ ⇐ ⇒⇔ ⇦⇧⇨⇩  ￩￪￫￬`
    - ticks and crosses: `☐☑☒ ✓✔✕✖✗✘`
    - box drawing: `─│┌┐└┘├┤┬┴┼╭╮╯╰╱╲╳╴╵╶╷`
    - game characters: `♔♕♖♗♘♙♚♛♜♝♞♟ ♠♡♢♣♤♥♦♧`
    - currency: `$ £ € ¥ ₹ ₽ ₩ ৳ ฿ ₿`
    - misc but useful: `⌂☸ ♩♪♫♬♭♮♯ ♀♂⚢⚣⚤⚥⚦⚧⚨⚩⚭⚮⚯⚲ ⌘ ␣ ☉ ♿ 円圓`

1. All the operators [parsed by Julia](https://github.com/JuliaLang/julia/blob/master/src/julia-parser.scm) (which is itself a good test of a technical font).

1. [Unicode mathematical alphanumeric symbols](https://en.wikipedia.org/wiki/Mathematical_Alphanumeric_Symbols), e.g. `𝐀𝐴𝑨 𝒜𝒲𝓐 𝔄 𝔸 𝕬 𝖠𝗔𝘈𝘼 𝙰`, with the script capitals in both roundhand (the default, `\mathscr`) and chancery (`\mathcal`) styles. The chancery forms are reached by Unicode's variation sequence (the capital followed by U+FE00) or by the `ss01` feature, which is what `unicode-math` uses: `\setmathfont{Lisnoti}[range=\mathcal, StylisticSet=1]`.

1. The other standardised variation sequences of the maths blocks: `∩︀ ∪︀ ⊓︀ ⊔︀` with serifs, `⊕︀ ⊗︀` with a white rim, `⊊︀ ⊋︀` with the stroke through both lower members, `0︀` with a short slash (the only zero in the font without a dot, and only reachable this way), and so on.

(If you want all the above but with a monospaced font, then take a look at [Julia Mono](https://juliamono.netlify.app/).)

## What changed in 2.000

Lisnoti 2.000 is a rebuild of the font from scratch, with every glyph, advance, kern and anchor checked against the 1.002 release as it went. In summary:

- The base is [Noto Sans](https://fonts.google.com/noto/specimen/Noto+Sans) 2.015 (1.002 was built on 2.013) and the maths donor is [Noto Sans Math](https://fonts.google.com/noto/specimen/Noto+Sans+Math) 3.000, Khaled Hosny's 2024 redesign, which brought the `MATH` table, a lower maths axis that the arithmetic and comparison operators all share, and some 2,500 more glyphs, the stretchy size variants and assembly parts among them.
- The *n*-ary operators, the radical sign and its size variants, the tick and cross family, the colon-equals family and the diameter sign are drawn or derived by rule so that they agree with one another and with the maths donor's stroke.
- Mark anchors and the sub and superscript kerning are built for every glyph Lisnoti changes, rather than inherited.
- The standardised variation sequences of Unicode's maths blocks are carried, and the chancery script capitals are also on `ss01`.
- The user-selectable alternates that undo Lisnoti's point (a slashed or dotless zero, an unserifed `I`, oldstyle or proportional figures) are gone: the default digits are lining and tabular, and every zero carries the dot unless a document asks for the slashed form by variation sequence.
- The web fonts are sliced by script and use, as Google Fonts serves Noto, so a Latin-only page fetches about 27 KB rather than 400 KB.
- WOFF 1 files are no longer produced; every browser in use supports WOFF2.
