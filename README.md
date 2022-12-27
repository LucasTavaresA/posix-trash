# Trash

No bash bullshit, extremely basic trash shellscript.

## Usage

To delete files:

```console
trash <file1> <file2>
```

To list and ask to delete your trash folder:

```console
trash clean
```

### Trash folder

You can change the variable `$TRASH_FOLDER` to change its location,
by default it uses `~/.local/share/Trash` like other trash tools.

### Clean alert

Notifications depend on having the command `notify-send`, normaly on the `libnotify` package,
otherwise it uses `echo`.

The count goes up after every completed trash operation,
it defaults to 5 operations but you can change using the `$TRASH_AMOUNT` variable.

### File names

Files moved to the trash are renamed to avoid the complexity of file name conflicts.

Files are named like this:

`<file/folder>--<day>_<hour>:<minute>--<nanosecond><file-extension>`

- Nanosecond grants that no files have the same name

