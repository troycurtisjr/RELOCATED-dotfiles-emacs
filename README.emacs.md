# My Sneakernet spacemacs Configuration
This project is my attempt to make a usable [spacemacs](http://spacemacs.org) configuration that can be taken via sneaker-net and used in a mode complete disconnected from the Internet.  I really like using spacemacs, but many of it's underlying framework features presume you have a working Internet connection.  This isn't always the case with me.  So this is my one-stop-shot for my preferred configuration.

# Getting Started
This project expects to be rooted at the top-level of your home directory.  Generally it is a bad idea to have a git repo at the top-level of your home directory, so I use the [vcsh](https://github.com/RichiH/vcsh) project.  This allows git control of any files in your home directory without any of the symlink hacks that other options have.  If you don't want to adopt vcsh, then you should be able to grab a zip archive and extract it into you home directory.

Also, since this is based on the spacemacs project, it has the same requirement of at least emacs 24.5.

Once all the files are in place, fire up the right version of emacs.  The first launch will be a bit slow, so the first order of business is the byte-compile most of the scripts.  Do this by typing `SPC : spacemacs/recompile-elpa`.  This will take a bit, but subsequent launches will be much faster.

There is pretty good docs right from the splash screen that you can use to get started.

# Notes for Vimmers
With the evile plugin, the vast majority of keybindings will be natural to vim users.  I also have the "hybrid" mode enabled, which means that while in insert mode, most of the Emacs native style keybindings are available.  These are the same ones that you might use in your default shell keybindings.

# Quick Reference
- Common VIM Command
  - Basically all the VIM commands I use, visual mode/insert/block/normal
- Basic
  - SPC qq -or- Ctrl-X Ctrl-C :: Quit, asking to save modified files
  - SPC hi -or Ctrl-H i :: Get online help
  - SPC h SPC :: spacemacs help
  - SPC : -or- Alt-x :: Run emacs command
- Basic EMACS commands
  - Needed especially when "finding" a file, in helm, or in buffer screens. Of course arrow keys/home/end can be used instead
  - Ctrl-n :: Down a line
  - Ctrl-p :: Up a line
  - Ctrl-b :: Move left by one character
  - Ctrl-f :: Move right by one character
  - Ctrl-v :: Page down
  - Alt-v :: Page up
  - Ctrl-a :: Move to start of line
  - Ctrl-e :: Move to end of line
- Window/Buffer Management
  - SPC w 3 :: Opens a three split mode (also 2 version)
  - SPC <num> or <Alt>+<num> :: Go directly to numbered window
  - SPC w c :: Close the current window (buffer still open in background)
  - SPC b k :: Kill buffer, closes out the buffer (not open in background) 
  - SPC b b :: Helm selection of buffer + recent files
- File Management
  - SPC f f :: Open the file-visit dialog, open a file
  - SPC f s :: Save current file
  - SPC f S :: Save all modified files
  - SPC f j :: "Jump" to dired mode, open parent directory of current file
- General Features 
  - SPC t :: Show lots of options you can toggle on and off
  - SPC hl :: Resumes most recent helm command, cscope, file open, buffer, etc.
- C/C++ Development
  - Tags
    - SPC p G :: Regenerate tags file  
    - SPC p y :: Find tag
  - cscope
    - , g i :: Create cscope index file
    - , g r :: Find this symbol
    - , g d :: Find this definition
    - , g f :: Find this file
  - Editing
    - VISUAL: gc :: Comment/Uncomment  selected code
    - Normal: gcc :: Comment/Uncomment current line
  - Snippets
    - `After typing keyword, type Alt-/ useful keywords:
      - if 
      - while
      - once (header inclusion protection)
