# Zig-update

Small script I made to keep my Zig install up to date.
It will fetch the latest release from the Zig website and create a symlink to it at $HOME/.zig/zig.
You can switch to a specific version by running `zig-update [latest|0.7|0.6|...]`

Example:
```
$ zig-update 0.7
Downloading https://ziglang.org/download/index.json...
Downloading https://ziglang.org/download/0.7.0/zig-linux-x86_64-0.7.0.tar.xz...
Switched to Zig version 0.7.0.
$ zig version
0.7.0
```

The tool will remember your choice and stay on that version from now on until you specify a new one.
To switch back to the latest version:
```
$ zig-update latest
Downloading https://ziglang.org/download/index.json...
Zig latest already present and up to date.
Switched to Zig version latest.
```

For this to work, you will need to add ~/.zig/zig to your path. It will offer to update your .profile file for you.

You can change the directory used to install Zig by setting the `ZIG_UPDATE_DIR` variable.