# AWS
#### Check  https://www.rstudio.com/products/rstudio/download-server/ for latest version of RStudio Server
#### On EC2 instance level : add the following inbound rule --> [Custom TCP Rule : TCP : 8787 : Anywhere]
#### By default, RStudio Server Pro uses port 8787 for HTTP and port 443 for HTTPS
##### !bin/bash

##### 1--> Update the package manager
sudo yum update -y

##### 2--> Install R
sudo amazon-linux-extras install R3.4 -y

##### 3--> Install RStudio Server
wget https://download2.rstudio.org/server/centos6/x86_64/rstudio-server-rhel-1.2.5019-x86_64.rpm

sudo yum -y install rstudio-server-rhel-1.2.5019-x86_64.rpm

##### 4--> Add user(s)
sudo useradd username

echo username:password | sudo chpasswd

