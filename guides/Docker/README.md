# Docker general setup includes:

For a ubuntu 22.04 vanilla system:

```
sudo apt install apt-transport-https ca-certificates curl software-properties-common
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg
echo "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
sudo apt update
apt-cache policy docker-ce | grep -ci ubuntu #should be dozens, must not be zero
sudo apt install docker-ce
#verify docker is present:
sudo systemctl status docker
#add current user to docker group to avoid sudo need/nag
sudo usermod -aG docker ${USER}
##or add specific user:
#sudo usermod -aG docker  <username>
#log out and back in to refresh group status, check with:
groups | grep docker
```
