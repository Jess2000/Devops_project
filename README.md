
# Devops final project

This is our devops final project.

## Opportunities

1. The DevOps project is based on all of the labs passed during the course, it is allowed to use them.

2. Work on the project can be carried out only by a group of 2 students or 1.

## Work performed

1. Create a web application

We take the webtech application project and we add some tests.
We use the draft application located in courses/devops/modules/04.continuous-testing/assets/userapi

2. Apply CI/CD pipeline

We chose to use Heroku for configure and apply CI/CD (including deployment).

3. Configure and provision a virtual environment and run your application using the IaC approach

We configure Vagrant and we we use Ansible.

4. Build Docker image of your application

We build our docker image of our application and we push it to Docker Hub.

5. Make container orchestration using Docker Compose

We create a docker-compose.yml file.

6. Make docker orchestration using Kubernetes

We create the 4 Kubernetes Manifest YAML files (deployment.yaml, persistentVolume.yaml, persistentVolumeClaim.yaml, service.yaml).

7. Make a service mesh using Istio

We deploy our application using Istio and we create virtualService.yaml.

8. Implement Monitoring to your containerized application

We started but not finished.

9. Document your project

## Usage

*how to start and use the application, run the tests, ...*

* Clone this repository, from your local machine:
  ```
  git clone https://github.com/Jess2000/Devops_project.git
  ```
* Install [Go](https://golang.org/) and [Dex](https://dexidp.io/docs/getting-started/). For example, on Ubuntu, from your project root directory:   
  ```
  # Install Go
  apt install golang-go
  # Build Dex
  cd dex
  make
  make examples
  ```
  Note, the provided `.gitignore` file ignores the `dex` folder.
* Register your GitHub application, get the `clientID` and `clientSecret` from GitHub and report them to your Dex configuration. Modify the provided `./dex-config/config.yml` configuration to look like:
  ```yaml
  - type: github
    id: github
    name: GitHub
    config:
      clientID: xxxx98f1c26493dbxxxx
      clientSecret: xxxxxxxxx80e139441b637796b128d8xxxxxxxxx
      redirectURI: http://127.0.0.1:5556/dex/callback
  ```
* Inside `./dex-config/config.yml`, the front-end application is already registered and CORS is activated. Now that Dex is built and configured, you can start the Dex server:
  ```yaml
  cd dex
  bin/dex serve dex-config/config.yaml
  ```
* Start the back-end
  ```bash
  cd back-end
  # Install dependencies (use yarn or npm)
  yarn install
  # Optional, fill the database with initial data
  bin/init
  # Start the back-end
  bin/start
  ```
* Start the front-end
  ```bash
  cd front-end
  # Install dependencies (use yarn or npm)
  yarn install
  # Start the front-end
  yarn start
  ```

## Learn More

You can learn more in the [Create React App documentation](https://facebook.github.io/create-react-app/docs/getting-started).

To learn React, check out the [React documentation](https://reactjs.org/).

[Gitlab on CentOS](https://about.gitlab.com/install/#centos-7)

[Vagrant documentation](https://www.vagrantup.com/docs)

[Heroku Deploy documentation](https://github.com/marketplace/actions/deploy-to-heroku#getting-started)

[Docker documentation](https://docs.docker.com/develop/)

[Docker Hub](https://hub.docker.com/)

## Author

AUVE Jessica [jessica.auve@edu.ece.fr](mailto:jessica.auve@edu.ece.fr)

BENZEKRI Aicha [aicha.benzekri@edu.ece.fr](mailto:aicha.benzekri@edu.ece.fr)