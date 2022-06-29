## App Info

This is a Node and Express web application built to run in a Docker container.
It's purpose is to be run by an Azure Web App service.

 - Notice that this repo contains a script file named collectionsDataUploader.js, which is used to
   be manually run in order to upload NFT collections data into MongoDB


## Example of usage
    After making your changes, you can test them locally by:
      1. Building the docker image file: docker build -t <Login server>/<Repository name (image name)>:latest .
         * <Login server> is taken from Azure::ContainerRegistry::<your container instance>::Access Keys::Login server
          - example: docker build -t feapi.azurecr.io/legendao-fe-api:latest .

      2. docker run -d -p 8080:<config.js port> <Login server>/<Repository name (image name)>
          - example: docker run -d -p 8080:3001 feapi.azurecr.io/legendao-fe-api

      3. Go to your browser to test it: http://localhost:8080/token/info


    In order to upload your changes to the Azure Web App:
      1. Login: docker login <Login server>
          - example: docker login feapi.azurecr.io
          * The user name and password are taken from Azure::ContainerRegistry::<your container instance>::Access Keys...

