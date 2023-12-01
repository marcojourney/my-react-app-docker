# Getting Started with Create React App + Docker

## Development

In your root project directory, you can run:

Build an Image
### `docker build -t my-react-dev -f ./Dockerfile.DEV .`

Run Container
### `docker run -d --name my-react-app-1 -p 8080:3000 -v $(pwd):/usr/src/app/ my-react-dev`

## Production

Build an Image
### `docker build -t my-react-prod -f ./Dockerfile.PROD .`

Run Container
### `docker run -d --name my-react-prod-1 -p 80:80 my-react-prod`

## Using Docker Swarm
