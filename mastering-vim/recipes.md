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
