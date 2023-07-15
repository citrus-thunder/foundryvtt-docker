# FoundryVTT/Docker

***Simple FoundryVTT Containerization with Docker***

This repository contains a very simple Docker setup for Foundry Virtual Tabletop. Its contents include a Dockerfile which describes the Docker Image setup, and a Docker Compose YAML definition for quick and easy container/volume setup.

### Quick Setup

#### Step 1: Install Docker
In order to containerize your Foundry instance using Docker, Docker must first be installed. Follow [Docker's Installation Guide](https://docs.docker.com/engine/install/) to get started.

#### Step 2: Retrieve Foundry Installation
In order to containerize your Foundry instance, you will need the Foundry program. There are two ways to get this:

* Download the Linux/Node version of Foundry from the account area of the FoundryVTT website.
	* You will receive a `.zip` file containing the Foundry program. Move this file to the same folder as the `Dockerfile`, and rename it to `foundry.zip`.
	* If you use this option, be sure to comment out `Option 1` in the `Dockerfile` and un-comment `Option 2`
* Get a temporary download URL for the Linux/Node version of Foundry from the account area of the FoundryVTT website.
	* If using Docker Compose in the next step, put this URL in the `FOUNDRY_URL` arg in the `docker-compose.yml` file.
	* If using Docker CLI in the next step, you will pass this URL to the `docker build` command with the flag `--build-arg FOUNDRY_URL=your-url-here`

#### Step 3a (Option 1): Set up using Docker Compose (Recommended)
Simply configure the `docker-compose.yml` file to your requirements, then run the `docker compose up` command. See the [docker compose reference](https://docs.docker.com/compose/) for more info.

#### Step 3b (Option 2): Set Up using Docker CLI
Simply run the `docker build` command to build your image. See the [docker build reference](https://docs.docker.com/engine/reference/commandline/build/) for more info.