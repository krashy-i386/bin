# bin
A paste bin written in rust.
Stolen from [here](https://github.com/w4/bin)

##### How to compile

```bash
$ git clone https://github.com/krashy-i386/bin

$ cd bin

$ cargo build --release
   ...

$ ./target/release/bin
    ...
```

##### Settings

```
$ ./bin --help

Usage: bin [<bind_addr>] [--buffer-size <buffer-size>] [--max-paste-size <max-paste-size>]

a pastebin.

Positional Arguments:
  bind_addr         socket address to bind to (default: 127.0.0.1:8820)

Options:
  --buffer-size     maximum amount of pastes to store before rotating (default:
                    150)
  --max-paste-size  maximum paste size in bytes (default. 512kB)
  --help            display usage information
```

##### Curl support

```bash
$ curl -X PUT --data 'hello world' http://127.0.0.1:8820
http://127.0.0.1:8820/cateettary
$ curl http://127.0.0.1:8820/cateettary
hello world
```

##### Syntax highlighting

To get syntax highlighting you need to add the file extension at the end of your paste URL.
