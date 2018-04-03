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
