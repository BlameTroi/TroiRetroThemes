# On IBM 3270 displays

Wikipedia has a very detailed description of the [IBM 3270](https://en.wikipedia.org/wiki/IBM_3270) series of displays, controllers, and printers. While this history and communications architecture are interesting in their own right, we are only interested in its visible display characteristics here.

## Format and colors

While limited in size (80x25, 80x43, 80x32, plus some printer width options) the 3270 CRT was very readable.

On monochrome 3270 terminals, the display was green or bright green on a dark background. The display background was not a true black, more of a very faint green. Later models offered four or seven colors.

## The base 3270 display

All 3270 displays build upon the architecture of the original monochrome models. Unlike modern character or bit addressable displays, the 3270 family displayed characters within fields. Fields were used for transmission efficiency–think communications packets.

Fields had attributes: the position of the field on the display, length, contents, could it be modified, was it visible, etc. The attributes that apply to theming are:

- Displayable
- Protected
- Intensified

### Four color displays

Four color models mapped colors to attributes thusly:

|             | normal | intensified |
| ----------- | ------ | ----------- |
| protected   | blue   | white       |
| unprotected | green  | red         |

### Seven color displays

Later models offered seven colors and additional attributes:

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
