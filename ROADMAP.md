## Custom commands

* `gh` - show the hover tooltip.
* `gb` - add an additional cursor at the next place that matches `*`.

## Left-right motions

Status | Command | Description
---|--------|------------
:white_check_mark:   |:1234:  h	| 	left (also: CTRL-H, BS, or Left key)
:white_check_mark:   |:1234:  l	| 	right (also: Space or Right key)
:white_check_mark:   |   0		| to first character in the line (also: Home key)
:white_check_mark:   |   ^		| to first non-blank character in the line
:white_check_mark:   |:1234:  $	| to the last character in the line (N-1 lines lower) (also: End key)
:white_check_mark:   |   g0		| to first character in screen line (differs from "0" when lines wrap)
:white_check_mark:   |   g^		| to first non-blank character in screen line (differs from "^" when lines wrap)
:white_check_mark:   |:1234:  g$    	| to last character in screen line (differs from "$" when lines wrap)
:white_check_mark:   |   gm		| to middle of the screen line
:white_check_mark:   |:1234:  \|	| to column N (default: 1)
:white_check_mark:   |:1234:  f{char}	| to the Nth occurrence of {char} to the right
:white_check_mark:   |:1234:  F{char}	| to the Nth occurrence of {char} to the left
:white_check_mark:   |:1234:  t{char}	| till before the Nth occurrence of {char} to the right
:white_check_mark:   |:1234:  T{char}	| till before the Nth occurrence of {char} to the left
:white_check_mark:   |:1234:  ;	| repeat the last "f", "F", "t", or "T" N times
:white_check_mark:   |:1234:  ,	| repeat the last "f", "F", "t", or "T" N times in opposite direction

## Up-down motions

Status | Command | Description
---|--------|------------
:white_check_mark:   | :1234:  k		| up N lines (also: CTRL-P and Up)
:white_check_mark:   | :1234:  j		| up N lidown N lines (also: CTRL-J, CTRL-N, NL, and Down)
:white_check_mark:   | :1234:  -		| up N lines, on the first non-blank character
:white_check_mark:   | :1234:  +		| down N lines, on the first non-blank character (also: CTRL-M and CR)
:white_check_mark:   | :1234:  _		| down N-1 lines, on the first non-blank character
:white_check_mark:   | :1234:  G		| goto line N (default: last line), on the first non-blank character
:white_check_mark:   | :1234:  gg		| goto line N (default: first line), on the first non-blank character
:white_check_mark:   | :1234:  %		| goto line N percentage down in the file; N must be given, otherwise it is the |%| command
:white_check_mark:   | :1234:  gk		| up N screen lines (differs from "k" when line wraps)
:white_check_mark:   | :1234:  gj		| own N screen lines (differs from "j" when line wraps)

## Text object motions

