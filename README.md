# Simple Project to Learn Docker

## Installation

1. Install Docker on your PC.

## Usage

1. Download an image: 
    ```
    docker pull [image name]
    ```

2. Create a container for the new image: 
    ```
    docker create --name [container name] [image]
    ```

3. Start the container with the container name: 
    ```
    docker start [container name]
    ```

4. Show and follow logs: 
    ```
    docker logs --follow [container name]
    ```

5. Check running containers: 
    ```
    docker ps
    ```

6. Stop a running container: 
    ```
    docker stop [container name]
    ```

7. Show all containers: 
    ```
    docker ps -a
    ```

8. Delete a container: 
    ```
    docker rm [container name]
    ```

## Port Mapping

When you run a Docker container, you can expose ports within the container to be accessed from outside the container by mapping those ports to ports on the host (the machine running Docker).

For example, if you have a web application inside a Docker container running on port 8080 within the container, you can map that port to port 8080 on the host. This means that any request that arrives at port 8080 on the host will be redirected to the Docker container, thus allowing access to the web application.

```docker create -p [host port]:[container port] [container name] [image]```


## Docker Run

1. Find the image, if not found, this command creates it: 
    ```
    docker run --name [container name] -p [host port]:[container port] -d [image]
    ```

2. Initialize the container:
    ```
    docker start [container name]
    ```
    
