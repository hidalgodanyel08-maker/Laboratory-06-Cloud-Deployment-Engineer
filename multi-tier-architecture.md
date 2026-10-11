# Understanding Multi-Tier Architecture

## Definition of Two-Tier Architecture

A two-tier architecture divides an application into two main components: the application tier and the database tier. Each component has a different task, but they communicate to provide the services needed by users. In my activity, I used Nextcloud and MariaDB to demonstrate this type of architecture.

## The Web/Application Tier

The application tier is the part that processes user requests and provides the interface that users see in their browsers. Nextcloud serves this purpose in my deployment. It allows users to access the cloud storage interface and sends requests to the database when information is needed.

## The Database Tier

The database tier is responsible for keeping and managing the application's information. MariaDB stores data used by Nextcloud, including account information and file-related metadata. It helps the application retrieve information when users interact with the system.

## Why Separate the Two Tiers?

Separating the application and database makes the system easier to maintain because each service has its own purpose. If the application needs an update, I can manage its container separately from the database container. This design also makes it easier to adjust the resources or configuration of each service when the application grows.

## Components of the Deployment

| Component      | Purpose                                          |
| -------------- | ------------------------------------------------ |
| Nextcloud      | Provides the cloud storage web interface         |
| MariaDB        | Stores application data                          |
| Docker Compose | Manages the containers together                  |
| Port 8080      | Provides browser access to Nextcloud             |
| `database`     | Service name used by Nextcloud to locate MariaDB |

## What I Learned

I learned that separating application components helps organize a system and makes it easier to manage. Both containers have different responsibilities, but they need to communicate correctly for the application to work.
