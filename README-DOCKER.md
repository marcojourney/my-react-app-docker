docker build -t my-react-app . [Default will access Dockerfile]
docker build -t my-react-dev -f ./Dockerfile.DEV .
docker build -t my-react-prod -f ./Dockerfile.PROD .
docker run -p 8080:3000 your-image-name [port 3000 link to your react app port]
   .n container name
   .p binding port
   .v volumes
   .d detach (for run in background)
docker run -d --name my-react-app-1 -p 8080:3000 -v $(pwd):/usr/src/app/ my-react-app [mount localhost to inside docker container]
docker run -d --name my-react-prod-1 -p 80:80 my-react-prod