Status | Command | Description
---|--------|------------
:white_check_mark:   | :1234:  w		| N words forward
:white_check_mark:   | :1234:  W		| N blank-separated |WORD|s forward
:white_check_mark:   | :1234:  e		| N words forward to the end of the Nth word
:white_check_mark:   | :1234:  E		| N words forward to the end of the Nth blank-separated |WORD|
:white_check_mark:   | :1234:  b		| N words backward
:white_check_mark:   | :1234:  B		| N blank-separated |WORD|s backward
:white_check_mark:   | :1234:  ge		| N words backward to the end of the Nth word
:white_check_mark:   | :1234:  gE		| N words backward to the end of the Nth blank-separated |WORD|
:white_check_mark:   | :1234:  )		| N sentences forward
:white_check_mark:   | :1234:  (		| N sentences backward
:white_check_mark:   | :1234:  }		| N paragraphs forward
:white_check_mark:   | :1234:  {		| N paragraphs backward
:white_check_mark:   | :1234:  ]]		| N sections forward, at start of section
:white_check_mark:   | :1234:  [[		| N sections backward, at start of section
:white_check_mark:   | :1234:  ][		| N sections forward, at end of section
:white_check_mark:   | :1234:  []		| N sections backward, at end of section
:white_check_mark:   | :1234:  [(		| N times back to unclosed '('
:white_check_mark:   | :1234:  [{		| N times back to unclosed '{'
:white_check_mark:   | :1234:  ])		| N times forward to unclosed ')'
:white_check_mark:   | :1234:  ]}		| N times forward to unclosed '}'

## Pattern searches

Status | Command | Description | Note
---|--------|------------|------------------
:white_check_mark: :star: | :1234: `/{pattern}[/[offset]]<CR>` | search forward for the Nth occurrence of {pattern} | Currently we only support JavaScript Regex but not Vim's in-house Regex engine.
:white_check_mark: :star: | :1234: `?{pattern}[?[offset]]<CR>` | search backward for the Nth occurrence of {pattern} | Currently we only support JavaScript Regex but not Vim's in-house Regex engine.
:white_check_mark: | :1234: * | search forward for the identifier under the cursor
:white_check_mark: | :1234: # | search backward for the identifier under the cursor
:white_check_mark: | gd | goto local declaration of identifier under the cursor

## Marks and motions

Status | Command | Description
---|--------|------------------------------
:white_check_mark: |    m{a-zA-Z}	       |  mark current position with mark {a-zA-Z}
:white_check_mark:|   `{a-z}	       |  go to mark {a-z} within current file
:white_check_mark:|    `{A-Z}	       |  go to mark {A-Z} in any file
:white_check_mark:|    `{0-9}	       |  go to the position where Vim was previously exited
:white_check_mark: |    ``		       |  go to the position before the last jump
:white_check_mark: |    `.		       |  go to the position of the last change in this file
:white_check_mark: |    '.		       |  go to the position of the last change in this file

## Various motions

Status | Command | Description
---|--------|------------------------------
:white_check_mark:    |   %		        | find the next brace, bracket, comment, or "#if"/ "#else"/"#endif" in this line and go to its match
:white_check_mark:    |:1234:  H		        | go to the Nth line in the window, on the first non-blank
:white_check_mark:    |        M		        | go to the middle line in the window, on the first non-blank
:white_check_mark:    |:1234:  L		        | go to the Nth line from the bottom, on the first non-blank

## Inserting text

Status | Command | Description
---|--------|------------------------------
:white_check_mark:    | :1234:  a	| append text after the cursor (N times)
:white_check_mark:    | :1234:  A	| append text at the end of the line (N times)
:white_check_mark:    | :1234:  i	| insert text before the cursor (N times) (also: Insert)
:white_check_mark:    | :1234:  I	| insert text before the first non-blank in the line (N times)
:white_check_mark:    | :1234:  gI	| insert text in column 1 (N times)
:white_check_mark:    | gi	| insert at the end of the last change
:white_check_mark:    | :1234:  o	| open a new line below the current line, append text (N times)
:white_check_mark:    | :1234:  O	| open a new line above the current line, append text (N times)

in Visual block mode:

Status | Command | Description
---|--------|------------------------------
:white_check_mark:| I	| insert the same text in front of all the selected lines
:white_check_mark:| A	| append the same text after all the selected lines

## Deleting text

Status | Command | Description
---|--------|------------------------------
:white_check_mark:    | :1234:  x		| delete N characters under and after the cursor
:white_check_mark:    | :1234:  Del	    | delete N characters under and after the cursor
:white_check_mark:    | :1234:  X		| delete N characters before the cursor
:white_check_mark:    | :1234:  d{motion}	| delete the text that is moved over with {motion}
:white_check_mark:    |    {visual}d	| delete the highlighted text
:white_check_mark:    | :1234:  dd	| 	delete N lines
:white_check_mark:    | :1234:  D		| delete to the end of the line (and N-1 more lines)
:white_check_mark:    | :1234:  J		| join N-1 lines (delete EOLs)
:white_check_mark:    |    {visual}J	| join the highlighted lines
:white_check_mark:    | :1234:  gJ	| 	like "J", but without inserting spaces
:white_check_mark:|   {visual}gJ	| like "{visual}J", but without inserting spaces
:white_check_mark:| :[range]d [x]	| delete [range] lines [into register x]

## Copying and moving text

* We don't support read only registers.

Status | Command | Description
---|--------|-------------|-----------------
:warning: | "{char}	        | use register {char} for the next delete, yank, or put 
:white_check_mark:   | "*	        | use register `*` to access system clipboard
:white_check_mark:   | :reg		| show the contents of all registers
:white_check_mark:   | :reg {arg}	        | show the contents of registers mentioned in {arg}
:white_check_mark:   | :1234:  y{motion}	| yank the text moved over with {motion} into a register
:white_check_mark:   |    {visual}y	| yank the highlighted text into a register
:white_check_mark:   | :1234:  yy		| yank N lines into a register
:white_check_mark:   | :1234:  Y		| yank N lines into a register
:white_check_mark:   | :1234:  p		| put a register after the cursor position (N times)
:white_check_mark:   | :1234:  P		| put a register before the cursor position (N times)
:white_check_mark:   | :1234:  ]p		| like p, but adjust indent to current line
:white_check_mark:   | :1234:  [p		| like P, but adjust indent to current line
:white_check_mark:   | :1234:  gp		| like p, but leave cursor after the new text
:white_check_mark:   | :1234:  gP		| like P, but leave cursor after the new text

## Changing text

Status | Command | Description | Note
---|--------|------------|------------------
:white_check_mark: | :1234:  r{char}	| replace N characters with {char}
:arrow_down: | :1234:  gr{char}	| replace N characters without affecting layout
:white_check_mark: :star: | :1234:  R		| enter Replace mode (repeat the entered text N times) | {count} is not supported
:arrow_down: | :1234:  gR		| enter virtual Replace mode: Like Replace mode but without affecting layout
:white_check_mark:|  {visual}r{char} | in Visual block, visual, or visual line modes: Replace each char of the selected text with {char}

(change = delete text and enter Insert mode)

Status | Command | Description
---|--------|------------------------------
:white_check_mark:  | :1234:  c{motion}	| change the text that is moved over with {motion}
:white_check_mark:  | {visual}c	| change the highlighted text
:white_check_mark:  | :1234:  cc	| 	change N lines
:white_check_mark:  | :1234:  S		| change N lines
:white_check_mark:  | :1234:  C		| change to the end of the line (and N-1 more lines)
:white_check_mark:  | :1234:  s		| change N characters
:white_check_mark:  | {visual}c	| in Visual block mode: Change each of the selected lines with the entered text
:white_check_mark:  |    {visual}C	| in Visual block mode: Change each of the selected lines until end-of-line with the entered text
:white_check_mark:	| switch case for highlighted text
:white_check_mark:  |    {visual}u	| make highlighted text lowercase
:white_check_mark:  |    {visual}U	| make highlighted text uppercase
:white_check_mark:  |    g~{motion}     | switch case for the text that is moved over with {motion}
:white_check_mark:  |    gu{motion}     | make the text that is moved over with {motion} lowercase
:white_check_mark:  |    gU{motion}     | make the text that is moved over with {motion} uppercase
:arrow_down:    |    {visual}g?     | perform rot13 encoding on highlighted text
:arrow_down:    |    g?{motion}     | perform rot13 encoding on the text that is moved over with {motion}
:white_check_mark:    | :1234:  <{motion}	| move the lines that are moved over with {motion} one shiftwidth left
:white_check_mark:    | :1234:  <<	|	move N lines one shiftwidth left
:white_check_mark:    | :1234:  >{motion}	|  move the lines that are moved over with {motion} one shiftwidth right
:white_check_mark:    | :1234:  >>	|	move N lines one shiftwidth right
:white_check_mark:| :1234:  gq{motion}|	format the lines that are moved over with {motion} to 'textwidth' length

## Visual mode

Status | Command | Description
---|--------|------------------------------
:white_check_mark:   | v		| start highlighting characters
:white_check_mark:   | V		| start highlighting linewise
:white_check_mark:| o		| exchange cursor position with start of highlighting
:white_check_mark:| gv		| start highlighting on previous visual area
:white_check_mark:   | v		| highlight characters or stop highlighting
:white_check_mark:   | V		| highlight linewise or stop highlighting

## Text objects (only in Visual mode or after an operator)

Status | Command | Description
---|--------|------------------------------
:white_check_mark:    | :1234:  aw	| Select "a word"
:white_check_mark:    | :1234:  iw	| Select "inner word"
:white_check_mark:    | :1234:  aW	| Select "a |WORD|"
:white_check_mark:    | :1234:  iW	| Select "inner |WORD|"
:white_check_mark:    | :1234:  as	| Select "a sentence"
:white_check_mark:    | :1234:  is	| Select "inner sentence"
:white_check_mark:    | :1234:  ap	| Select "a paragraph"
:white_check_mark:    | :1234:  ip	| Select "inner paragraph"
:white_check_mark:    | :1234:  a], a[    | select '[' ']' blocks
:white_check_mark:    | :1234:  i], i[    | select inner  '[' ']' blocks
:white_check_mark:    | :1234:  ab, a(, a)	| Select "a block" (from "[(" to "])")
:white_check_mark:    | :1234:  ib, i), i(	| Select "inner block" (from "[(" to "])")
:white_check_mark:    | :1234:  a>, a<	| Select "a &lt;&gt; block"
:white_check_mark:    | :1234:  i>, i<	| Select "inner <> block"
:white_check_mark:    | :1234:  aB, a{, a}	| Select "a Block" (from "[{" to "]}")
:white_check_mark:    | :1234:  iB, i{, i}	| Select "inner Block" (from "[{" to "]}")
:white_check_mark:    | :1234:  at	| Select "a tag block" (from &lt;aaa&gt; to &lt;/aaa&gt;)
:white_check_mark:    | :1234:  it	| Select "inner tag block" (from &lt;aaa&gt; to &lt;/aaa&gt;)
:white_check_mark:    | :1234:  a'	| Select "a single quoted string"
:white_check_mark:    | :1234:  i'	| Select "inner single quoted string"
:white_check_mark:    | :1234:  a"	| Select "a double quoted string"
:white_check_mark:    | :1234:  i"	| Select "inner double quoted string"
:white_check_mark:    | :1234:  a`	| Select "a backward quoted string"
:white_check_mark:    | :1234:  i`	| Select "inner backward quoted string"

## Repeating commands

Status | Command | Description | Note
---|--------|--------------|----------------
:white_check_mark: :star:  | :1234:  .		 | repeat last change (with count replaced with N) | Content changes that don't happen under cursor can not be repeated.
:white_check_mark:|    q{a-z}	         | record typed characters into register {a-z}
:white_check_mark:|    q		 | stop recording

## External commands

Status | Command | Description
---|--------|-----------------
:arrow_down: | :sh[ell] | start a shell
:arrow_down: | :!{command} | execute {command} with a shell
:arrow_down: | K | lookup keyword under the cursor with 'keywordprg' program (default: "man")

## Editing a file

Status | Command | Description | Note
---|--------|------------------|-----------
:white_check_mark: :star:   | :e[dit] {file}  | Edit {file}. | We will open file in a new Tab of current Grouped Editor instead of opening in current tab.

## Multi-window commands

Status | Command | Description | Note
---|--------|-----------------|-------------
:white_check_mark: :star: | :e[dit] {file}  | Edit {file}. | We will open file in a new Tab of current Grouped Editor instead of opening in current tab.
:white_check_mark: :star: | &lt;ctrl-w&gt; hl  | Switching between windows. | As we don't have the concept of Window in VS Code, we are mapping these commands to switching between Grouped Editors.
:white_check_mark: :star: | :vsp {file}  | Split vertically current window in two. | VS Code only supports three vertical window at most and that's the limitation of this command.
:white_check_mark: :star:  | :vne[w] | Create a new window vertically and start editing an empty file in it. | VS Code only supports three vertical window at most and that's the limitation of this command.

## Folding

Status | Command | Description
---|--------|------------------------------
:white_check_mark: | zo | Open one fold under the cursor.When a count is given, that many folds deep will be opened.
:white_check_mark: | zO | Open all folds under the cursor recursively.
:white_check_mark: | zc | Close one fold under the cursor.  When a count is given, that many folds deep are closed.
:white_check_mark:| zC | Close all folds under the cursor recursively.
:white_check_mark: | zM | Close all folds: set 'foldlevel' to 0. 'foldenable' will be set.
:white_check_mark: | zR | Open all folds.  This sets 'foldlevel' to highest fold level.
