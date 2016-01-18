---
layout:    post
title:     "Spacemacs!"
date:      2015-12-18
author:    "Dave Anderson"
subtitle:  "A cheatsheet"
---

When I first arrived at Recurse Center, one of my favorite memories was Diego enthusiastically describing the spacemacs extension for emacs. "You're going to love this," he said. It's pretty great.

Some other alternative text editors include Sublime Text 3, Atom, emacs and VIM. modal editors.

Spacemacs White belt.

Belts - their order and meaning http://www.wmacenter.com/index.cfm?page=17
White
Introduction to emacs, spacemacs, its plugins and terms.
Direct to installation instructions. Advise use of EVIL mode for VI shortcuts and modal editing.
Important plug-ins
Important terms
Basic commands
- Leader key, The spacemacs help file
- Open/Create file
- Save file
- Navigate text
- Insert text (i, o)
- Basic search commands (/, n)
- Basic buffer commands (SPC TAB, SPC b d)
Yellow
- Edit configuration file for new layers
- Projects
- Windowing
- Advanced Navigation/editing with EVIL
Orange
- Navigation with Avy
- Restore file
Green
Blue
Purple
Brown
Red
Black

What is Emacs?
http://www.gnu.org/software/emacs/

What is Spacemacs?
https://github.com/syl20bnr/spacemacs

SPC f e d - edit spacemacs dotfile

Python layer
https://github.com/syl20bnr/spacemacs/tree/master/layers/%2Blang/python
Javascript layer
https://github.com/syl20bnr/spacemacs/tree/master/layers/%2Blang/javascript

What is EVIL mode?
https://bitbucket.org/lyro/evil/wiki/Home
https://github.com/cofi/evil-leader

What is Which-Key?
Leader key for discovery of keyboard shortcuts and application functionality SPC
Major mode leader: ,

https://github.com/justbur/emacs-which-key

What is Helm?
https://github.com/emacs-helm/helm

C-h/j/k/l - navigate helm buffer (arrow key)
C-g - close the helm buffer
SPC w b - switch to minibuffer window - if you need to restore focus to helm after clicking away

What is Projectile?
https://github.com/bbatsov/projectile

What is Avy?
https://github.com/abo-abo/avy

Built in to Emacs:
ido - Interactively DO anything. minibuffer with anywhere completion for commands?
https://www.emacswiki.org/emacs/InteractivelyDoThings

dired - special read-only buffer for viewing the contents of directories
http://www.gnu.org/software/emacs/manual/html_node/emacs/Dired.html

File
Directory
Tree
Project - folder containing a special file (such as a git repo)

Window
Buffer
Layouts

Major Mode
Minor Mode
micro-state
key binding

Package
Layer


Keyboard shortcuts
http://ergoemacs.org/emacs/emacs_kb_shortcuts_pain.html
C - Control
M - Meta (Alt)
S - Super (ex. Windows Key)
- - hold the key down (ex. C-m or C-M-m)

: command key (enables execution of VI commands like saving files and quitting)

Quit - When you're starting out, this is super useful when you've started a weird command and you want it to stop.

SPC ` - Go back to previous location (before jump) pops off of a stack, so you can use this multiple times

SPC f e d - find dotfile - opens the spacemacs configuration file for changing defaults and configured layers.

SPC h SPC - Spacemacs help - search in helm. Open "Spacemacs documentation"

. - evil-repeat - repeat previous command

Quit
C-g

Files (SPC f)
Open/Create File
SPC f f

Copy file
SPC f c

Delete file
SPC f D

Rename file
SPC f R

Get filename
SPC f y

Buffers (SPC b)
Search open buffers
SPC b b

Close Buffers
SPC b d
