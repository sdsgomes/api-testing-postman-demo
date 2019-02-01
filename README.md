# API testing with Postman
This repository contains the presentation and demo contents I presented at the talk I gave in Quality Talks on the 31st January 2019, in Lisbon.
The first part of the talk was a presentation focusing on the advantages of API testing and how we can leverage it in test automation.
The second part was a demo where I showed how we can automate API tests using Postman and how we can run Postman collections in Docker containers. I used [Sendgrid's API](https://sendgrid.com/docs/api-reference/) for this demo.

## Contents
You can find the presentation [here](./presentation/QualityTalksJanuary.pdf).
The Postman collection is on the [collections folder](./collections) and the environment variables are on the file on [envrionments folder](./environments).
There is a docker-compose file on the root directory that allows to run Postman collections in Docker containers.
Finally, I used Circle CI as a continuous integration tool to run the collections each time a new commit is added to this repo. You can find the Circle CI configurations [here](.circleci/config.yml).

## Running Postman collections using Docker
To run the collection in a Docker container, you need to have [Docker](https://www.docker.com/get-started) installed as well [docker-compose](https://docs.docker.com/compose/install/), which a tool that allows to easily manage Docker containers. Then, you just need to run the following command on the directory that contains the `docker-compose.yml` file.
```
docker-compose up
```