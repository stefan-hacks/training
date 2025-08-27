# Exhaustive Vim Editor Commands Reference

## Table of Contents
1. [Normal Mode](#normal-mode)
2. [Insert Mode](#insert-mode)
3. [Visual Mode](#visual-mode)
4. [Command-Line Mode](#command-line-mode)
5. [Replace Mode](#replace-mode)
6. [Operator-Pending Mode](#operator-pending-mode)
7. [Terminal-Job Mode](#terminal-job-mode)
8. [Select Mode](#select-mode)
9. [Ex Mode](#ex-mode)

---

## Normal Mode

### Movement Commands

| Command | Description | Example |
|---------|-------------|---------|
| `h` | Move left | `5h` moves left 5 characters |
| `j` | Move down | `10j` moves down 10 lines |
| `k` | Move up | `5k` moves up 5 lines |
| `l` | Move right | `3l` moves right 3 characters |
| `0` | Move to start of line | `0` moves to column 0 |
| `^` | Move to first non-blank character | `^` moves to first non-whitespace |
| `$` | Move to end of line | `$` moves to line end |
| `g_` | Move to last non-blank character | `g_` moves to last non-whitespace |
| `+` | Move to first char of next line | `5+` moves down 5 lines |
| `-` | Move to first char of previous line | `3-` moves up 3 lines |
| `_` | Move to first non-blank char (alternative) | `_` moves to first non-whitespace |
| `\|` | Move to column | `30\|` moves to column 30 |
| `%` | Jump to matching bracket | `%` on `(` jumps to `)` |
| `(` | Move to previous sentence | `3(` moves back 3 sentences |
| `)` | Move to next sentence | `2)` moves forward 2 sentences |
| `{` | Move to previous paragraph | `{` moves to previous paragraph |
| `}` | Move to next paragraph | `}` moves to next paragraph |
| `[[` | Move to previous section | `[[` moves to previous section |
| `]]` | Move to next section | `]]` moves to next section |
| `[]` | Move to end of previous section | `[]` moves to end of previous section |
| `][` | Move to end of next section | `][` moves to end of next section |
| `gE` | Move to end of previous WORD | `gE` moves to end of previous WORD |
| `E` | Move to end of WORD | `E` moves to end of current WORD |
| `e` | Move to end of word | `e` moves to end of current word |
| `b` | Move backward by word | `2b` moves back 2 words |
| `B` | Move backward by WORD | `5B` moves back 5 WORDS |
| `w` | Move forward by word | `3w` moves forward 3 words |
| `W` | Move forward by WORD | `4W` moves forward 4 WORDS |
| `ge` | Move to end of previous word | `ge` moves to end of previous word |
| `gg` | Go to first line | `gg` jumps to file start |
| `G` | Go to line | `50G` jumps to line 50 |
| `H` | Move to top of screen | `5H` moves to 5th line from top |
| `M` | Move to middle of screen | `M` moves to middle line |
| `L` | Move to bottom of screen | `3L` moves to 3rd line from bottom |
| `Ctrl+B` | Scroll up one screen | `Ctrl+B` scrolls up |
| `Ctrl+F` | Scroll down one screen | `Ctrl+F` scrolls down |
| `Ctrl+U` | Scroll up half screen | `Ctrl+U` scrolls up half |
| `Ctrl+D` | Scroll down half screen | `Ctrl+D` scrolls down half |
| `Ctrl+E` | Scroll line down | `Ctrl+E` moves screen down |
| `Ctrl+Y` | Scroll line up | `Ctrl+Y` moves screen up |
| `Ctrl+O` | Jump to older position | `Ctrl+O` goes back in jump list |
| `Ctrl+I` | Jump to newer position | `Ctrl+I` goes forward in jump list |
| `Ctrl+^` | Edit alternate file | `Ctrl+^` switches to previous file |
| `Ctrl+W` | Window commands prefix | `Ctrl+W s` splits window |
| `z Enter` | Scroll line to top | `z Enter` moves cursor line to top |
| `z.` | Scroll line to center | `z.` centers screen on cursor |
| `z-` | Scroll line to bottom | `z-` moves cursor line to bottom |
| `zt` | Scroll line to top | `zt` scrolls cursor line to top |
| `zz` | Scroll line to center | `zz` centers screen on cursor |
| `zb` | Scroll line to bottom | `zb` scrolls cursor line to bottom |
| `'` | Jump to mark line | `'a` jumps to line of mark a |
| `` ` `` | Jump to mark position | `` `a `` jumps to exact mark a position |
| `f` | Find forward in line | `f x` finds next "x" in line |
| `F` | Find backward in line | `F x` finds previous "x" in line |
| `t` | Till forward in line | `t x` moves to before next "x" |
| `T` | Till backward in line | `T x` moves to after previous "x" |
| `;` | Repeat last `f`, `F`, `t`, `T` | `f x ;` repeats `f x` forward |
| `,` | Repeat last `f`, `F`, `t`, `T` in reverse | `f x ,` repeats `f x` backward |
| `/` | Search forward | `/foo` searches "foo" |
| `?` | Search backward | `?bar` searches "bar" backward |
| `n` | Repeat last search | `n` repeats `/foo` forward |
| `N` | Repeat search in opposite direction | `N` after `/foo` searches backward |
| `*` | Search word under cursor forward | `*` finds next occurrence of word |
| `#` | Search word under cursor backward | `#` finds previous occurrence of word |
| `g*` | Search partial word under cursor forward | `g*` finds next partial match |
| `g#` | Search partial word under cursor backward | `g#` finds previous partial match |
| `gd` | Go to local declaration | `gd` jumps to local variable declaration |
| `gD` | Go to global declaration | `gD` jumps to global variable declaration |
| `gf` | Go to file under cursor | `gf` opens file under cursor |
| `gF` | Go to file under cursor with line number | `gF` opens file:line under cursor |
| `g;` | Go to last changed position | `g;` jumps to previous change |
| `g,` | Go to newer changed position | `g,` jumps to next change |
| `]` | Section forward movement | `]m` jumps to next method start |
| `[` | Section backward movement | `[m` jumps to previous method start |

### Editing Commands

| Command | Description | Example |
|---------|-------------|---------|
| `a` | Append after cursor | `a` inserts after cursor |
| `A` | Append at end of line | `A` adds text after last char |
| `i` | Insert before cursor | `i` inserts at cursor |
| `I` | Insert before first non-blank char | `I` inserts at line start |
| `o` | Open new line below | `o` inserts line below cursor |
| `O` | Open new line above | `O` inserts line above cursor |
| `r` | Replace single char | `r x` replaces char with 'x' |
| `R` | Enter Replace mode | `R` overwrites existing text |
| `s` | Substitute char | `s` deletes char and inserts |
| `S` | Substitute entire line | `S` deletes line and enters Insert mode |
| `c` | Change (operator) | `c w` changes word |
| `C` | Change from cursor to end of line | `C` deletes and enters Insert mode |
| `d` | Delete (operator) | `d $` deletes to line end |
| `D` | Delete to end of line | `D` deletes from cursor to line end |
| `x` | Delete char under cursor | `x` deletes current character |
| `X` | Delete char before cursor | `X` deletes previous character |
| `y` | Yank (operator) | `y y` yanks current line |
| `Y` | Yank line | `Y` copies current line |
| `p` | Paste after cursor | `p` pastes after cursor |
| `P` | Paste before cursor | `P` pastes before cursor |
| `J` | Join lines | `J` merges current and next line |
| `gJ` | Join lines without space | `gJ` joins without adding space |
| `~` | Toggle case | `~` toggles case of character |
| `gu` | Make lowercase (operator) | `g u w` makes word lowercase |
| `gU` | Make uppercase (operator) | `g U w` makes word uppercase |
| `g~` | Toggle case (operator) | `g ~ w` toggles case of word |
| `>` | Indent (operator) | `> >` indents current line |
| `<` | De-indent (operator) | `< <` de-indents current line |
| `=` | Auto-indent (operator) | `= =` auto-indents current line |
| `Ctrl+A` | Increment number | `Ctrl+A` on 5 changes to 6 |
| `Ctrl+X` | Decrement number | `Ctrl+X` on 5 changes to 4 |
| `.` | Repeat last change | `dd .` deletes another line |
| `m` | Mark position | `m a` marks cursor as 'a' |
| `"` | Specify register | `"a y y` yanks line to register a |
| `@` | Execute register | `@a` executes macro in register a |
| `@@` | Repeat last executed register | `@@` repeats last macro |
| `q` | Record macro | `q a` starts recording to register a |
| `Q` | Enter Ex mode | `Q` switches to Ex mode |
| `v` | Enter Visual mode | `v` selects characters |
| `V` | Enter Visual line mode | `V` selects lines |
| `Ctrl+V` | Enter Visual block mode | `Ctrl+V` selects block |
| `Ctrl+Q` | Enter Visual block mode (alternative) | `Ctrl+Q` selects block |
| `u` | Undo | `u` reverts last change |
| `Ctrl+R` | Redo | `Ctrl+R` redoes undone change |
| `U` | Undo changes on line | `U` reverts line changes |
| `Ctrl+W` | Window commands prefix | `Ctrl+W s` splits window |
| `z` | Scroll and fold commands | `z a` toggle fold |
| `gq` | Format lines | `g q q` format current line |
| `gw` | Format lines without moving cursor | `g w}` format to paragraph end |
| `:` | Enter Command-line mode | `:w` saves file |
| `!` | Filter through external command | `!}sort` sorts paragraph |
| `&` | Repeat last `:s` | `&` repeats last substitution |
| `Ctrl+]` | Jump to tag | `Ctrl+]` jumps to tag under cursor |
| `Ctrl+T` | Jump back from tag | `Ctrl+T` returns from tag jump |
| `Ctrl+Z` | Suspend Vim | `Ctrl+Z` backgrounds Vim |
| `Ctrl+[` | Escape (same as Esc) | `Ctrl+[` returns to Normal mode |
| `Ctrl+C` | Escape (similar to Esc) | `Ctrl+C` returns to Normal mode |
| `ZZ` | Save and quit | `ZZ` writes and exits |
| `ZQ` | Quit without saving | `ZQ` quits without saving |
| `g Ctrl+G` | Show cursor information | `g Ctrl+G` shows position info |

### Text Objects

| Command | Description | Example |
|---------|-------------|---------|
| `iw` | Inner word | `d i w` deletes inner word |
| `aw` | A word | `d a w` deletes word with space |
| `iW` | Inner WORD | `d i W` deletes inner WORD |
| `aW` | A WORD | `d a W` deletes WORD with space |
| `is` | Inner sentence | `d i s` deletes inner sentence |
| `as` | A sentence | `d a s` deletes sentence with space |
| `ip` | Inner paragraph | `d i p` deletes inner paragraph |
| `ap` | A paragraph | `d a p` deletes paragraph with space |
| `i"` | Inside double quotes | `d i "` deletes inside quotes |
| `a"` | Around double quotes | `d a "` deletes quotes and content |
| `i'` | Inside single quotes | `d i '` deletes inside single quotes |
| `a'` | Around single quotes | `d a '` deletes single quotes and content |
| `` i` `` | Inside backticks | `` d i ` `` deletes inside backticks |
| `` a` `` | Around backticks | `` d a ` `` deletes backticks and content |
| `i[` or `i]` | Inside brackets | `d i [` deletes inside brackets |
| `a[` or `a]` | Around brackets | `d a [` deletes brackets and content |
| `i(` or `i)` | Inside parentheses | `d i (` deletes inside parentheses |
| `a(` or `a)` | Around parentheses | `d a (` deletes parentheses and content |
| `i{` or `i}` | Inside braces | `d i {` deletes inside braces |
| `a{` or `a}` | Around braces | `d a {` deletes braces and content |
| `i<` or `i>` | Inside angle brackets | `d i <` deletes inside angle brackets |
| `a<` or `a>` | Around angle brackets | `d a <` deletes angle brackets and content |
| `it` | Inside tag | `d i t` deletes inside HTML tag |
| `at` | Around tag | `d a t` deletes HTML tag and content |
| `iB` | Inside block (same as `i{`) | `d i B` deletes inside block |
| `aB` | Around block (same as `a{`) | `d a B` deletes block and content |

---

## Insert Mode

### Basic Editing

| Command | Description | Example |
|---------|-------------|---------|
| `Ctrl+H` | Delete back one character | `Ctrl+H` equals backspace |
| `Ctrl+W` | Delete back one word | `Ctrl+W` deletes previous word |
| `Ctrl+U` | Delete back to start of line | `Ctrl+U` clears entered text |
| `Ctrl+T` | Indent current line | `Ctrl+T` adds indent |
| `Ctrl+D` | De-indent current line | `Ctrl+D` reduces indent |
| `Ctrl+I` | Insert tab | `Ctrl+I` inserts tab character |
| `Ctrl+V` | Insert next character literally | `Ctrl+V Esc` inserts escape character |
| `Ctrl+@` | Insert previously inserted text | `Ctrl+@` inserts last inserted text |
| `Ctrl+A` | Insert previously inserted text | `Ctrl+A` same as `Ctrl+@` |
| `Ctrl+R` | Insert from register | `Ctrl+R a` inserts register a |
| `Ctrl+O` | Execute one Normal command | `Ctrl+O d d` deletes line |
| `Ctrl+[` | Escape to Normal mode | `Ctrl+[` same as `<Esc>` |
| `Ctrl+C` | Escape to Normal mode | `Ctrl+C` similar to `<Esc>` |

### Completion Commands

| Command | Description | Example |
|---------|-------------|---------|
| `Ctrl+N` | Next completion match | `Ctrl+N` cycles completions |
| `Ctrl+P` | Previous completion match | `Ctrl+P` cycles back |
| `Ctrl+X` | Enter completion submode | |
| `Ctrl+X Ctrl+F` | File completion | `Ctrl+X Ctrl+F` completes filenames |
| `Ctrl+X Ctrl+I` | Include completion | `Ctrl+X Ctrl+I` completes from included files |
| `Ctrl+X Ctrl+]` | Tag completion | `Ctrl+X Ctrl+]` completes tags |
| `Ctrl+X Ctrl+D` | Definition completion | `Ctrl+X Ctrl+D` completes definitions |
| `Ctrl+X Ctrl+K` | Dictionary completion | `Ctrl+X Ctrl+K` completes from dictionary |
| `Ctrl+X Ctrl+L` | Whole line completion | `Ctrl+X Ctrl+L` completes whole lines |
| `Ctrl+X Ctrl+N` | Keyword completion (current file) | `Ctrl+X Ctrl+N` completes from current file |
| `Ctrl+X Ctrl+P` | Keyword completion (previous) | `Ctrl+X Ctrl+P` completes previous keywords |
| `Ctrl+X Ctrl+T` | Thesaurus completion | `Ctrl+X Ctrl+T` completes from thesaurus |
| `Ctrl+X Ctrl+U` | User completion | `Ctrl+X Ctrl+U` completes with user function |
| `Ctrl+X Ctrl+V` | Vim command completion | `Ctrl+X Ctrl+V` completes Vim commands |
| `Ctrl+X Ctrl+Y` | Omni completion | `Ctrl+X Ctrl+Y` completes with omni function |
| `Ctrl+X Ctrl+O` | Omni completion | `Ctrl+X Ctrl+O` completes with omni function |
| `Ctrl+X s` | Spelling suggestions | `Ctrl+X s` shows spelling suggestions |

### Special Inserts

| Command | Description | Example |
|---------|-------------|---------|
| `Ctrl+K` | Digraph insertion | `Ctrl+K o :` inserts ö |
| `Ctrl+R =` | Expression evaluation | `Ctrl+R =5+3` inserts 8 |
| `Ctrl+V {number}` | Insert character by code | `Ctrl+V 065` inserts 'A' |
| `Ctrl+V u {hex}` | Insert Unicode character | `Ctrl+V u 00E4` inserts 'ä' |
| `Ctrl+V x {hex}` | Insert hex character | `Ctrl+V x 41` inserts 'A' |
| `Ctrl+V o {octal}` | Insert octal character | `Ctrl+V o 101` inserts 'A' |

---

## Visual Mode

### Selection Commands

| Command | Description | Example |
|---------|-------------|---------|
| `v` | Character-wise Visual mode | `v` selects characters |
| `V` | Line-wise Visual mode | `V` selects lines |
| `Ctrl+V` | Block-wise Visual mode | `Ctrl+V` selects block |
| `gv` | Reselect previous visual area | `gv` reselects last selection |
| `o` | Move to other end of selection | `o` swaps cursor to other end |
| `O` | Move to other corner in block mode | `O` moves to other corner in block mode |
| `Ctrl+G` | Switch to Visual mode | `Ctrl+G` toggles Visual/Select mode |

### Editing in Visual Mode

| Command | Description | Example |
|---------|-------------|---------|
| `y` | Yank selection | `y` copies selected text |
| `d` | Delete selection | `d` cuts selected text |
| `c` | Change selection | `c` deletes and enters Insert mode |
| `x` | Delete selection | `x` same as `d` |
| `s` | Change selection | `s` same as `c` |
| `p` | Paste over selection | `p` replaces selection with register |
| `r` | Replace selection | `r x` replaces with 'x' |
| `~` | Toggle case selection | `~` swaps case of selected text |
| `u` | Make lowercase selection | `u` changes selected text to lowercase |
| `U` | Make uppercase selection | `U` changes selected text to uppercase |
| `J` | Join selected lines | `J` joins selected lines |
| `gJ` | Join selected lines without spaces | `gJ` joins without adding spaces |
| `>` | Indent selection | `>` shifts right |
| `<` | De-indent selection | `<` shifts left |
| `=` | Auto-indent selection | `=` auto-indents selection |
| `!` | Filter selection through command | `!}sort` sorts selected lines |
| `:` | Command on selection | `:s/foo/bar` substitutes in selection |
| `Ctrl+C` | Exit Visual mode | `Ctrl+C` returns to Normal mode |
| `Esc` | Exit Visual mode | `Esc` returns to Normal mode |
| `Ctrl+[` | Exit Visual mode | `Ctrl+[` returns to Normal mode |

---

## Command-Line Mode

### File Commands

| Command | Description | Example |
|---------|-------------|---------|
| `:e` | Edit file | `:e file.txt` opens file.txt |
| `:enew` | Edit new buffer | `:enew` creates new buffer |
| `:sp` | Split window and edit file | `:sp file.txt` splits and opens |
| `:vsp` | Vertical split and edit file | `:vsp file.txt` vertical split |
| `:w` | Write file | `:w` saves current file |
| `:w!` | Write file forcefully | `:w!` forces write |
| `:wa` | Write all buffers | `:wa` saves all files |
| `:wq` | Write and quit | `:wq` saves and exits |
| `:x` | Write and quit (if modified) | `:x` saves if modified and exits |
| `:q` | Quit | `:q` exits Vim |
| `:q!` | Quit without saving | `:q!` quits without saving |
| `:qa` | Quit all | `:qa` quits all windows |
| `:qa!` | Quit all without saving | `:qa!` quits all without saving |
| `:wqa` | Write all and quit all | `:wqa` saves all and quits |
| `:sav` | Save file as | `:sav newname.txt` saves as newname |
| `:r` | Read file | `:r file.txt` inserts file content |
| `:r!` | Read command output | `:r !ls` inserts ls output |

### Buffer Commands

| Command | Description | Example |
|---------|-------------|---------|
| `:b` | Switch to buffer | `:b 2` switches to buffer 2 |
| `:bd` | Delete buffer | `:bd` deletes current buffer |
| `:bd!` | Delete buffer forcefully | `:bd!` forces buffer delete |
| `:ba` | Edit all buffers | `:ba` edits all buffers |
| `:bn` | Next buffer | `:bn` goes to next buffer |
| `:bp` | Previous buffer | `:bp` goes to previous buffer |
| `:bl` | Last buffer | `:bl` goes to last buffer |
| `:bf` | First buffer | `:bf` goes to first buffer |
| `:bw` | Wipe out buffer | `:bw` removes buffer from list |
| `:b#` | Alternate buffer | `:b#` switches to previous buffer |
| `:ls` | List buffers | `:ls` shows all buffers |
| `:sb` | Split window and switch to buffer | `:sb 3` splits and goes to buffer 3 |

### Window Commands

| Command | Description | Example |
|---------|-------------|---------|
| `:sp` | Split window | `:sp` splits horizontally |
| `:vsp` | Vertical split | `:vsp` splits vertically |
| `:new` | New horizontal window | `:new` creates new window |
| `:vnew` | New vertical window | `:vnew` creates vertical window |
| `:close` | Close window | `:close` closes current window |
| `:only` | Keep only this window | `:only` closes other windows |
| `:hide` | Hide window | `:hide` hides current window |
| `:res` | Resize window | `:res 20` sets height to 20 |
| `:vertical res` | Resize window vertically | `:vertical res 80` sets width to 80 |
| `:wincmd` | Window command | `:wincmd k` moves to window above |

### Navigation Commands

| Command | Description | Example |
|---------|-------------|---------|
| `:e #` | Edit alternate file | `:e #` edits previous file |
| `:cd` | Change directory | `:cd /path` changes working directory |
| `:pwd` | Print working directory | `:pwd` shows current directory |
| `:marks` | Show marks | `:marks` lists all marks |
| `:jumps` | Show jump list | `:jumps` shows jump history |
| `:changes` | Show change list | `:changes` shows change history |

### Search and Replace

| Command | Description | Example |
|---------|-------------|---------|
| `:s` | Substitute | `:s/old/new` replaces first "old" |
| `:s/old/new/g` | Substitute all in line | `:s/old/new/g` replaces all in line |
| `:%s/old/new/g` | Substitute all in file | `:%s/old/new/g` replaces all in file |
| `:s/old/new/gc` | Substitute with confirmation | `:s/old/new/gc` confirms each replace |
| `:&` | Repeat last substitute | `:&` repeats last :s |
| `:~` | Repeat last substitute with flags | `:~` repeats last :s with flags |
| `:g` | Global command | `:g/foo/d` deletes lines with "foo" |
| `:v` | Inverted global | `:v/bar/d` deletes lines without "bar" |
| `:norm` | Execute Normal commands | `:%norm A;` appends ; to every line |

### Settings and Information

| Command | Description | Example |
|---------|-------------|---------|
| `:set` | Set option | `:set number` shows line numbers |
| `:set no` | Unset option | `:set nonumber` hides line numbers |
| `:set inv` | Invert option | `:set invnumber` toggles line numbers |
| `:set all` | Show all options | `:set all` displays all settings |
| `:set {option}?` | Show option value | `:set tabstop?` shows tabstop value |
| `:set {option}={value}` | Set option value | `:set tabstop=4` sets tab to 4 spaces |
| `:map` | Show mappings | `:map` displays Normal mode mappings |
| `:imap` | Show Insert mode mappings | `:imap` displays Insert mode mappings |
| `:vmap` | Show Visual mode mappings | `:vmap` displays Visual mode mappings |
| `:nmap` | Show Normal mode mappings | `:nmap` displays Normal mode mappings |
| `:syntax` | Syntax commands | `:syntax on` enables syntax highlighting |
| `:filetype` | Filetype commands | `:filetype on` enables filetype detection |
| `:verbose` | Show additional information | `:verbose set tabstop?` shows where option was set |

### External Commands

| Command | Description | Example |
|---------|-------------|---------|
| `:!` | Shell command | `:!ls` runs ls in shell |
| `:r !` | Read command output | `:r !date` inserts current date |
| `:w !` | Write buffer to command | `:w !grep foo` searches buffer for foo |
| `:!%` | Run current file | `:!% ./%` runs current file |
| `:shell` | Start shell | `:shell` starts sub-shell |
| `:terminal` | Start terminal | `:terminal` opens terminal window |

### Miscellaneous

| Command | Description | Example |
|---------|-------------|---------|
| `:redir` | Redirect messages | `:redir > file.txt` redirects to file |
| `:so` | Source file | `:so ~/.vimrc` reloads vimrc |
| `:finish` | Stop sourcing | `:finish` stops sourcing current file |
| `:au` | Show autocommands | `:au` shows all autocommands |
| `:noh` | No highlight | `:noh` clears search highlighting |
| `:let` | Set variable | `:let myvar = 5` sets variable |
| `:unlet` | Delete variable | `:unlet myvar` deletes variable |
| `:echo` | Echo expression | `:echo "hello"` prints hello |
| `:echom` | Echo message | `:echom "hello"` adds to message history |
| `:messages` | Show messages | `:messages` shows message history |
| `:version` | Show version | `:version` shows Vim version |
| `:help` | Show help | `:help w` help for w command |

---

## Replace Mode

| Command | Description | Example |
|---------|-------------|---------|
| `Esc` | Return to Normal mode | `Esc` exits Replace mode |
| `Ctrl+[` | Return to Normal mode | `Ctrl+[` exits Replace mode |
| `Ctrl+C` | Return to Normal mode | `Ctrl+C` exits Replace mode |
| `Ctrl+H` | Delete last character | `Ctrl+H` corrects last entry |
| `Ctrl+W` | Delete last word | `Ctrl+W` deletes previous word |
| `Ctrl+U` | Delete entire line | `Ctrl+U` clears replaced content |
| `Ctrl+R` | Insert from register | `Ctrl+R a` inserts register a |
| `Ctrl+O` | Execute one Normal command | `Ctrl+O $` moves to line end |
| `Ctrl+V` | Insert next character literally | `Ctrl+V Esc` inserts escape character |
| `Ctrl+@` | Insert previously inserted text | `Ctrl+@` inserts last inserted text |

---

## Operator-Pending Mode

| Command | Description | Example |
|---------|-------------|---------|
| `w` | Until next word | `d w` deletes to next word |
| `W` | Until next WORD | `d W` deletes to next WORD |
| `e` | To end of word | `c e` changes to word end |
| `E` | To end of WORD | `c E` changes to WORD end |
| `b` | Back to word start | `y b` yanks to word start |
| `B` | Back to WORD start | `y B` yanks to WORD start |
| `ge` | To end of previous word | `d g e` deletes to previous word end |
| `gE` | To end of previous WORD | `d g E` deletes to previous WORD end |
| `$` | To line end | `y $` yanks to line end |
| `0` | To line start | `d 0` deletes to line start |
| `^` | To first non-blank | `c ^` changes to first non-blank |
| `g_` | To last non-blank | `y g_` yanks to last non-blank |
| `gg` | To first line | `d g g` deletes to file start |
| `G` | To last line | `y G` yanks to file end |
| `%` | To matching bracket | `d %` deletes to matching bracket |
| `t` | Till before character | `d t x` deletes until before 'x' |
| `T` | Till after character backward | `d T x` deletes until after 'x' backward |
| `f` | Find character | `y f x` yanks up to and including 'x' |
| `F` | Find character backward | `y F x` yanks up to and including 'x' backward |
| `/{pattern}` | Until pattern | `d /foo` deletes until "foo" |
| `?{pattern}` | Until pattern backward | `d ?bar` deletes until "bar" backward |
| `(` | To previous sentence | `c (` changes to previous sentence |
| `)` | To next sentence | `y )` yanks to next sentence |
| `{` | To previous paragraph | `d {` deletes to previous paragraph |
| `}` | To next paragraph | `y }` yanks to next paragraph |
| `[[` | To previous section | `c [[` changes to previous section |
| `]]` | To next section | `y ]]` yanks to next section |
| `[]` | To end of previous section | `d []` deletes to end of previous section |
| `][` | To end of next section | `y ][` yanks to end of next section |
| `a` | Text object: a | `d a w` deletes a word |
| `i` | Text object: inner | `c i w` changes inner word |
| `Ctrl+I` | Same as `<Tab>` movement | `d Ctrl+I` deletes to next jump |

---

## Terminal-Job Mode

| Command | Description | Example |
|---------|-------------|---------|
| `Ctrl+W N` | Switch to Normal mode | `Ctrl+W N` exits job mode |
| `Ctrl+W "` | Paste register | `Ctrl+W " +` pastes clipboard |
| `Ctrl+W :` | Enter command | `Ctrl+W :` allows command input |
| `Ctrl+D` | Send EOF | `Ctrl+D` signals end-of-file |
| `Ctrl+C` | Interrupt job | `Ctrl+C` stops current job |
| `Ctrl+Z` | Suspend job | `Ctrl+Z` suspends current job |
| `Ctrl+\ Ctrl+N` | Switch to Normal mode | `Ctrl+\ Ctrl+N` exits terminal mode |
| `Ctrl+\ Ctrl+G` | Switch to Terminal-Normal mode | `Ctrl+\ Ctrl+G` enters special mode |

---

## Select Mode

| Command | Description | Example |
|---------|-------------|---------|
| `Ctrl+G` | Switch to Visual mode | `Ctrl+G` toggles Select/Visual mode |
| `Esc` | Return to Normal mode | `Esc` exits Select mode |
| `Ctrl+[` | Return to Normal mode | `Ctrl+[` exits Select mode |
| `Ctrl+C` | Return to Normal mode | `Ctrl+C` exits Select mode |
| `Shift+Left` | Extend selection left | `Shift+Left` selects left |
| `Shift+Right` | Extend selection right | `Shift+Right` selects right |
| `Shift+Up` | Extend selection up | `Shift+Up` selects upward |
| `Shift+Down` | Extend selection down | `Shift+Down` selects downward |
| `Home` | Extend to line start | `Home` selects to line start |
| `End` | Extend to line end | `End` selects to line end |
| `PageUp` | Extend page up | `PageUp` selects page up |
| `PageDown` | Extend page down | `PageDown` selects page down |

---

## Ex Mode

| Command | Description | Example |
|---------|-------------|---------|
| `:visual` | Return to Normal mode | `:visual` exits Ex mode |
| `:vi` | Return to Normal mode | `:vi` same as `:visual` |
| `Q` | Enter Ex mode | `Q` switches to Ex mode |
| `:global` | Global command | `:global/foo/p` prints lines with foo |
| `:vglobal` | Inverted global | `:vglobal/bar/p` prints lines without bar |
| `:substitute` | Substitute | `:substitute/old/new` replaces old with new |
| `:copy` | Copy lines | `:copy 5` copies lines to after line 5 |
| `:move` | Move lines | `:move 10` moves lines to after line 10 |
| `:join` | Join lines | `:join` joins lines |
| `:delete` | Delete lines | `:delete` deletes lines |
| `:write` | Write file | `:write` saves file |
| `:quit` | Quit | `:quit` exits Ex mode |

---

