## Copilot
To install Docker on your Ubuntu system, you can follow these steps:
- Update your existing list of packages:

sudo apt update

- Install a few prerequisite packages which let apt use packages over HTTPS:

sudo apt install apt-transport-https ca-certificates curl software-properties-common

- Add the GPG key for the official Docker repository to your system:

curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -

- Add the Docker repository to APT sources:

sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable"

- Update the package database with the Docker packages from the newly added repo:

sudo apt update

- Make sure you are about to install from the Docker repo instead of the default Ubuntu repo:

apt-cache policy docker-ce

- Finally, install Docker:

sudo apt install docker-ce

After these steps, Docker should be installed and ready to use.
