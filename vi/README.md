# Vi Editor

Vi or Vim is an text editor. 

> Learn Vi or Vim progressively. Only you can teach yourself Vi or Vim. The fastest way possible is to
> **start** by learning the minimal to survive, then you integrate all the
> tricks slowly. 

## Lesson one to survive in Vi

Whenever in doubt, press <kbd>Esc</kbd>. 
> Always press <kbd>Esc</kbd>. 

Do nothing and press <kbd>Esc</kbd> again.

Exit the editor Vi by pressing <kbd>Esc</kbd> -> type `:q!` -> <kbd>Enter</kbd>.

> But before we start, just a warning. Learning Vim will be painful at first.
> It will take time. Don't expect to be more efficient with vim than other
> editor in less than 3 days. In fact it will certainly take 2 weeks instead of
> 3 days. 

## Always press <kbd>Esc</kbd>

Any instruction does not explicitly <kbd>Esc</kbd> does includes
<kbd>Esc</kbd>. 

Always press <kbd>Esc</kbd> to enter <kbd>Normal</kbd> (or Command) mode before any
commands.

## How to learn from this note instruction

Commands starting with `:` ends with <kbd>Enter</kbd>. 

For example, when I write `:q` or `:q<CR>`, I mean <kbd>`Esc`</kbd>`:q`<kbd>`Enter`</kbd>

For example, when I write `:text<CR>` or `:text`
1. Press <kbd>Esc</kbd> to enter <kbd>Normal</kbd> (or Command) mode.

2. Type `:`

3. Type whichever command `text` in placeholder shown in instruction. 

4. `<CR>` = Press <kbd>Enter</kbd>
> <kbd>Enter</kbd> is needed to execute the command indicated after `:` and
> before <kbd>Enter</kbd> or `<CR>`

Press <kbd>Key</kbd> together when <kbd>Key</kbd> are connected with `-`.

- <kbd>ctrl</kbd>-<kbd>w</kbd>-<kbd>k</kbd>


Press <kbd>Key</kbd> separately when <kbd>Key</kbd> are connected with or without `+`.
- <kbd>10</kbd> + <kbd>G</kbd> can be <kbd>Esc</kbd>, then type `:10G` <kbd>Enter</kbd>
- <kbd>Esc</kbd><kbd>g</kbd><kbd>g</kbd>  can be <kbd>Esc</kbd>, then type `:gg` + <kbd>Enter</kbd>


## Modes in Vi or Vim 
Modes in Vi or Vim 
- Command mode = <kbd>Normal</kbd> mode = <kbd>Esc</kbd>

- <kbd>Insert</kbd> mode = To insert text to file = <kbd>Esc</kbd><kbd>i</kbd>

- <kbd>Visual</kbd> mode = Selection of text by row or line = <kbd>Esc</kbd><kbd>v</kbd>

- <kbd>V-Block</kbd> mode = Selection of text by columns or rectangular regions = <kbd>Esc</kbd><kbd>ctrl</kbd>+<kbd>v</kbd>

- <kbd>V-Line></kbd> mode = Selection of full row or line = <kbd>Esc</kbd><kbd>shift</kbd>+<kbd>v</kbd>

> <kbd>Normal</kbd>, <kbd>Insert</kbd>, <kbd>Visual</kbd>, <kbd>V-Block</kbd>, and <kbd>V-Line</kbd> are not keys but to present `vi` modes in the editor

> <kbd>Visual</kbd>, <kbd>V-Block</kbd>, and <kbd>V-Line</kbd> are types of <kbd>Visual</kbd> modes.

## Basic Commands

> All of these basic commands starts in <kbd>Normal</kbd> mode. 

> Press <kbd>Esc</kbd> first to enter in <kbd>Normal</kbd> mode.

### Insert text

> These commands transition from <kbd>Normal</kbd> mode to <kbd>Insert</kbd>

- <kbd>a</kbd> = Append text following current cursor position

- <kbd>A</kbd> = Append text to the end of current line

- <kbd>i</kbd> = Insert text before the current cursor position

- <kbd>I</kbd> = Insert text at the beginning of the cursor line

- <kbd>o</kbd> = Open a new line following the current line and insert text

- <kbd>O</kbd> = Open a new line above the current line and insert text




> Vi starts the editor in <kbd>Normal</kbd> mode.

## Workflow of Editing a file

1. On the terminal, `vi filename`.

> `vi` = path to `vi`, `vim`, or `gvim`, etc. 

> `filename` = path of file to be editied in `vi`.  

2. Press <kbd>Esc</kbd>

