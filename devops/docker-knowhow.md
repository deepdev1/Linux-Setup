## Docker-CE Installation

Ubuntu 22.04
```bash
sudo apt update && sudo apt install -y apt-transport-https ca-certificates curl software-properties-common && \
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg && \
echo "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null && \
sudo apt update && \
sudo apt install -y docker-ce && \
sudo apt install -y docker-compose && \
sudo usermod -aG docker ${USER} && \
su - ${USER}
```
Source: [digital-ocean](https://do.co/3Q0OzWv)
  
  
Ubuntu 20.04
```bash
sudo apt update && sudo apt install -y apt-transport-https ca-certificates curl software-properties-common && \
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add - && \
sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu focal stable" && \
sudo apt update && \
sudo apt install -y docker-ce && \
sudo apt install -y docker-compose && \
sudo usermod -aG docker ${USER} && \
su - ${USER}
```
Source: [digital-ocean](https://do.co/3fRCEd7)

