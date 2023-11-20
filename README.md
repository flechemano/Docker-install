# Docker-install
# update
```console
 apt update -y && apt upgrade -y
```
# we will need docker, add Docker's official GPG key:
```console
sudo apt-get install ca-certificates curl gnupg
```
```console
sudo install -m 0755 -d /etc/apt/keyrings
```
```console
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /etc/apt/keyrings/docker.gpg
```
```console
sudo chmod a+r /etc/apt/keyrings/docker.gpg
```
# Add the repository to Apt sources:

```console
echo \
  "deb [arch="$(dpkg --print-architecture)" signed-by=/etc/apt/keyrings/docker.gpg] https://download.docker.com/linux/ubuntu \
  "$(. /etc/os-release && echo "$VERSION_CODENAME")" stable" | \
  sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
```
# more update
```console
sudo apt-get update
```
# Install the Docker packages.
```console
sudo apt-get install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin -y
```
