# IEX

* close IEX fast ctrl+\

## run elixir script and keep running
* `elixir --no-halt cool.exs`

## history
```
export ERL_AFLAGS="-kernel shell_history enabled"
```

## mix

### remove dependencies
```
mix deps.clean --unlock --unused
```

## debug

*  :sys.get_state(pid)
*  Process.info(pid, :current_function)
*  spawn(fn -> :etop.start end)
*  Process.exit(pid, :kill)
*  iex --name laptop@192.168.1.2 --cookie "your_cookie_value" --remsh node1@server.local


## force a gc

*  :erlang.garbage_collect()

