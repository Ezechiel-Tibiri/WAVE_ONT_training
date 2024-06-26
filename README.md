![](images/logo.png)

# Welcome to the WAVE ONT training github repository

# Bioinformatics Applied Course Docker Environment

This Dockerfile sets up an extended Jupyter environment tailored for bioinformatics analysis. It includes various Python and system-level packages necessary for bioinformatics tasks.
This Docker environment is designed to support bioinformatics courses and analyses, providing a comprehensive set of tools and libraries commonly used in the field.

## Contributors
* Ezechiel B. TIBIRI,
email: ezechiel.tibiri@wave-center.org
* Cyrielle NDOUGONNA,
email: cyrielle.ndougonna@wave-center.org
* Fidèle TIENDREBEOGO,
email: fidele.tiendrebeogo@wave-center.org
* Pakyendou Estel NAME,
email: pakyendouename@gmail.com

* This training workshop was supported by the [Cambridge-Africa ALBORADA Research Fund](https://www.cambridge-africa.cam.ac.uk/initiatives/the-alborada-research-fund/funded-projects-2023/) from the University of Cambridge and the [Central and West African Virus Epidemiology (WAVE)](https://wave-center.org/) Regional Center of Excellence for transboundary plant pathogens.
## Docker installation and configuration
## On Linux 

```bash
sudo apt update && sudo apt upgrade -y
```
Install docker

```bash
sudo apt install docker.io
```
Start docker service

```bash
sudo systemctl start docker
```
Check installation

```bash
docker --version
```
Add user to docker group
```bash
sudo usermod -aG docker $USER
```

### On WSL (Windows Subsystem for Linux):

Watch this video for the Docker installation: [Installation and configuration of Docker on Windows](https://www.youtube.com/watch?v=qApYnUYaDPA)

*Activating WSL:* Before installing Docker on WSL, ensure that WSL is enabled on your Windows system. You can enable WSL by following the instructions provided by Microsoft: [Install WSL on Windows 10](https://learn.microsoft.com/en-us/windows/wsl/install)

*Installing Docker Desktop for Windows:* On Windows, the simplest way to use Docker with WSL is to install Docker Desktop for Windows, which supports WSL 2. You can download Docker Desktop from the official Docker website: [Docker Desktop for Windows](https://docs.docker.com/desktop/install/windows-install/)

*Configuring Docker with WSL:* Once Docker Desktop is installed, ensure that it is configured to use WSL. You can configure Docker Desktop to use WSL by selecting "Settings" in the Docker taskbar, then enabling "Use the WSL 2 based engine".


* You can verify if Docker is working correctly with WSL by opening a WSL terminal and running the following command:

```bash
docker --version
```

## Usage
* Test the Docker image, use the following command:

```bash
docker run hello-world
```
* For our course, we will use an already available docker image
```
docker load -i bioinformatics-course.tar
```
* Load your docker image
```bash
docker run -p 8888:8888 bioinformatics-course
```

* Copy a directory from the host system to a Docker container:

```bash
docker cp directory/ container_name:/path/destination/
```

* Copy a directory from a Docker container to the host system:

```bash
docker cp container_name:/path/source/ directory/
```
