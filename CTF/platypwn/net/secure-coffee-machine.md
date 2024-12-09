
# Secure Coffee Machine

You have gained access to a computer controlling the coffee machine in a company using corporate internet of things technologies. Because it is a coffee machine, it is not deemed important enough to be protected or isolated from the rest of the network…

You were able to change the coffee machine server ssh credentials to `ctf:ctf`, which luckily also has some tools like `tcpdump` preinstalled and is connected to the company network on the `coffee-machine` network interface.



Connecting to machine via ssh using credentials `ctf:ctf`

**findings:**

1. network interface `coffee-machine`  IP 10.0.0.1/24

![[ctf_platypwn_coffee-machine.png]]

2. files with SUID permission
![[ctf_platypwn_coffee-machine_3.png]]\


3. found few files with write permission but noting interesting 

4. found a folder `app` and file `enterypoint.sh`

![[ctf_platypwn_coffee-machine_4.png]]

```
#!/bin/bash

set -ex

mkdir -p /run/sshd
ssh-keygen -A

if [[ ! -v PEER_IP ]]; then
	echo "Please set PEER_IP"
	exit 1
fi

echo "Waiting for peer ip to be reachable"
until ping -c1 "$PEER_IP" >/dev/null 2>&1; do :; done

exec "$@"

```

thought this would lead me to a PrivEsc but this file was purely a rabbit hole ;)


checking the files from `app` directory.....

![[ctf_platypwn_coffee-machine_5.png]]

this looks like a source files of an application named `cyclonedds` 







