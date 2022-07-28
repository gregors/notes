# JS

```sh
% node
Welcome to Node.js v14.19.3.
Type ".help" for more information.
> boom = (x) => console.log(x)
[Function: boom]
> boom("greg")
greg
undefined
```

# Elixir

```sh
% iex
Erlang/OTP 25 [erts-13.0] [source] [64-bit] [smp:16:16] [ds:16:16:10] [async-threads:1] [jit:ns] [dtrace]

Interactive Elixir (1.13.4) - press Ctrl+C to exit (type h() ENTER for help)
iex(1)> boom = fn x -> IO.puts(x) end
#Function<42.3316493/1 in :erl_eval.expr/6>
iex(2)> boom.("greg")
greg
:ok
```

# Ruby

```sh
% irb
2.7.0 :001 > boom = lambda{|x| puts x}
2.7.0 :002 > boom.("greg")
greg
 => nil
```

# Python

```sh
% python3
Python 3.9.13 (main, May 24 2022, 21:28:31)
[Clang 13.1.6 (clang-1316.0.21.2)] on darwin
Type "help", "copyright", "credits" or "license" for more information.
>>> boom = lambda x: print(x)
>>> boom("greg")
greg
```

# Java

```sh
 % jshell
|  Welcome to JShell -- Version 17.0.1
|  For an introduction type: /help intro

jshell> Consumer<String> boom = (x) -> System.out.println(x);
boom ==> $Lambda$21/0x0000000800c09a08@1d81eb93

jshell> boom.accept("greg")
greg
```

# Rust
