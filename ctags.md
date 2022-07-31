# Ctags

## Installation

```sh
brew install universal-ctags
```

## Running
```sh
ctags -R --languages=elixir
```

```sh
ctags -R .
```

## Vim

```
:set tags=./tags,tags;$HOME
```

### Keyboard command Action

* `Ctrl-]` Jump to the tag underneath the cursor
* `:ts <tag> <RET>` Search for a particular tag
* `:tn` Go to the next definition for the last tag
* `:tp` Go to the previous definition for the last tag
* `:ts` List all of the definitions of the last tag
* `Ctrl-t` Jump back up in the tag stack

https://courses.cs.washington.edu/courses/cse451/10au/tutorials/tutorial_ctags.html
