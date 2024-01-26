# Generate new ssh
```shell
ssh-keygen -t ed25519 -C "your_email@example.com"
```
This creates a new SSH key, using the provided email as a label.
#### type of ssh
There are RSA, DSA, ECDSA, or EdDSA
> The most secured is **ed25519 algorithm** (an ECDSA variant)
## Add ssh to keygen agent
Start the ssh-agent in the background.
```shell
$ eval "$(ssh-agent -s)"
> Agent pid 59566
```
