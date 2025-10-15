# Troi's Retro CRT inspired themes

## Summary

Some retro leaning themes for the Helix editor that try to find a sweet spot between retro minimalism and modern language tools.

## Motivation

Bad eyesight and fondness for mainframe era terminals.

The best of these was the IBM 3278-4. For a dash of color the 3279 provided eight. An amber alternative was the 3290 information panel (meant more for display than interaction). Monochrome monitors for micro and mini computer systems came in green, amber, or white.

## Design and Implementation

I don't know either color or UX theory but I know what I can read. I want fewer colors and good contrast. While I lean toward Pike's "syntax highlighting is juvenile" I am not an absolutist. I think colors and fonts should provide hinting to guide the reader to important things.

I found good examples of palette and component theming from Emacs' `vegetative.el`, Vim's `amber color scheme`, and the excellent minimalistic `Acme` themes. Helix's built-in `ao` theme provides an extensive list of themeable UI elements and was my theme template file.

From there it was a matter of experimenting to find what worked and come up with my own rules for theming. I can't clearly articulate them yet.

## Installation and Use

Copy the theme files to your local configuration (`~/.config/helix/themes` on Mac and Linux) and select the theme from the editor command line or your `config.toml` file.

## Prior Art

As mentioned earlier:

- I borrowed my green screen palette from the Emacs `vegetative.el`.
- I borrowed my amber screen palette from the Vim `amber color scheme`.
- I used both built-in `ao` theme for Helix and the `helix-theme-template` to come up with both the layout and list of themeable elements.

All of these can be found on GitHub.

## AUTHORSHIP, LICENSING, AND COPYRIGHT

My work is copyright (c) 2025 by Troy Brumley. Whenever possible my work is released under (your choice of) the public domain under the terms of the UNLICENSE, or the MIT license.

Troy Brumley blametroi@gmail.com

October 2025\
Cincinnati Ohio

So let it be written.\
So let it be done.
