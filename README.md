
## GNU Emacs / N Λ N O 

**GNU Emacs / N Λ N O** is a set of configuration files for GNU Emacs
such as to provide a nice and consistent look and feel as shown below.
It is based on design principles I described in the article "[On the
design of text Editors](https://arxiv.org/abs/2008.06030)" that is
available on arXiv. The light theme is based on [Material
colors](https://material.io/) and the dark theme is based on [Nord
colors](https://www.nordtheme.com/).

The philosophy of nano emacs is to stick as much as possible to
vanilla emacs without introducing too much dependencies (or none if
possible) and to keep it modular enough. The idea is for users to copy
the part they are interested in such as to include them in their own
configuration.

<div>
<img src="./images/nano-emacs-light.png" width=47.5%>
<img src="./images/nano-emacs-dark.png"  width=47.5%>
</div>

### Requirements

You need a recent version of
[GNU Emacs](https://www.gnu.org/software/emacs/) and to have the
[Roboto Mono](https://fonts.google.com/specimen/Roboto+Mono) and
[Fira Code](https://fonts.google.com/specimen/Fira+Code) fonts
installed on your system. There are no other dependencies.

### Quick test

The easiest way to test nano emacs is to clone the directory on your
desktop and to type (from inside the cloned repository):

```
$ emacs -q -l nano.el
```

### Installation

If you like the result, you can merge the content of
[nano.el](nano.el) into your emacs configuration file. To do so,
you'll need to modify the `load-path` to include the nano emacs
repository and then call for the different modules. The only mandatory
module is the theme that defines 6 faces that are used in other
modules.

```shell
# nano emacs
export nano_emacs="$HOME/fun/nano-emacs"
alias nano_emacs="cd $nano_emacs && $(which emacs) -q -l ${nano_emacs}/nano.el -dark &; cd -"
```

### Modules


<img align="right" alt="mandatory" src="https://img.shields.io/badge/-mandatory-red?style=flat-square">

- **[nano-theme-light.el](./nano-theme-light.el)** or
  **[nano-theme-dark.el](./nano-theme-dark.el)** Theses modules define a
  light and dark themes respectively through the defnition of the different
  faces that will be used by other modules.  It is thus mandatory (one of
  dark or light version).

<img align="right" alt="optional" src="https://img.shields.io/badge/-optional-blue?style=flat-square">

- **[nano.el](./nano.el)** This module is only used to test nano emacs
  locally. Its content is supposed to be merged into an existing emacs
  configuration.

<img align="right" alt="optional" src="https://img.shields.io/badge/-optional-blue?style=flat-square">

- **[nano-help.el](./nano-help.el)** This module provides a function to
  display a small message in the echo area.


<img align="right" alt="optional" src="https://img.shields.io/badge/-optional-blue?style=flat-square">

- **[nano-modeline.el](./nano-modeline.el)** This module define a
  header line that is mode dependent and take care of hiding the
  modeline when necessary.


<img align="right" alt="optional" src="https://img.shields.io/badge/-optional-blue?style=flat-square">

- **[nano-layout.el](./nano-layout.el)** This module define the overall layout of an emacs frame, defining default font, fringes, margins, etc.
	
<img align="right" alt="optional" src="https://img.shields.io/badge/-optional-blue?style=flat-square">

- **[nano-splash.el](./nano-splash.el)** This module provides a splash
  screen when emacs is started.


<img align="right" alt="optional" src="https://img.shields.io/badge/-optional-blue?style=flat-square">

- **[nano-colors.el](./nano-colors.el)** This module provides a collection of colors palettes with function for easily accessing them.








