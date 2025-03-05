# Docker

Project notes can be found [here](https://docs.google.com/document/d/1wtYo19RYvx8xaSh4Pe7NWwsF6ORW-cE1qKrE8W6hlKA/edit)


Docker is a platform designed to help developers build, deploy, and manage applications in a consistent environment called containers. Containers package up an application and all of its dependencies, making it easy to run the application on any environment, whether it's a developer's laptop, a test server, or a production server in the cloud.

Here are some core concepts:

![docker registry](https://github.com/user-attachments/assets/a7d9e152-9872-4048-9772-7741ea0dfb32)

1.  **Containers**: Containers are lightweight, stand-alone packages that include everything needed to run a piece of software, including the code, runtime, system tools, libraries, and settings. They are isolated from each other and the host machine, which makes them portable across environments. This can be considered same as instance or objects in java.

2.  **Docker Images**: A Docker image is a lightweight, standalone, executable package that includes the application code and its dependencies. It’s a read-only template used to create containers. You can think of it as a blueprint for running your application. This can be considered as .class files in java which are compiled form .java files

3.  **Docker Engine**: The Docker Engine is the core component that manages containers. It runs on the host OS, providing services for building, starting, and stopping containers.

4.  **Dockerfile**: A Dockerfile is a text file with instructions on how to build a Docker image. You define the base image, install dependencies, add application code, and configure settings here. This file need not have any extension but sometimes `.dockerfile` or `.txt` is used for that. This can be considered as .java files in java where we have instructions written.

5.  **Docker Hub**: Docker Hub is a cloud-based registry where you can find pre-built images shared by others or upload your own images for easy sharing and reuse. It is similar to Maven


Docker is widely used in DevOps, continuous integration/continuous deployment (CI/CD), and microservices architectures because it simplifies application deployment and ensures consistency across environments.

Docker Commands Can be found [here](/notes/DOCKER_COMMANDS.MD). In order to run docker commands

Docker namespace is used to create a unique name for the container. It is used to avoid conflicts with other containers. The namespace is optional and can be used with the `--name` flag. If not provided, Docker will generate a random name for the container.

Docker names its containers using a combination of an **adjective** and a **famous scientist, mathematician, or hacker's last name**. This is done through the [`moby/moby`](https://github.com/moby/moby) project's `namegenerator` utility.

For example, `boring_varahamihira` follows this pattern:

*   **"boring"** → A randomly chosen adjective.
*   **"varahamihira"** → The name of an Indian mathematician and astronomer (6th century AD).

### How Docker Generates Names:

1.  If a name is **not specified** when creating a container, Docker assigns one automatically.
2.  Docker picks a **random adjective** from a predefined list.
3.  It picks a **random scientist's last name** from another predefined list.
4.  The two are combined with an **underscore** (`_`) in between.
5.  If the combination is already taken, Docker retries until it finds a unique name.

### How to Assign a Custom Name:

You can override this default naming by using the `--name` flag when running a container:

```sh
docker run --name my_container alpine
```





# Interesting points

* Docker is genrally built to run only on Linux machine. So, when you run Docker on Windows, it's actually running inside a small Linux VM (either WSL or Hyper-V), even though you interact with it from Windows. This abstraction makes it look like Docker is running natively.
