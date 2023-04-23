  ad8888888888ba
 dP'         `"8b,
 8  ,aaa,       "Y888a     ,aaaa,     ,aaa,  ,aa,
 8  8' `8           "88baadP""""YbaaadP"""YbdP""Yb
 8  8   8              """        """      ""    8b
 8  8, ,8         ,aaaaaaaaaaaaaaaaaaaaaaaaddddd88P
 8  `"""'       ,d8""
 Yb,         ,ad8"
  "Y8888888888P"
Learning Objectives

General

What is a (physical) server
SSH essentials
SSH Config File
Public Key Authentication for SSH
man or help

ssh
ssh-keygen
env
Environment

OS: Ubuntu 20.04 LTS
Terminal: Bash 5.0.17
Puppet
Style guidelines: Puppet Style Guide
Puppet lint
install the OpenSSH client

$ sudo apt-get install openssh-client
$
Execute

$ ./0-use_a_private_key
ubuntu@server01:~$ exit
Connection to 8.8.8.8 closed.
$
$ ./1-create_ssh_key_pair
Generating public/private rsa key pair.
Your identification has been saved in school
Your public key has been saved in school.pub
The key fingerprint is:
SHA256:7vxuWOhoZPFYW1h3DeIaF+MZqFtfYXx1IpX2fdOLqRk root@9d03faf1f602
The key's randomart image is:
+---[RSA 4096]----+
|           .*o+++|
|          oo.BB.+|
|         +..=+ +o|
|      . + o+  ..=|
|       =S*.. .o +|
|      +.= .E.o . |
|     o o.o  +    |
|      ooo .o     |
|     .  o+o      |
+----[SHA256]-----+
$
Add the SSH public key to the server

sudo vim ~/.ssh/authorized_keys

and add the key

Autor

ESERE EJENUGBOR C.
