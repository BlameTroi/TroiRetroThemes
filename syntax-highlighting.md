# On Syntax Highlighting

> Syntax highlighting considered harmful.

No, not really. My stance is:

[https://github.com/troy.git](https:/github.git)

> Gratuitous syntax highlighting considered harmful.

## My arguments against syntax highlighting

```sh
# some shell code here
echo $@
```

```
block
blorg
blab
```

    this # or that
    or
    # boink
    that

And raw text `inline` here.

### And then there's this

asdf

#### four

##### five

###### VI

- I learned to program in the monochrome world.
- Theme authors can not resist creating distinct faces for each
  syntactic element.
- Excessive use of facing is more noise than information.
- Cluttered and poorly designed themes are visually tiring.

## Highlighting options in Helix

Helix supports syntax highlighting based on Tree-sitter scopes. Each
highlight target has:

- Foreground color (colors are 24-bit)
- Background color
- Optional underline
  - Color
  - Style
    - One of line, curl, dashed, dotted, or double-line.
- Font modifiers, any combination of:
  - Bold
  - Italic
  - Strike through
  - Dim
  - Blinking
  - Reversed foreground and background
  - Hidden

While the number of scope targets is language grammar dependent,
sample theme templates have thirty-plus keys for highlighting.

One color theme author (I forget exactly who) said some themes looked
like "a clown vomited on the screen".

## An extreme take

Rob Pike once wrote in the golang-nuts group:

> Syntax highlighting is juvenile. When I was a child, I was taught
> arithmetic using colored rods. I grew up and today I use
> monochromatic numerals.\
> -rob

## The bad old days

Teletypes and terminals had one font and one color. If you were lucky
a teletype would be able to simulate bold text and the terminal had
two intensities and reverse video.

And there were no *CPU* cycles free **for** deciding how to format
different parts of the source program.

Early programming texts would use fonts to distinguish between
keywords, comments, and other text.

## A happy medium

Trying to use highlights to convey rich detail is a mistake, but using
them to guide and hint is useful.

At the highest level, modern computer language source code is made up
of:

- Reserved words (the vocabulary).
- Comments.
- Variable names.
- Literals.
- Operators.

Borrowing from textbook conventions, I propose:

- One predominate color.
- Reserved words in italics.
- Comments in italics and dimmed.
- Literals and punctuation in a different color.
- The editor UI elements are kept in the background by using dimmer
  complementary colors.

This brings the actual program code to the fore.

## Conclusion

The retro inspired Helix themes I am writing (TroiRetro*) will honor
the above recommendations.