> Remove any previous command and enter into <kbd>Normal</kbd> (or Command)
> mode.

3. Type `i` to switch to <kbd>Insert</kbd> mode

4. Press <kbd>Esc</kbd>

> Remove any previous command and enter into <kbd>Normal</kbd> (or Command)
> mode.

5. Type `:wq<CR>` to write and quit (exit) vim.
> `w` = write
> `q` = quit (Exit) 





## File Manipulation Commands

- Write (Save) file =  `:w`

- Refresh file = `:e` 

- Load and edit file to current workspace = `:e filename`
> where `filename` is the path to file 

- Read file to current workspace = `:r filename` 
> where `filename` is the path to file

## Exit Command

- Write file and quit editor = `:wq` + <kbd>Enter</kbd>
> Same command with <kbd>Esc</kbd><kbd>Z</kbd><kbd>Z</kbd> 


- Write file and quit editor with no warning = `:wq!` + <kbd>Enter</kbd>

- Quit file = `:q` + <kbd>Enter</kbd>
> Warning is printed if a modified file has not been saved. 



## Movements

Movements are in <kbd>Normal</kbd> mode.

Always press <kbd>Esc</kbd> first.

### Move cursor
> Always press <kbd>Esc</kbd> first.

up = <kbd>k</kbd> 

down = <kbd>j</kbd>

left = <kbd>h</kbd>

right = <kbd>l</kbd> 

### Move cursor by word
>  Always press <kbd>Esc</kbd> first.

end of word = <kbd>e</kbd>

right a word = <kbd>w</kbd> 

left a word = <kbd>b</kbd>

right 5 words = <kbd>5</kbd> + <kbd>w</kbd>

right to nearest "z" character = <kbd>f</kbd> + <kbd>z</kbd>

left to nearest "z" character = <kbd>F</kbd> + <kbd>z</kbd>

### Move to specific file location
>  Always press <kbd>Esc</kbd> first.

beginning of file = <kbd>gg</kbd>

end of file = <kbd>shift</kbd> + <kbd>g</kbd>

beginning of non-whitespace part of line  = <kbd>^</kbd>

beginning of line = <kbd>0</kbd> (Enter number 0)

end of line = <kbd>$</kbd>



## Search and Replace

Search "text" = <kbd>/</kbd> + `text`(type the text you want to search) + <kbd>Enter</kbd>
- Find next <kbd>n</kbd>
- Find previous <kbd>N</kbd> or <kbd>shift</kbd> + <kbd>n</kbd>

Turn off hightling (after a search) = `:noh`

Find next instant of a word that your cursor is over = <kbd>\*</kbd>

Search and replace from current line to end of file = `:,$s/search/replace/gc`
> `,$` = current line to `$` end of file
> `search` = Replace `search` with the text to search
> `replace` = Replace `replace` with the text to be replace with

## Undo a Command

Undo = <kbd>u</kbd>

Redo = <kbd>ctrl</kbd> + <kbd>r</kbd>

## View Directory and File Explorer 

Type `:S` (**S** is uppercase s)
> This will split the window and open up a file explorer. Use the key to select
> directories or to open file


## Split Window Editing

Type `:sp ` followed by a file name.

Go to window above = <kbd>ctrl</kbd> + <kbd><w</kbd> + <kbd>k</kbd> (Press all
keys at the same time)

Go to window below = <kbd>ctrl</kbd> + <kbd><w</kbd> + <kbd>k</kbd>


## Shell (Exit temporary to a shell)

Type `:sh` 

To come back to VIM from the shell type `exit`. 


## Relative number lines 

Put the following in your `~/.vimrc`:
```vi
set number           " Display line number 
set relativenumber   " Display relative line number from current
```

Or in the vi editor

First, press <kbd>Esc</kbd> to enter <kbd>Normal</kbd> mode.

```
:set number<CR>
:set relativenumber<CR>
```
> where `<CR>` is <kbd>Enter</kbd>


Operations based on relative line numbers:

- Move 4 lines above current line = <kbd>4</kbd> + <kbd>k<kbd>

- Move 10 lines below current line = <kbd>10</kbd> + <kbd>j</kbd>

- Indent current line and 2 lines below = <kbd>></kbd> + </kbd>2</kbd> + <kbd>j</kbd>

You still can use absolute number to move:

- Move to 899th line = <kbd>899</kbd> + <kbd>G</kbd> or `:899<CR>` 

## How to copy 

In `Vi`, yank is copy. 

Yank (or copy) operation must be in <kbd>Normal</kbd> mode. 

