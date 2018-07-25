To fix error: Unable to update and upgrade Kali Linux
```
gpg --keyserver pgpkeys.mit.edu --recv-key  ED444FF07D8D0BF6
gpg -a --export ED444FF07D8D0BF6 | sudo apt-key add -
```
Then we can run
```
sudo apt-get update
```
