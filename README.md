# Setup

## Installation

Download Docker desktop from [here](https://www.docker.com/products/docker-desktop/). And follow all the instruction guidelines. Make sure to choose correct version of installer for Windows (AMD64 in my case).
After installing make sure to restart the system and later open command prompt and run the command `docker version`. This should render the client and server information.

Search for the required Docker images from the docker hub (Eg: selenium/standalone-chrome) using the command `docker pull selenium/standalone-chrome` on the command prompt

Later run this command `docker run -d -p 4444:4444 --shm-size="2g" selenium/standalone-chrome:latest` The meaning of command can be found here
is used to run a **Selenium Grid standalone Chrome container** with specific configurations. Let’s break it down:


`docker run` - This command starts a new container from the specified image (`selenium/standalone-chrome:latest`).

`-d` - Runs the container in **detached mode**, meaning it runs in the background, and the terminal is not blocked by the container's output.

`-p 4444:4444` - Maps port **4444** on the **host** to port **4444** on the **container**.

*   The first `4444` is the port on your **local machine** (host).
*   The second `4444` is the port inside the **container** where the Selenium server is listening.
*   This allows you to access Selenium Grid at `http://localhost:4444`.

`--shm-size="2g"` - Sets the **shared memory size** of the container to **2 GB**.

*   By default, Docker containers have a small `/dev/shm` (shared memory) size, which can cause issues with Chrome (e.g., crashes or freezing) when running tests.
*   Increasing it to `2g` improves the performance and stability of the Chrome browser inside the container.

`selenium/standalone-chrome:latest` - Specifies the Docker image to use.

*   **`selenium/standalone-chrome`** is a Selenium image with a standalone Selenium server and the Chrome browser pre-installed.
*   **`:latest`** is the image tag, which pulls the latest version of the image from Docker Hub.



#### **Purpose of This Command**

*   This command runs a **Selenium standalone Chrome** instance in a Docker container, exposing it on port 4444, ready to accept test automation commands.
*   It is commonly used for running browser-based automation tests in environments where Chrome needs to run in isolation or headlessly.


#### Accessing Selenium Grid

Once the container is running, you can access Selenium Grid through your browser or automation framework at:

```arduino
http://localhost:4444
```


The dependecies used in this project.

Docker notes can be found [here](/notes/DOCKER.MD)

Project notes can be found [here](https://docs.google.com/document/d/1wtYo19RYvx8xaSh4Pe7NWwsF6ORW-cE1qKrE8W6hlKA/edit)
