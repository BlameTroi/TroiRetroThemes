# Theming and syntax highlighting

*Draft*

> Syntax highlighting is juvenile. When I was a child, I was taught arithmetic using colored rods. I grew up and today I use monochromatic numerals.
>
> Rob Pike in the golang-nuts google group.

> An attempt at a color scheme that does not look like a clown puked up the source code.
>
> From the readme for no-clown-fiesta.nvim on GitHub.

Or as I see it:

> Gratuitous syntax highlighting considered harmful.

My goal is to find a workable theme design that meets my requirements:

- High contrast.
- Color and brightness levels that are friendly to older eyes.
- Make it easy to focus on code without visual distraction from either excessive highlighting or the editor's UI.
- Honors early mainframe and minicomputer sensibilities.

## Background

Things have come a long way from the early days of computing:

- Printers and video terminals had one font and one color. If you were lucky a printer would be able to simulate bold text and a video terminal had two levels of brightness and reverse video.
- Compilation and code analysis were expensive and often batch processes.

Today:

- Almost no one uses printers for code listings.
- Workstation displays can display thousands of distinct colors.
- Font size and shape are no longer fixed by hardware.
- Compilation and code analysis run quickly in the background providing both diagnostics and syntax analysis of program code.

But too much color makes the program code display both ugly and uninformative.

## My approach

At the highest level, modern computer language source code is made up of:

- Reserved words (the vocabulary).
- Comments.
- Variable names.
- Literals.
- Operators.

Early programming texts would use fonts to distinguish between keywords, comments, and other text.

Based on those textbook conventions and experience with IBM's TSO and VM/CMS system editors, these are my rules for a theme:

- One predominate color for program text.
- Reserved words in italics.
- Comments in dim italics.
- Literals and punctuation in a different but complementary color from the program text.
- The editor UI elements are kept in the background by using dimmer complementary colors.

This brings the actual program code to the fore.

## Platform

The Helix editor is both easy to use and theme. There are no legacy plugins to support and highlighting is based upon Tree-sitter grammars which use a standard vocabulary for all languages.

## Conclusion

The `TroiRetroGreen` theme is inspired by the IBM 3270 family of terminals. I hope to add an amber theme (IBM 3290), and a 7-color theme (IBM 3279).

## Appendices

### Theming in Helix

My Helix themes will use monochrome green/amber/white predominately, with some shading. There are enough useful UI features of Helix to warrant using more colors, but they will be limited to the framing UI. Source code/text will use the predominate color, some shading, and italics.

Red and yellow are often used for errors and warnings.

Reverse video is used for the cursor and some selections. There outlining or blinking text.

### IBM 3270 terminals: format and colors

These were CRT displays, initially using green phosphor. The display background was not a true black, and was very faintly green. Unlike modern character or bit addressable displays, the 3270 family displayed characters within fields. The fielding was for transmission efficiency. Fields had attributes: binary switches describing how to display the field and whether or not it was modifiable.

#### Basic 3270 displays

The field attributes that relate to color theming are:

- Protected
- Displayable
- Intensified

On monochrome 3270 series terminals, the display was green or bright green on a dark background.

#### Adding color

#### Four color displays

Four color models mapped colors to attributes thusly:

|             | normal | intensified |
| ----------- | ------ | ----------- |
| protected   | blue   | white       |
| unprotected | green  | red         |

#### Seven color displays

More advanced models offered seven colors and additional attributes:

The colors:

- White
- Red
- Blue
- Green (default)
- Pink (magenta)
- Yellow
- Turquoise (cyan)

The additional attributes:

- Blinking
- Reversed
- Underscored
- Outlined
