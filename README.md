# Laboratory 06: The Cloud Deployment Engineer

## Mission Overview

In this mission, I explored how to deploy a private cloud storage application using Docker Compose. I used Nextcloud for the web application and MariaDB for storing database information. This activity helped me understand how multiple containers can communicate and work together to run one application.

## Objectives

* Learn the basic concept of multi-tier architecture.
* Understand how Docker Compose manages multiple containers.
* Create a YAML configuration file using the nano editor.
* Deploy and manage Nextcloud and MariaDB.
* Learn the importance of Infrastructure as Code.
* Improve my documentation skills using Markdown and GitHub.

## Commands Executed

```bash
mkdir nextcloud-deployment
cd nextcloud-deployment
nano docker-compose.yml
docker-compose up -d
docker-compose ps
docker-compose down
```

## Skills Learned

I practiced creating configuration files, deploying Docker services, checking container status, and accessing a web application through a browser. I also learned how to organize cloud computing activities in a GitHub repository.

## Deployment Evidence

The following screenshots will be added to the `screenshots` folder:

* `compose-deployment.png`
* `nextcloud-web.png`
* `compose-teardown.png`

## Conclusion

This activity showed me how automation can make cloud deployment easier. I learned that Docker Compose is useful when an application needs multiple containers that must be configured to work together.
