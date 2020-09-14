* https://dwmkerr.com/effective-shell-part-1-navigating-the-command-line/
* https://www.computerhope.com/unix/bash/bind.htm
* https://www.techrepublic.com/blog/linux-and-open-source/using-vi-key-bindings-in-bash-and-zsh/

# reverse-i-search
* control-r  search backwards
* control-s  search forwards
* control-g  exit search


# edit current line
Just do Ctrl-X then Ctrl-E

# edit previous command
* `fc`

# lines of code in a project

```bash
find . -name '*.rb' | xargs wc -l
```
