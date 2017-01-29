# Command Line Interface Tools Tips

## Vim

### General Tips

- never ever leave vim, stay within vim all the time. `<CTRL>-Z` to suspend
	vim, execute shell command and `fg` to foregrounding into vim again. This
	will keep your vim history/state intact. If required open additional
	terminals to do things. But repeat: never ever leave vim

### Plugings

- ctrlp
- easymotion (leader command single `,`)
- cscope

### Open Files

- No fancy nerdtree

Command | Comment
---     | ---
`<CTRL> | start typing chars of filename and hit enter, really fast
`:e .` | open netrw and provides list to open files
`:e<TAB>` | same same but different

### Motions

Command | Comment
---     | ---
`,w` | easymotion forward
`,b` | easymotion forward
`f<char>` | jump to next occurance of <char> in line, forward
`t<char>` | jump to next occurance of <char> in line, next to it

### Marks & Jumps

Command | Comment
---     | ---
`<CTRL>O` | jump to the previous entry in jump list
`<CTRL>I` | jump to next entry in jump list
`:jumps` | display all available jump targets

### Cut, copy & paste

Command | Comment
---     | ---
`y` | yank selected text
`yy` | yank line
`p` | paste yank buffer
`dd` | delete current line
`D` | cut till end
