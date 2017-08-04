![Release tag](https://img.shields.io/github/tag/hlissner/emacs-doom-themes.svg?label=release&style=flat-square)
[![MELPA](http://melpa.org/packages/doom-themes-badge.svg?style=flat-square)](http://melpa.org/#/doom-themes)
[![Build Status](https://travis-ci.org/hlissner/emacs-doom-themes.svg?branch=master&style=flat-square)](https://travis-ci.org/hlissner/emacs-doom-themes)
[![MIT](https://img.shields.io/badge/license-MIT-green.svg?style=flat-square)](./LICENSE)

# doom-themes

> **Announcement:** v2.0 of this package was released with three large changes:
>
>   + `doom-buffer-mode` and `doom-brighten-minibuffer` have been moved to a new
>     plugin: [solaire-mode]
>   + `doom-nlinum` was removed; line highlighting is now supported in nlinum 1.7
>   + A rewrite of doom-themes' backend and themes means problems or breakages
>     may have slipped through. [Let me know][issues] if you find one!

DOOM Themes is an opinionated UI plugin and pack of themes extracted from my
[emacs.d], inspired by some of my favorite color themes.

[See the screenshots.][screenshots]

## Features

- **Color themes:**
  - [X] `doom-one`: doom-themes' flagship theme, inspired by [Atom]'s One Dark themes
  - [X] `doom-vibrant`: a more vibrant version of `doom-one`
  - [X] `doom-molokai`: based on Textmate's monokai
  - [X] `doom-nova`: adapted from [Nova] (thanks to [bigardone])
  - [ ] `doom-one-light`: light version of doom-one
  - [ ] `doom-x`: reads your colors from ~/.Xresources
  - [ ] `doom-tomorrow-night` / `doom-tomorrow-day`: by [Chris Kempson][tomorrow]
  - [ ] `doom-spacegrey`: [I'm sure you've heard of it][spacegrey]
  - [ ] `doom-mono-dark` / `doom-mono-light`: a minimalistic, monochromatic theme
  - [ ] `doom-tron`: based on Tron Legacy from [daylerees' themes][daylerees]
  - [ ] `doom-peacock`: based on Peacock from [daylerees' themes][daylerees]
- **Included features:**
  - `(doom-themes-visual-bell-config)`: flash the mode-line when the Emacs bell
    rings (i.e. an error occurs).
  - `(doom-themes-neotree-config)`: a customizable [neotree] theme that takes
    after [Atom]'s file drawer, and is simpler than the built in icon theme in
    neotree ([screenshot](/../screenshots/doom-one.png), [more details][wiki]).

    This requires `all-the-icons`' fonts to be installed: `M-x
    all-the-icons-install-fonts`
- **Resources that may interest you:**
  - To get dimmed sidebars and brighter source buffers (like in the
    [screenshots]), see [solaire-mode].
  - To get line number highlighting for `nlinum`, see [nlinum-hl] (or [hlinum] for
    `linum`).
  - [AnthonyDiGirolamo] added doom-one ([screenshot][airline-doom-one]) and
    doom-molokai ([screenshot][airline-doom-molokai]) skins
    to [airline-themes][airline-themes].
  - I'm working on making my modeline more accessible. In the meantime, check
    out [my mode-line configuration][mode-line] in my [emacs.d].

## Install

`M-x package-install RET doom-themes`

A comprehensive configuration example:

```emacs-lisp
(require 'doom-themes)

;; Global settings (defaults)
(setq doom-themes-enable-bold t    ; if nil, bold is universally disabled
      doom-themes-enable-italic t) ; if nil, italics is universally disabled

;; Load the theme (doom-one, doom-molokai, etc); keep in mind that each theme
;; may have their own settings.
(load-theme 'doom-one t)

;; Enable flashing mode-line on errors
(doom-themes-visual-bell-config)

;; Enable custom neotree theme
(doom-themes-neotree-config)  ; all-the-icons fonts must be installed!
```

[The wiki contains details for customizing the neotree theme][wiki].

## Contribute

I welcome contributions of any kind, be they pull requests, bug reports or elisp
pointers. Additional theme and plugin support requests are welcome too.


[AnthonyDiGirolamo]: https://github.com/AnthonyDiGirolamo
[Atom]: http://atom.io
[Nova]: https://trevordmiller.com/projects/nova
[airline-doom-molokai]: https://github.com/AnthonyDiGirolamo/airline-themes/raw/master/screenshots/airline-doom-molokai-theme.png
[airline-doom-one]: https://github.com/AnthonyDiGirolamo/airline-themes/raw/master/screenshots/airline-doom-one-theme.png
[airline-themes]: https://github.com/AnthonyDiGirolamo/airline-themes
[all-the-icons]: https://github.com/domtronn/all-the-icons.el
[bigardone]: https://github.com/bigardone
[daylerees]: http://daylerees.github.io/
[emacs.d]: https://github.com/hlissner/.emacs.d
[hlinum]: https://melpa.org/#/hlinum
[issues]: https://github.com/hlissner/emacs-doom-themes/issues
[mode-line]: https://github.com/hlissner/.emacs.d/blob/master/modules/ui/doom-modeline/config.el
[neotree]: https://github.com/jaypei/emacs-neotree
[nlinum-hl]: https://github.com/hlissner/emacs-nlinum-hl
[screenshots]: https://github.com/hlissner/emacs-doom-themes/tree/screenshots
[solaire-mode]: https://github.com/hlissner/emacs-solaire-mode
[spacegrey]: http://kkga.github.io/spacegray/
[tomorrow]: https://github.com/ChrisKempson/Tomorrow-Theme
[wiki]: https://github.com/hlissner/emacs-doom-themes/wiki