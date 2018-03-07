nmap container
=======

How to build
-----

- With Docker tooling
```bash
$ sudo docker build -t nmap .
```

- With buildah
```bash
$ sudo buildah bud -f Dockerfile -t nmap
```

How to run
----

Some scan types require additional capabilities that can be enabled by running with `--privileged`

```bash
$ sudo docker run --rm -it nmap -A -Pn www.google.com

$ sudo podman run --privileged --rm -it nmap --script ssl-cert www.github.com -vv
```
