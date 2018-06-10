# Recipes for Mastering Vim

## Execute a single command without leaving "Insert" mode

It's important that you know that you can execute a single command 
without leaving the "Insert" mode.

To do that, let's say you are in the "Insert" mode typing. Then:

* Press "Ctrl" + "o".
* Use any Vim command (:w).
* You are back to "Insert" mode.

## Replace a word from the cursor position until the end of the word

It's possible to do this by using "cw", which stands for 
"change word".

This command will delete the word from the cursor position until the 
end of the word and enter the "Insert" mode. 

## Search text through multiple files

You can do this in an easy way by using the "vimgrep" command.

This command, for instance, will search for the string "Insert" in all 
Markdown files (ending with .md) in the "mastering-vim" directory:

```
:vimgrep Insert mastering-vim/*.md
```

If you want to jump to the next and previous entry, use:

```
:cn[ext] and :cp[revious]
```

If you want to jump to the next and previous file, use:

```
:cnf[ile] and :cpf[ile]
```

If you want to go to the beginning or end of the search list, use:

```
:cr[ewind] and :cla[st]
```

Finally, you can discover plenty of other commands using:

```
:help quickfix
```

## Split the buffer into multiple windows safely

Buffers are a very important concept to understand. When you open a file 
in Vim and start editing it, you are, in fact, only editing a "copy" of 
the file. The file has actually been opened into a "buffer", and that 
buffer is just a chunk of memory allocated to holding a copy of the file
you wanted to edit.

The original file remains unchanged until you actually "write" the 
buffer back to the file (that's where the `:w` write command comes in; 
it effectively "saves" the file).

Another reason why buffers are important to understand is that we can 
utilize them in different ways. For example, because we're dealing with 
buffers and not the original file, we can safely split the buffer into 
multiple windows, using the `:sp` command. From there, we can edit/write 
the buffer in either window, without any conflicts.

## Get an interactive story of executed commands

To do that, type:

```
q:
```

You can edit or run them, by hitting Enter.

```
vi hello.py
:w
:wq
```
