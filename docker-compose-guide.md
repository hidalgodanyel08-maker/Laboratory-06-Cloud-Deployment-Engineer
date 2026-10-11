# Guide to Docker Compose Deployment

## Introduction

Docker Compose is a tool for defining and running applications that use multiple containers. It uses a YAML file to describe the services and their configurations. For this mission, I used Docker Compose to set up Nextcloud and MariaDB in one deployment.

## Purpose of the `services:` Block

The `services:` block lists the containers required by the application. My configuration contains two services:

1. **database** – Runs MariaDB 10.6 and defines the database credentials and database name.
2. **app** – Runs Nextcloud and maps port 8080 on the host to port 80 inside the container.

Docker Compose uses these definitions to configure and start the required services.

## How Nextcloud Connects to MariaDB

The setting `MYSQL_HOST=database` tells Nextcloud to connect to the service named `database`. Docker Compose provides network-based service discovery, so the application can locate the database using its service name instead of needing a manually assigned IP address.

The database username, password, and database name must also be configured consistently between the two services.

## Difference Between `docker run` and `docker-compose up -d`

The `docker run` command is commonly used to create and start an individual container with specified options. When an application requires several containers, configuring each one manually can take more time.

The `docker-compose up -d` command reads the Compose file and starts the services defined in it. The `-d` option allows the containers to run in the background. I find this method more convenient because the configuration is saved and can be reused.

## Commands Used in the Mission

### Create the working directory

```bash
mkdir nextcloud-deployment
cd nextcloud-deployment
```

### Create the YAML file

```bash
nano docker-compose.yml
```

I used the nano editor to write and save the configuration.

### Start the deployment

```bash
docker-compose up -d
```

This command creates and starts the services in the background.

### Verify the services

```bash
docker-compose ps
```

This command helps me check whether the containers are running.

### Stop the deployment

```bash
docker-compose down
```

This command stops and removes the containers and default network created for the Compose project. Named volumes are not removed by this command unless specifically requested.

## Understanding Infrastructure as Code

Infrastructure as Code (IaC) means describing infrastructure through configuration files that can be stored, reviewed, and reused. In this mission, the `docker-compose.yml` file acts as the deployment plan. Instead of remembering every command and setting, I can refer to the file when deploying the application again.

## Conclusion

Through this task, I learned that Docker Compose can simplify the management of applications with multiple services. It also helps make deployment instructions more consistent and easier to share with other developers.
