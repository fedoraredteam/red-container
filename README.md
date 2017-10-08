# red-container
The Red Container project will work on containerizing the popular tooling in Kali Linux 
so that they can be run from any Linux distro, including Fedora, CentOS, and RHEL.

### Using Dockerfiles
1. cd into the folder of your choice. An example shown below.
```
cd nmap
```

2. Execute docker build with the tag of the appropriate tool name.
```
# docker build -t nmap .
```

3. Check if the build was successful.
```
# docker images
```

4. Run and attch to the container.

```
# docker run -ti nmap /bin/bash
```

5. Use said tool
```
nmap --version
```
