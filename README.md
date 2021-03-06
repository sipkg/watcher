Watcher is a **Go live reload** program for **Linux**.

Watcher monitors the files in a directory and all its subfolders. 
If a write or delete event occurs on any file, the Go program is reloaded.

Watcher ignores any pattern in the **.gitignore** and the **.watcherignore** files.

## Usage

`-dir path` the folder to watch (default current folder)
`-run prog` the program to run (default empty)
`-help` to view the command usage 

**Examples**

Watch the current folder (default) and run the program in ./cmd/server

```sh
watcher -run ./cmd/server/ 
```

Watch folder ./pkg and run the program in ./cmd/server

```sh
watcher -run ./cmd/server -dir ./pkg
```

Example of a *.watcherignore* file

```
$ cat .watcherignore
.watcherignore
.git
cmd/client
*.md
*.yml
*.sh
*.mod
*.sum
Makefile
```
