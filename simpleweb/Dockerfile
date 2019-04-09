# Specify a base image 
# FROM alpine npm is not installed in alpine image 
# find an image with npm already installed 
# apline is the most striped down image possible in the docker world 
FROM node:alpine 

# make sure that all build files are avalible 
WORKDIR ./usr/app 
# Only copy over the package.json file 
COPY ./package.json ./
# Install some dependencies 
RUN npm install 
# copy the rest 
COPY ./ ./

# Default command 
CMD ["npm", "start"]
