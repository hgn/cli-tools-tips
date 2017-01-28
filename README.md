# Command Line Interface Tools Tips

## Vim

### General Tips

- never ever leave vim, stay within vim all the time. `<CTRL>-Z` to suspend vim, execute shell command and `fg` to foregrounding into vim again. This will keep your vim history/state intact. If required open additional terminals to do things. But repeat: never ever leave vim

### Plugings

- ctrlp
- easymotion
- cscope

### Open Files

- No fancy nerdtree

Command | Comment
---     | ---
`<CTRL> | start typing chars of filename and hit enter, really fast
`:e .` | open netrw and provides list to open files
`:e<TAB>` | same same but different

### Motions

- Easymotion installed (leader command single `,`)

Command | Comment
---     | ---
`,w` | easymotion forward
`,b` | easymotion forward

### Marks & Jumps

- Cscope installed

Command | Comment
---     | ---
`<CTRL>O` | jump to the previous entry in jump list
`<CTRL>I` | jump to next entry in jump list
`:jumps` | display all available jump targets
