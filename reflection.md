# Mission 6 Reflection

In this laboratory activity, I learned how to prepare and deploy a multi-container application using Docker Compose. The activity helped me understand that a cloud application can consist of several services instead of depending on only one container. I used Nextcloud as the application and MariaDB as its database.

I think writing a `docker-compose.yml` file is more convenient than entering every Docker command manually. The file contains the settings needed for the deployment, so I can use one command to start the services. It also helps me avoid repeating the same configuration whenever I need to deploy the application again.

One important thing I learned is that YAML requires correct indentation. If I use a Tab instead of spaces or place a setting in the wrong position, the configuration may fail to load. Because of this, I need to pay attention to spacing and check the file carefully before running the deployment command.

Environment variables are also important because they provide configuration values such as the database username, password, and database name. These settings help Nextcloud communicate with MariaDB. I realized that the values must match correctly, or the application may have difficulty connecting to the database. In actual cloud environments, sensitive credentials should be protected instead of being stored openly in configuration files.

I found the deployment process interesting because it showed me how different services can be started and connected with only a few commands. It gave me a better idea of how cloud storage systems can be managed using containers and automation.

Compared with Mission 1, I now understand cloud computing in a broader way. Before, I mainly thought about cloud services as a way to store files and access applications online. Now, I understand that cloud computing also involves configuring servers, connecting services, managing data, and automating deployments. This mission helped me develop my confidence in using Docker and encouraged me to practice more cloud technologies.
