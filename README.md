# Access Cpanel via SSH without password

## 1. First we have to generate SSH key pair from your development machine

```bash
kenura@kenura-HP-250-G7-Notebook-PC:~$ ssh-keygen
Generating public/private rsa key pair.

Enter file in which to save the key (/home/kenura/.ssh/id_rsa): <id_rsa_test_key_1>

Enter passphrase (empty for no passphrase): 
Enter same passphrase again:

Your identification has been saved in id_rsa_test_key_1
Your public key has been saved in id_rsa_test_key_1.pub

The key fingerprint is:
SHA256:8C28yMWh9Vl/+/5CY1g9XEyR/8xDWO1euIwL0aA8xBs kenura@kenura-HP-250-G7-Notebook-PC
The key's randomart image is:
+---[RSA 3072]----+
|       .       +=|
|        E .    o+|
|      .oo+ o. ++o|
|       B=+.o.oo+=|
|      . S.+. =o==|
|     . o o. o *o*|
|      o .  . + o.|
|            . . .|
|               o=|
+----[SHA256]-----+

```
Enter the file location with name in `Enter file in which to save the key (/home/kenura/.ssh/id_rsa):`

Enter a password if you want extra protection over the ssh key - `Enter passphrase (empty for no passphrase): `

Then if you need to put the below codes inside the file `~/.ssh/config`. If this file do not exists then create one.

```
IdentityFile <location_for_the_private_key>
```

## 2. Copy both Private key and the Public key to Cpanel

Login to cpanel and put the key pairs and authorize them. Thats all.

Thank you,

@Kenura R.Gunarathna.
