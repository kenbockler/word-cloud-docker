# Word Cloud Docker

Welcome to the Word Cloud Docker repository! This project provides a microservices architecture for the Word Cloud application, designed for easy deployment using Docker.

The application uses PostgreSQL and RabbitMQ services deployed via Docker, and consists of three microservices: Core, Worker, and Frontend.

## Services

* **PostgreSQL**: Database service for storing word occurrence statistics.
* **RabbitMQ**: Message queue service for transferring messages from Core to Worker.
* **Core**: Spring Boot-based microservice providing REST/JSON API for Frontend, and communicates with RabbitMQ and PostgreSQL. GitHub repository: https://github.com/kenbockler/word-cloud-core
* **Worker**: Spring Boot-based microservice for processing text file content, counting word occurrences, and storing statistics in the database. GitHub repository: https://github.com/kenbockler/word-cloud-worker
* **Frontend**: React.js-based user interface for uploading text files and displaying word clouds. GitHub repository: https://github.com/kenbockler/word-cloud-frontend

## Installation

1. Ensure you have [Docker](https://docs.docker.com/get-docker/) and [Docker Compose](https://docs.docker.com/compose/install/) installed.

2. Clone the repository:

    ```
    git clone https://github.com/yourusername/word-cloud-docker.git
    ```

3. Navigate to the cloned repository folder:

    ```
    cd word-cloud-docker
    ```



4. Start the application:
    ```
    docker-compose up -d
    ```

This will start all services and applications in Docker containers. Once all containers have successfully started, the Word Cloud application will be accessible in your browser at http://localhost.

## Usage

Once the application is running, you can use the user interface to:

* Upload a text file (up to 100 MB in size).
* Obtain an identifier to use for displaying word occurrence statistics and word cloud.
* View word occurrence statistics in JSON format.
* Generate and view the word cloud.

## Contributing

If you'd like to improve or extend the project, your contributions are welcome! Please create a new branch and make a pull request with your changes.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
