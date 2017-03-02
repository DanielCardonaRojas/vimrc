# Dotfiles

Mostly vim setup documentation, but also some notes on tmux and zsh configs.

## Vim Setup

Do the following: 

1. Move to home directory 

```shell
cd ~
```

2. initialize a git repository and point it to the remote repository 

```shell
git init && git remote add origin https://github.com/DanielCardonaRojas/dotfiles
```

3. Sync with master

```shell
git pull origin master
```

4. Install Plug (a minimalistic vim plugin manager) running the shell command. paste the curl command from [here](https://github.com/junegunn/vim-plug)

5. After this has been done enter vim and type: ":PlugInstall" this will download and install all plugins.

6. Install YouCompleteMe 

To see a OS specific setup or more detailed explanation see [YCM repo](https://github.com/Valloric/YouCompleteMe) 
Also to give support to other languages see [YCM repo](https://github.com/Valloric/YouCompleteMe)

For mac: 

```shell
brew install cmake
```
For ubuntu:

```shell
sudo apt-get install cmake
sudo apt-get install python-dev python3-dev
```

``` shell
cd ~/.vim/plugged/YouCompleteMe
git submodule update --init --recursive
./install.py --clang-completer 
```


## Vim [Plugins](http://vimawesome.com/)

    
- Ultisnips: Lets you create snippets for different file formats.
Look at the repository [here] (https://github.com/SirVer/ultisnips)

- Three themes are used in this vimrc [Solarized](http://ethanschoonover.com/solarized), [Monokai](https://github.com/crusoexia/vim-monokai) and [Gruvbox](https://github.com/morhetz/gruvbox/wiki/Configuration).

- [Airline](https://github.com/vim-airline/vim-airline): Gives a nice look to the status bar in vim. Its a replacement of an
older plugin called Powerline, take a look at the repository [here] (https://github.com/vim-airline/vim-airline)
- [Sparkup](https://github.com/rstacruz/sparkup): Lets you write html code faster.
- [NerdTree](https://github.com/scrooloose/nerdtree): Power Vim with directory navigation.
- [Gundo](https://github.com/sjl/gundo.vim): Graphical undo lets you visualize then undo tree.
- [EasyMotion](https://github.com/easymotion/vim-easymotion): Easy motion lets you move fast to any word on screen. Very cool
- [Ctrlp](https://kien.github.io/ctrlp.vim/): Is a fuzzy file finder, lets you quickly search for files open them in split windows,tabs etc.
- [Rainbow Parentheses](http://vimawesome.com/plugin/rainbow-parentheses-vim): Colors parentheses, braces, brackets based on indentation.
- [Vim-surround](https://github.com/tpope/vim-surround): Is a plugin for ease of wrapping words in parentheses, brackets, quotes.
- [vim-unimpaired](https://github.com/tpope/vim-unimpaired): Some useful command starting by `[` or `]`, like move through tabs and buffers.
- [vim-signature](https://github.com/kshenoy/vim-signature): Visualize, create and navigate through marks easily.

- Hoogle: Lets you use the Hoogle search engine to lookup Haskell functions and types.
- Fugitive: Lets you call git commands, from within vim. 

- TagBar/ctags: *ctags* indexes files to extract locations of functions, class variable definitions. Tagbar lets you navigate through these breakpoints.


## Colorschemes 
There are two available colorschemes solarized and monokai, to switch between the two do:
> :colorscheme gruvbox
> :colorscheme solarized
> :colorscheme monokai

To select black solarized scheme do

> :set background=dark

## Plugin Configuration

### Key bindings for this vimrc
| Action | Command|
|:------:|:------:|
|Write file | ,w |
|Edit vimrc | ,ev |
|Close Split | ,cw |
|Show directory | ,f|
|Move to right split | ,h|
|Move to left split | ,l|
|Move to upper split | ,k|
|Move to lower split | ,j|
|Create right split | ,sh|
|Create left split | ,sl|
|Create upper split | ,sk|
|Create lower split | ,sj|
|Increment vertical split size | ,> |
|Decrement vertical split size | ,< |
|Increment horizontal split size | ,K |
|Decrement horizontal split size | ,J |
|Swap current line with upper | K |
|Swap current line with lower | J |
|Toggle spell checking | ,ss|
|Choose spell language | ,sc|
|Paste from OS clipboard |,p|
|Copy into OS clipboard |,y|
|Run a terminal command  | ctr-space |
|Replace all ocurrances of word under cursor | ,S |
|Paste yank buffer to vim command  | ,r0 |
|Paste yank buffer to terminal command  | ,R0 |

### Other mappings

| Action | Command|
|:------:|:------:|
| yank inside line | yil |
| select inside line | vil |
| yank line without new line char | yal |
| select line without new line char | val |
| Show/Hide highlight matches | F3 |
| Toggle paste mode | F2 |

### Plugin Key Bindings
| Action | Command|
|:------:|:------:|
|Comment line | ,c<space>|
| Change comment style | ,ca |
| Tagbar Toggle | ,tt |
| Delete surrounding quotes | ds' |
| Delete surrounding html tag | dst |
| Surround word with ' | ysiw' |
| Surround visual selection in quotes | v<motion>S' |
| Ctrlp fuzzy search | ctrl+p |
| CtrlP Most recently used files | ,m |
| CtrlP on the current files directory | ,<space> |
| EasyMotion Jump to any word with | ,,w |
| Gundo Show/Hide undo tree (Gundo) | F5 |
| Sparkup expand | ctrl+e |
| Sparkup jump to next edit point in insert mode | ctrl+n |
| Ultisnip expand snippet | ctrl+j |
| Ultisnip jump to next edit point | ctrl+b |
| Ultisnip jump to previous edit point | ctrl+z |
| EasyMotion jump to firt letter of any word after cursor | ,,w |
| EasyMotion jump to firt letter of any word before cursor | ,,b |
| EasyMotion jump to any letter of any word after cursor | ,,f<someLetter> |
| Unimpaired move left through buffers | [b  |
| Unimpaired move right through buffers | ]b  |
| Unimpaired swap lines (with line above) | [e  |
| Unimpaired swap lines (with line below) | ]e  |
| Vim-Signature mark current line with next available marker | m, |
| Vim-Signature navigate through markers | \]\` OR \[\` |

### Context sensitive Key bindings
| Context | Action | Command|
|:------:|:------:|:------:|
| CtrlP open | ctrl-f | Toggle files, most recently used, etc |
| NERDTree open | t | opens file in new tab
| CtrlP open | file in new tab | ctrl+t |
| CtrlP open | file in vsplit | ctrl+v |
| CtrlP open | file in horizontal split | ctrl+s ctrl+x |
| CtrlP open | move up and down | ctrl+k ctrl+j |

### Native Vim key bindings

| Action | Command|
|:------:|:------:|
| Autocompletion | ctr-n |
| Uppercase | gU[motion] |
| Jump between paragraphs | {} |
| Spell correction | z= |
| Close code fold | zc |
| Open code fold | zo |
| Open/close all folds | zR , zM|
| Open file in new tab | :tabe <file_name> |
| Jump to next tab | gt |
| Jump to prev tab | gT |
| Repeat last f or t command | ; |
| Repeat last : command | @: |



### Window Splits
Vim can do window splits to any order. So having key bindings to do this fase is very important.

> nmap <silent> <leader>sh :leftabove  vnew<CR>

Leader is a custom defined key that is mapped to the ',' key so basically typing ,sh is the same as typing the :leafabove vnew command and hiting enter (CR) which creates a new vertical split to the left.

## Basic Settings

### Useful external commands and tools

Some of the features I've loved most learning Vim:

Executing external commands from withing Vim. This is done typing **:!**someProgram
this lets you compile programs easily, or do anything else. For example convert markdown to html with pandoc.

**Pandoc Integration**

To create html from markdown run :PandocMD html, the first argument to :PandocMD is the value for the -t flag witch you would 
normally pass to the command line program. This is just so different type of documents can be rendered.

To create revealjs deck of slides

1. Download revealjs and put in the same directory where the markdown file is.
2. Maybe the downloaded revealjs folder comes with a version number.
Remove so its named reveal.js only.
3. Run this command from terminal in the corresponding directory: 
```$
pandoc -s -S -t revealjs -o test.html revealjsPandoc.md -V theme=blood
```

Theme can be chosen from one of [revealjs themes](). I liked these themes:

- solarized
- blood
- moon
- beige

To create html from markdown

```shell
pandoc input.md -s -o output.html
```

#Notes

To add other files to the repository:

```shell
git add -f <fileName>
```

# Other settings

To install Vim 7.4 update xcode command line tools. Then run `brew install vim`

## TMUX Setup

If working with tmux its important to make these changes, for key bindings to work.
[link](http://superuser.com/questions/660013/resizing-pane-is-not-working-for-tmux-on-mac)


**Install/Upgrade to lates tmux** 
```shell
sudo apt-get remove tmux
sudo apt-get install exuberant-ctags cmake libevent-dev libncurses5-dev
wget https://github.com/tmux/tmux/releases/download/2.3/tmux-2.3.tar.gz
tar xvzf tmux-2.3.tar.gz
chmod +x tmux-2.3/*
cd tmux-2.3
./configure && make
sudo make install
tmux -V
```

Install tmux plugin [manager](https://github.com/tmux-plugins/tpm) needed to install tmux-resurrect
====

**Not needed with macvim or linux terminals**

Note that solarized term256 must be turned off in linux gnome terminal (not shure if i need this or not)
on mac edit vimrc (,ev) line with "let g:solarized_termcolors=256" uncommenting it.

To fully use this vimrc we have to do the following: 

- Install Mac terminal solarized profile, downloading the solazirized.zip from [here](http://ethanschoonover.com/solarized). There should be a osx-terminal.app-colors-solarized folder. Import this to osx terminal profiles.
- Install powerline fonts by downloading zip from [here](https://github.com/powerline/fonts) and running ./install.sh on inside the downloaded folder containing the fonts.
- Check to have at least an old version of ctags 
> tmux source-file ~/.tmux.conf

### TMUX Keybindings and Commands

List all sessions
```shell
tmux ls
```

Start a new session with a name
```shell
tmux new -s myname
```

Attach to an existing session
```shell
tmux a -t myname
```

Kill a session
```shell
tmux kill-session -t myname
```

Prefix = Ctrl + b

| Action | Command|
|:------:|:------:|
| Tmux resurrect save | prefix + Ctrl-s |
| Tmux resurrect restore | prefix + Ctrl-r |
| Tmux tpm install plugins | prefix + I |
| Tmux source config | prefix + r |

**Sessions** 

- d detach from session

**Windows**

- c  create window
- w  list windows
- n  next window
- p  previous window
- f  find window
- ,  name window
- &  kill window
- ]  paste

**Panes**

- %  vertical split
- "  horizontal split
- x  kill pane


**Moving between splits**

- h move to left pane
- l move to right pane
- k move to top pane
- j move to bottom pane

- J move horizontal split line down
- K move horizontal split line up
- H move vertical split line left
- L move vertical split line right

# TODO

- Fix: Add tmux mouse on depending on version
- Make copy and paste to systems clipboard work on other platforms besides mac
- Add youcompleteme with easy configuration.
- Maybe add a installation script
- Ultisnips save snippets in this repo
- Use augroup in vimrc so multiple common settings dont have to be repeated for different FileTypes.
