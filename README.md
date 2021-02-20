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

- No fancy nerdtree, simple CTRLP

Command | Comment
---     | ---
`<CTRL> | start typing chars of filename and hit enter, really fast
`:e .` | open netrw and provides list to open files
`:e<TAB>` | same same but different

Nerdtree specific:

Command | Comment
---     | ---
`<CTRL>P` | open CTRL menu (subsequent commands are based on ctrlp)
`<ENTER>`  | replace current buffer with new buffer
`<ctrl-v>` | split window vertically and load new buffer
`<ctrl-x>` | split window horizontal and load new buffer

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

### Scrolling

Command | Comment
---     | ---
`CTRL-Y` | scroll downwards
`CTRL-E` | scroll upwards

### Csopes Movements

Command | Comment
---     | ---
`CTRL-]` | follow defintion
`CTRL-T` | backwards

## Radare2

### Common

```
r2 -A -e io.cache=true <object>
```

- disass main: `pdf@main`
- analyze all: `aa`
- show sections: `iS`
- list functions: `afl`
- list imports: `ii`
- list entrypoints: `ie`
- seek to function: `s main`
- add comment: `CC`

### Function Handling

- show basic block disassembly: `pdb`
- show function disassembly: `pdf`
- show function arguments: `afa`
- show function variables: `afv`
- rename current fucntion: `afn`
- rename function variable: `afvn`
- set function variable type: `afvt`
- add/analyze function: `af`

### Visual Mode

- enter visual mode: `V`
- select function, variable, xref: `v`
- quick command/seek: `_ <search string>`
- show cursor: `c`
- set function name: `d`
- add comment: `;`

### Graph Mode

- enter graph modes: `VV`
- cycle types of graphs: `p`
- seek to function: `g<identifier>`
- undo seek: `u`
- define new function at cursor: `df`
- show comments: `'`
- add comment: `/`
- add comment (complex): `:CC!`

### Misc

## analysis, assembly, memory ###

- analyze functions: `af`
- analyze stack: `ad@rsp` 
- search for opcode: `/a`
- search for rop/jop/etc: `/R`
- search for bytes: `/x `
- get offset for the actual seek point address: `?p`




