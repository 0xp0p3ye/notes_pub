---
share_link: https://share.note.sx/abw3qfu9#sTh2iU2gzzGMHc9HoE6JAz8mjXPOJw22SM1UU5IOHoM
share_updated: 2024-12-10T19:49:45+05:30
---

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

4. Using `tcpdump` to capture the traffic on the `coffee-machine` interface

![[ctf_platypwn_coffee-machine_4.png]]


6. found a folder `app` and file `enterypoint.sh`

![[ctf_platypwn_coffee-machine_5.png]]

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

![[ctf_platypwn_coffee-machine_6.png]]

this looks like a source files of an application named `cyclonedds` 

`https://github.com/eclipse-cyclonedds/cyclonedds-python`

Cyclone DDS Python is **a modern and easy to use binding for Cyclone DDS**. It provides access to almost all features available in the CycloneDDS C API while abstracting all of C's quirks and hassles.

![[ctf_platypwn_coffee-machine_7.png]]

we can see that there are 2 entities in the network
![[ctf_platypwn_coffee-machine_8.png]]



after learning about the available commands and it's usage we can know that the user can subscribe and publish to the 2 found entities

`request-secret` &  `secret-exchange`

*fetching the source code of two entities*

![[ctf_platypwn_coffee-machine_9.png]]

![[ctf_platypwn_coffee-machine_10.png]]

`request-secret` This function sets a boolean "send_flag" 

 `secret-exchange` fetches a string named "flag" 

let's now try to request for the flag and see if the  `secret-exchange` functions returns accordingly

to do that we can simply use subscribe command wait for the reply from remote 


![[ctf_platypwn_coffee-machine_11.png]]

even after waiting for long time this doesn't return any flag......;)

Assuming that the  `secret-exchange` function returns the flag sting only when the `send_flag` bool is true!
so 


```
>>> message = Msg(True)
>>> writer.write(message)
```


![[ctf_platypwn_coffee-machine_12.png]]
