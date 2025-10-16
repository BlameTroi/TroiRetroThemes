# Troi's Retro CRT inspired themes

## Preamble

> Syntax highlighting is juvenile. When I was a child, I was taught arithmetic using colored rods. I grew up and today I use monochromatic numerals.
>
> Rob Pike in the golang-nuts google group.

> An attempt at a color scheme that does not look like a clown puked up the source code.
>
> From the readme for no-clown-fiesta.nvim on GitHub.

Or as I see it:

> Gratuitous syntax highlighting considered harmful.

## Summary

I'm writing retro leaning themes for the Helix editor that try to find a sweet spot between retro minimalism and modern language tools.

## Motivation

Bad eyesight and fondness for mainframe era terminals.

The best of these was the IBM 3278-4. For a dash of color the 3279 provided seven. An amber alternative was the 3290 information panel (meant more for display than interaction). Monochrome monitors for micro and mini computer systems came in green, amber, or white.

## Design and Implementation

At the highest level, modern computer language source code is made up of:

- Reserved words (the vocabulary).
- Comments.
- Variable names.
- Literals.
- Operators.

Modern tooling can classify each token in source code into one of dozens (if not hundreds) of categories beyond those listed. *What is the scope of a variable? Is this a built-in function name? Is this a class or instance function?*

I don't know either color or UX theory but I know what I can read. I want fewer colors and good contrast. While I lean toward Pike's "syntax highlighting is juvenile" I am not an absolutist. I think colors and fonts should provide hinting to guide the reader to important things.

## Prior art

I never found a theme I liked, but I did find good examples of palette and component theming from Emacs' `vegetative.el`, Vim's `amber color scheme`, and the excellent minimalistic `Acme` themes. Helix's built-in `ao` theme provides an extensive list of themeable UI elements. All of these can be found on GitHub.

From there it was a matter of experimenting to find what worked and come up with my own rules for theming.

## Rules for these themes

Early programming texts would use fonts to distinguish between keywords, comments, and other text.

Based on spirit of those textbook conventions and my experience with IBM's TSO and VM/CMS editors on 3270 series terminals, these are my rules for a theme:

- One predominate color for program text.
- Reserved words in italics.
- Comments in dim italics.
- Literals and punctuation in a different but complementary color from the program text.
- The editor UI elements are kept in the background by using dimmer complementary colors.

This brings the actual program code to the fore.

## Installation and Use

Copy the theme files to your local configuration (`~/.config/helix/themes` on Mac and Linux) and select the theme from the editor command line or your `config.toml` file.

## AUTHORSHIP, LICENSING, AND COPYRIGHT

My work is copyright (c) 2025 by Troy Brumley. Whenever possible my work is released under (your choice of) the public domain under the terms of the UNLICENSE, or the MIT license.

Troy Brumley blametroi@gmail.com

October 2025\
Cincinnati Ohio

So let it be written.\
So let it be done.
