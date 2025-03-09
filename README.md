# Comuter_SciencePhDPhysicsPadova

## Docker Installation Guide in macOS Silicon

### 1. Download Docker Desktop
Download Docker Desktop from the following link:
https://www.docker.com/products/docker-desktop/

### 2. Install Docker
Open the downloaded .dmg file and drag the Docker icon to the applications folder.

![How-to-install-Docker-1](https://github.com/user-attachments/assets/d51cff78-2837-468c-8aa3-4bcb2fea0e17)

### 3. Permission settings
The first time you start Docker, it will ask for permissions to configure networks. Click Accept and enter your password if requested.

### 4. Verify the installation
Open the terminal as super user and enter your password when prompted:

_sudo su_

When you are in super user mode, run:

_docker_ _—version_

and you will get an output like this:

_Docker version 24.x.x, build xxxxxxx_

If you get an output like the one in the previous line, it means that you have successfully installed Docker on your MacOs Silicon system.

## AlmaLinux 9 in Docker

### 1. Download the AlmaLinux 9 image

Run in the terminal:

_docker pull almalinux:9_

This command will download the latest version of AlmaLinux 9.

### 2. Verify the downloaded image

Run on the terminal:

_docker images_

Where you get an output similar to this:

![Screenshot 2025-03-09 at 15 11 03](https://github.com/user-attachments/assets/1911a28d-db4e-4ef4-8d47-bfaef9637e35)

### 3. Create and run an AlmaLinux 9 container

If we want to  start a container in interactive mode, we must execute the following command:

_docker run -it --name mi-almalinux almalinux:9_

This will open a terminal inside the AlmaLinux 9 container.

### 4.Verify that you are in AlmaLinux 9

Inside the container, execute:

_cat /etc/os-release_

Where you should get an output like this:

![Screenshot 2025-03-09 at 15 16 14](https://github.com/user-attachments/assets/0d37fec5-ef52-468b-bb46-e104530649da)

### 5. Manage Containers

To list the running containers, we must execute the following command:

_docker ps_

If the container is stopped, use:

_docker ps -a_

You should get an output like this:

![Screenshot 2025-03-09 at 15 19 44](https://github.com/user-attachments/assets/3f3372b0-d0c6-4069-abca-bed79ae07665)

### 6. Stopping a container

To stop the container, you must use the following command:

_docker stop mi-almalinux_

### 7. To restart a container:

_docker start -ai mi-almalinux_

### 8. To delete a container: 

_docker rm mi-almalinux_
