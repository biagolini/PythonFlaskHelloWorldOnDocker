# Flask Tutorial: Hello World

Welcome to this Flask tutorial! In this guide, you'll learn how to set up a simple Flask web app using Docker on Windows 11. After setting up, you'll be able to access the web app from your host machine.

## Prerequisites

- Docker installed on Windows 11.
- Docker Desktop configured and running.

## Setup Project

Python projects typically utilize virtual environments to prevent package conflicts. However, when using Docker, we can leverage containerization to isolate our application and its dependencies.

### Create Virtual Environment

1. **Open a Terminal** on WindowsM.

2. **Create a Project Directory**:

```bash
mkdir PythonFlaskHelloWorld
cd PythonFlaskHelloWorld
```

3. **Create Dockerfile**: Here, you'll define the base image, set up the working directory, copy the requirements file, install the necessary packages, and specify the command to run the Flask app. Refer to the `Dockerfile` file in this repository to view the code.

4. **Create requirements.txt file**: This file will list the Python packages required for your Flask app, such as Flask itself. Refer to the `requirements.txt` file in this repository to view the code.

5. **Create Your Flask App**: Create a file named `app.py`. Refer to the `app.py` file in this repository to view the code.

6. **Construa a imagem Docker**:

```bash
docker build -t flask-hello-world .

```

7. **Run Your Flask App**:

```bash
docker run -p 5000:5000 flask-hello-world
```

8. **Access the Flask App from Your Host**: On your host machine, open a web browser and navigate to: `http://localhost:5000/`.

# Explore Alternative Deployment Options

As you dive into the world of Flask deployment, it's essential to be aware of the various methods available. Depending on your project requirements, infrastructure, and familiarity, you might find one method more suitable than the other. We've provided tutorials for two popular deployment methods: using Virtual Machines (VM) and Docker containers. 

- **Using VM**: If you're currently exploring the Docker-based tutorial, you might want to check out the VM-based deployment method. It provides a more traditional approach, allowing you to deploy your Flask app inside a Fedora 38 Virtual Box VM hosted on Windows 11. Learn more about this method [here](https://github.com/biagolini/PythonFlaskHelloWorldOnVM).

- **Using Docker**: If you're on the VM-based tutorial, consider exploring the Docker-based deployment. Docker offers a containerized solution, ensuring that your app and its dependencies are isolated, making it a popular choice for modern deployments. Dive into the Docker tutorial [here](https://github.com/biagolini/PythonFlaskHelloWorldOnDocker).

By familiarizing yourself with both methods, you can make an informed decision on which deployment strategy aligns best with your project needs.

# Git repository config

To automatically create a .gitignore file for a Python project, you can use the git command to generate a .gitignore file:

1. Initialize a new git repository (if you haven't already)

```bash
git init
```

2. Use the following command to create a .gitignore

```bash
git config --global alias.ignore '!gi() { curl -sL https://www.gitignore.io/api/$@ ;}; gi'
```

3. Now, you can generate the .gitignore file with:

```bash
git ignore python > .gitignore
```

# Reference

Pythonbasics (2023) Flask Tutorial: Hello World. Retrieved from: https://pythonbasics.org/flask-tutorial-hello-world/ (Accessed: 2023-10-03).