Yank is presented by command `y` or <kbd>y</kbd>

In <kbd>Normal</kbd> mode, yank = <kbd>y</kbd> + <kbd>Any motion</kbd>

`\n` = newline character at the end

Always enter <kbd>Normal</kbd> mode first = Press <kbd>Esc</kbd>

Yank (or copy) current word 
- (excludes surrounding space) = <kbd>y</kbd><kbd>i</kbd><kbd>w</kbd>
- (includes surrounding space) = <kbd>y</kbd><kbd>a</kbd><kbd>w</kbd>

Yank (or copy) current cursor 
- until before character `x` = <kbd>y</kbd><kbd>t</kbd><kbd>x</kbd>

Yank (or copy) lines
- current line including `\n` - <kbd>y</kbd><kbd>y</kbd>

- current cusor to end of line = <kbd>y</kbd><kbd>$</kbd>

- n lines including current line = <kbd>n</kbd><kbd>y</kbd><kbd>y</kbd>
    - 3 lines including current line = <kbd>3</kbd><kbd>y</kbd><kbd>y</kbd>

- current line to end of file = <kbd>y</kbd><kbd>G</kbd>

- current line to nth current line = <kbd>y</kbd><kbd>n</kbd><kbd>G</kbd>
    - current line to 6th current line = <kbd>y</kbd><kbd>6</kbd><kbd>G</kbd>

## How to paste

Paste uses <kbd>p</kbd> operation

Open up a line above and paste = <kbd>shift</kbd>+<kbd>p</kbd>

## How to delete

- Delete characters at current cursor =  <kbd>Esc</kbd> + <kbd>x</kbd>

- Delete n characters from current cursor = <kbd>Esc</kbd> + <kbd>n</kbd> + <kbd>x</kbd>
> where <kbd>n</kbd> can be any number <kbd>1</kbd>, <kbd>2</kbd>, ....,
> <kbd>n</kbd> 

- Delete 4 characters from current cursor = <kbd>Esc</kbd> + <kbd>4</kbd> + <kbd>x</kbd>

- Delete current line = <kbd>Esc</kbd> + <kbd>d</kbd> + <kbd>d</kbd>

- Delete n lines from current cursor = <kbd>Esc</kbd> + <kbd>n</kbd> + <kbd>d</kbd> + <kbd>d</kbd>

> where <kbd>n</kbd> can be any number <kbd>1</kbd>, <kbd>2</kbd>, ....,
> <kbd>n</kbd> 

- Delete current lines from end of file= <kbd>Esc</kbd> + <kbd>d</kbd> + <kbd>G</kbd>

- Delete 3 lines from current cursor = <kbd>Esc</kbd> + <kbd>3</kbd> + <kbd>d</kbd> + <kbd>d</kbd>

- Delete from current line to nth line = <kbd>Esc</kbd> + <kbd>d</kbd> + <kbd>n</kbd> + <kbd>G</kbd>
- Delete from current line to 3th line = <kbd>Esc</kbd> + <kbd>d</kbd> + <kbd>3</kbd> + <kbd>G</kbd>


## How to go to nth line

- Go to nth line = <kbd>Esc</kbd> + <kbd>n</kbd> + <kbd>G</kbd>
> where <kbd>n</kbd> can be any number <kbd>1</kbd>, <kbd>2</kbd>, ....,
> <kbd>n</kbd> 


- Go to 5th line = <kbd>Esc</kbd> + <kbd>5</kbd> + <kbd>G</kbd>

- Go to 10th line = <kbd>Esc</kbd> + <kbd>10</kbd> + <kbd>G</kbd>

## How to move to end of the line?

- Move to end of current line = <kbd>A</kbd> (or <kbd>shift</kbd> + <kbd>a</kbd>)

- Move to end of last line in file = <kbd>G</kbd> (or <kbd>shift</kbd> + <kbd>g</kbd>)

## How to insert an opening line below or after current line in vim?

- Insert new line above current line = <kbd>O</kbd> (or <kbd>shift</kbd> + <kbd>o</kbd>)

- Insert new line below current line = <kbd>o</kbd>

> The letter `O` or `o` from the word Orange. Not to be confused with zero 0. 


## References 

- [Things About Vim I Wish I Knew Earlier](https://blog.petrzemek.net/2016/04/06/things-about-vim-i-wish-i-knew-earlier/)

- [Simple VIM Reference](https://simpletutorials.com/c/vim/uldvdk5l/simple-vim-reference)

- [Vim Editor Commands](https://simpletutorials.com/c/vim/uldvdk5l/simple-vim-reference)
