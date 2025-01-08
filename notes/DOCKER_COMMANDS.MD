# Docker Commands

In Docker, the `--help` option is used to display detailed information and usage instructions for a specific Docker command. It's a quick way to access a command's documentation directly from the terminal.

### General Syntax

```bash
docker <command> --help
```

**Command-Specific Help**  
    Provides detailed information about the options, flags, and usage of a specific Docker command.

    `docker run --help` 
 would return the below output
    
    Usage:  docker run [OPTIONS] I MAGE [COMMAND] [ARG...]
    Run a command in a new container
    
    Options:
      -d, --detach              Run container in background and print container ID
      -e, --env list            Set environment variables
      -i, --interactive         Keep STDIN open even if not attached
      ...
    


### Benefits of `--help`

*   **Discover available commands** and their options.
*   **Learn about specific flags** and their functionality.
*   **Troubleshoot command usage** errors by understanding proper syntax.

Would you like to explore any specific Docker command in more detail?

### **1. Docker Installation and Version Info**
| **Command**                       | **Description**                                 |
|------------------------------------|-------------------------------------------------|
| `docker version`                   | Displays the Docker client and server version.  |
| `docker info`                      | Provides detailed system-wide information about Docker. |
| `docker --help`                    | Displays help for Docker commands.              |

---

### **2. Docker Image Commands**
| **Command**                       | **Description**                                 |
|------------------------------------|-------------------------------------------------|
| `docker pull <image>`              | Downloads an image from Docker Hub.             |
| `docker images`                    | Lists all the images on the local system.       |
| `docker rmi <image>`               | Removes an image from the local system.         |
| `docker build -t <name>:<tag> .`   | Builds an image from a Dockerfile in the current directory. |
| `docker tag <image> <new-tag>`     | Tags an image with a new name or version.       |
| `docker history <image>`           | Shows the history of an image’s layers.         |
| `docker inspect <image>`           | Displays detailed information about an image.   |

---

### **3. Docker Container Commands**
| **Command**                              | **Description**                                 |
|-------------------------------------------|-------------------------------------------------|
| `docker run <image>`                      | Runs a container from an image.                 |
| `docker run -d <image>`                   | Runs a container in detached mode (background). |
| `docker run -it <image>`                  | Runs a container in interactive mode with a terminal. |
| `docker ps`                               | Lists running containers.                       |
| `docker ps -a`                            | Lists all containers, including stopped ones.   |
| `docker stop <container>`                 | Stops a running container.                      |
| `docker start <container>`                | Starts a stopped container.                     |
| `docker restart <container>`              | Restarts a running container.                   |
| `docker kill <container>`                 | Forcefully stops a container.                   |
| `docker rm <container>`                   | Removes a stopped container.                    |
| `docker logs <container>`                 | Displays the logs of a container.               |
| `docker exec -it <container> <command>`   | Executes a command inside a running container.  |
| `docker inspect <container>`              | Displays detailed information about a container.|
| `docker attach <container>`               | Attaches to a running container's terminal.     |
| `docker cp <container>:<path> <local>`    | Copies files from a container to the host or vice versa. |

---

### **4. Docker Network Commands**
| **Command**                         | **Description**                                 |
|--------------------------------------|-------------------------------------------------|
| `docker network ls`                  | Lists all Docker networks.                      |
| `docker network create <name>`       | Creates a new network.                          |
| `docker network inspect <network>`   | Displays detailed information about a network.  |
| `docker network connect <network> <container>` | Connects a container to a network.         |
| `docker network disconnect <network> <container>` | Disconnects a container from a network.  |

---

### **5. Docker Volume Commands**
| **Command**                        | **Description**                                 |
|-------------------------------------|-------------------------------------------------|
| `docker volume ls`                  | Lists all Docker volumes.                       |
| `docker volume create <name>`       | Creates a new volume.                           |
| `docker volume inspect <volume>`    | Displays detailed information about a volume.   |
| `docker volume rm <volume>`         | Removes a volume.                               |

---

### **6. Docker Compose Commands**
| **Command**                        | **Description**                                 |
|-------------------------------------|-------------------------------------------------|
| `docker-compose up`                 | Builds and starts the services defined in `docker-compose.yml`. |
| `docker-compose up -d`              | Starts services in detached mode (background).  |
| `docker-compose down`               | Stops and removes containers, networks, and volumes. |
| `docker-compose ps`                 | Lists containers managed by Compose.            |
| `docker-compose logs`               | Displays logs of all services.                  |
| `docker-compose exec <service> <command>` | Runs a command inside a service container. |

---

### **7. Docker System Commands**
| **Command**                         | **Description**                                 |
|--------------------------------------|-------------------------------------------------|
| `docker system df`                   | Shows the amount of disk space used by Docker.  |
| `docker system prune`                | Removes unused data (containers, images, networks, and volumes). |
| `docker system events`               | Streams real-time Docker events.                |
| `docker stats`                       | Displays real-time resource usage of running containers. |

---

### **8. Docker Login & Registry Commands**
| **Command**                         | **Description**                                 |
|--------------------------------------|-------------------------------------------------|
| `docker login`                       | Logs in to a Docker registry (e.g., Docker Hub).|
| `docker logout`                      | Logs out from a Docker registry.                |
| `docker push <image>`                | Pushes an image to a Docker registry.           |
| `docker search <term>`               | Searches for images in Docker Hub.              |

---

### **9. Docker Save and Load Commands**
| **Command**                         | **Description**                                 |
|--------------------------------------|-------------------------------------------------|
| `docker save -o <file>.tar <image>`  | Saves an image to a tar archive.                |
| `docker load -i <file>.tar`          | Loads an image from a tar archive.              |

---

### **10. Docker Export and Import Commands**
| **Command**                         | **Description**                                 |
|--------------------------------------|-------------------------------------------------|
| `docker export -o <file>.tar <container>` | Exports a container’s filesystem to a tar archive. |
| `docker import <file>.tar <image>`   | Imports a tar archive as an image.              |

---