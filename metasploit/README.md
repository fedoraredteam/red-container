Metasploit Framework
======

How to build
------

- Docker tooling

```bash
cd metasploit
docker build -t metasploit .
```

- Using buildah

```bash
buildah bud -t metasploit -f metasploit/Dockerfile
```

How to run
---------

- Docker tooling

```bash
docker run --rm -itv $HOME/.msf4:/home/metasploit/.msf4 metasploit msfconsole
```

- Podman

```bash
podman run --rm -itv $HOME/.msf4:/home/metasploit/.msf4:z metasploit msfconsole
```

Example
---------
```
$ sudo podman run --rm -itv /home/jyoung/.msf4:/home/metasploit/.msf4:z metasploit msfconsole
Found a database at /home/metasploit/.msf4/db, checking to see if it is started
Starting database at /home/metasploit/.msf4/db...success

Call trans opt: received. 2-19-98 13:24:18 REC:Loc

     Trace program: running

           wake up, Neo...
        the matrix has you
      follow the white rabbit.

          knock, knock, Neo.

                        (`.         ,-,
                        ` `.    ,;' /
                         `.  ,'/ .'
                          `. X /.'
                .-;--''--.._` ` (
              .'            /   `
             ,           ` '   Q '
             ,         ,   `._    \
          ,.|         '     `-.;_'
          :  . `  ;    `  ` --,.._;
           ' `    ,   )   .'
              `._ ,  '   /_
                 ; ,''-,;' ``-
                  ``-..__``--`

                             https://metasploit.com


       =[ metasploit v4.16.44-dev-                        ]
+ -- --=[ 1742 exploits - 995 auxiliary - 301 post        ]
+ -- --=[ 529 payloads - 40 encoders - 10 nops            ]
+ -- --=[ Free Metasploit Pro trial: http://r-7.co/trymsp ]

msf > db_status
[*] postgresql connected to msf
msf >
```
