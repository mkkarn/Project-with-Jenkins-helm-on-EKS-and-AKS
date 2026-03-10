Install Docker

yum install docker
systemctl start docker
systemctl enable docker

provide permissions to jenkins user in jenkins server to access docker

  sudo groupadd docker
  sudo usermod -aG docker jenkins
  sudo chmod 777 /var/run/docker.sock

Add Jenkins user into sudoers file to get sudo access

   vi /etc/sudoers
   jenkins ALL=(ALL) NOPASSWD: ALL
