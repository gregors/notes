# IEX

* close IEX fast ctrl+\

## run elixir script and keep running
* `elixir --no-halt cool.exs`

## history
```
export ERL_AFLAGS="-kernel shell_history enabled"
```

## debug

*  :sys.get_state(pid)


## force a gc

*  :erlang.garbage_collect()

