# Docker

Project notes can be found [here](https://docs.google.com/document/d/1wtYo19RYvx8xaSh4Pe7NWwsF6ORW-cE1qKrE8W6hlKA/edit)


Docker is a platform designed to help developers build, deploy, and manage applications in a consistent environment called containers. Containers package up an application and all of its dependencies, making it easy to run the application on any environment, whether it's a developer's laptop, a test server, or a production server in the cloud.

Here are some core concepts:

![docker registry](https://github.com/user-attachments/assets/a7d9e152-9872-4048-9772-7741ea0dfb32)

1.  **Containers**: Containers are lightweight, stand-alone packages that include everything needed to run a piece of software, including the code, runtime, system tools, libraries, and settings. They are isolated from each other and the host machine, which makes them portable across environments.

2.  **Docker Images**: A Docker image is a lightweight, standalone, executable package that includes the application code and its dependencies. It’s a read-only template used to create containers. You can think of it as a blueprint for running your application.

3.  **Docker Engine**: The Docker Engine is the core component that manages containers. It runs on the host OS, providing services for building, starting, and stopping containers.

4.  **Dockerfile**: A Dockerfile is a text file with instructions on how to build a Docker image. You define the base image, install dependencies, add application code, and configure settings here.

5.  **Docker Hub**: Docker Hub is a cloud-based registry where you can find pre-built images shared by others or upload your own images for easy sharing and reuse.


Docker is widely used in DevOps, continuous integration/continuous deployment (CI/CD), and microservices architectures because it simplifies application deployment and ensures consistency across environments.

