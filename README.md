# Debug utils for PHP

## Remote debugging

Mey be usefull when code executed on remote server, and PHP runtime needs to connect to IDE on local machine, but
remote server can not connect to local IDE directly.

First forward remote port to local port, accessible by IDE:

```
ssh -fN some-ssh-host -R 9000:127.0.0.1:9000
```

Then run script:

```
./debugRemote /path/to/some.php arg1 arg2
```

## Building flame graph

More info about flame graphs may be found in http://www.brendangregg.com/flamegraphs.html.

Run scipt and pass path target to SVG file:

```
./flameGraph /path/to/flamegrapg.svf /path/to/some.php arg1 arg2
```

Flamegrapg will be stored at /path/to/flamegrapg.svf
