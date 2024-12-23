# Flask Application with Jenkins CI Pipeline

This project is a simple Flask web application integrated with a Jenkins CI pipeline. The goal of the project is to automate the process of building, testing, and deploying the application every time a change is pushed to the repository. The CI pipeline runs automated tests each time a commit is made, ensuring the integrity of the application.

## Features

- **Flask Web Application**: A minimal Flask app with basic functionality.
- **Jenkins CI Pipeline**: A Jenkins pipeline that automatically triggers on every push to the GitHub repository.
- **Automated Testing**: The pipeline runs automated tests using `pytest` to ensure code quality and reliability.
- **Docker Integration**: The pipeline builds and tests the application inside a Docker container to ensure consistency across different environments.

## CI/CD Pipeline Breakdown

1. **Clone Repository**: The pipeline starts by cloning the repository from GitHub.
2. **Build Docker Image**: The pipeline builds a Docker image for the Flask application using the Dockerfile.
3. **Run Tests**: It runs the test suite inside the Docker container to validate that the application works as expected.
4. **Login to Docker Hub**: After successful tests, the pipeline logs into Docker Hub using credentials stored securely in Jenkins.
5. **Push Docker Image**: (Optional, if you choose to extend the pipeline) Pushes the Docker image to Docker Hub for deployment purposes.

## Setup and Installation

1. **Clone the repository**:
    ```bash
    git clone https://github.com/yourusername/your-repo.git
    ```

2. **Set up Jenkins**:
    - Install Jenkins on your local machine or server.
    - Set up a Jenkins pipeline in your Jenkins instance.
    - Integrate your GitHub repository with Jenkins using a webhook.
    - Configure your Jenkinsfile to automate the build, test, and deploy processes.

3. **Configure Docker**:
    - Ensure Docker is installed and running on the machine where Jenkins is running.
    - Create a `Dockerfile` for your Flask app if you don't have one.

4. **Push Changes to GitHub**:
    - Whenever you push changes to your GitHub repository, the Jenkins pipeline will automatically be triggered to build the Docker image and run tests.

## Technologies Used

- **Flask**: A lightweight WSGI web application framework in Python.
- **Jenkins**: An open-source automation server used for building, testing, and deploying applications.
- **Docker**: A platform that uses containerization to package and deploy applications.
- **Pytest**: A framework that makes building simple and scalable test cases easy.

## Contributing

Feel free to fork this repository, open an issue, or submit a pull request with improvements or bug fixes. Contributions are always welcome!

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

