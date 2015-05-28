The vimsed script makes vim behave kind of like sed.

Syntax:
```sh
vimsed "<vim normal-mode keystrokes>"
```

vimsed will "pipe" stdin to stdout, modifying it first by running the keystrokes.

Warning: Uses temporary files `~/vimsedin`, `~/vimsedcmd.vim` and `~/vimsedout`.

Example:

(**Note:** The `"^M"` is a special character, not `^` and `M`.  Type `Ctrl-V + Enter` to type it.  It stands for a carriage return)

```sh
$ vimsed ":s/e/i/g^M"
(user input:)
hello
hello
(Ctrl-D to terminate user input)
(vimsed output:)
hillo
hello
```
