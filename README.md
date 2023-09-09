# docker-projects
This is a repository for my docker projects

# Jupiter Web Application

Jupiter is a web application hosted using the Apache HTTP Server on Amazon Linux. This repository provides a Dockerized setup for the application, ensuring consistent deployment across various environments.

## Prerequisites

- [Docker](https://www.docker.com/get-started) installed on your machine.

## Dockerfile Breakdown

- **Base Image**: Uses the latest version of Amazon Linux.
- **Dependencies**: Installs the Apache HTTP Server, `wget` for downloading files, and `unzip` for extracting zip files.
- **Web Files**: Downloads and sets up web files from the `jupiter` repository.
- **Port**: Exposes port 80 for the Apache HTTP Server.
- **Entry Point**: The default application that runs when the container starts is the Apache HTTP Server.

## Getting Started

1. **Clone the Repository**:

   ```bash
   git clone https://github.com/azeezsalu/jupiter.git
   cd jupiter
   ```

2. **Build the Docker Image**:

   Navigate to the root directory of the project where the `Dockerfile` is located and run:

   ```bash
   docker build -t jupiter-webapp .
   ```

   This will build a Docker image named `jupiter-webapp`.

3. **Run the Container**:

   Once the image is built, you can start a container:

   ```bash
   docker run -d -p 8080:80 jupiter-webapp
   ```

   This command runs the container in detached mode, mapping port 8080 on your host to port 80 on the container.

4. **Access the Application**:

   Open a web browser and navigate to:

   ```
   http://localhost:8080
   ```

   Here We Go! You should now see the Jupiter web application running.

5. **Issues**:

   If you encounter any issues, please open an issue on the GitHub repository.
