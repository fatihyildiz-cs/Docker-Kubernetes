# Specify a base image that includes node.js
FROM node:alpine

# Specify working directory to have the files
# in one place and not overwrite system files.
WORKDIR /usr/app

# this is now relative to the WORKDIR specified above
# we are copying files in 2 steps because we don't want
# to install all dependencies everytime we change
# index.js
COPY ./package.json ./

#Install some dependencies
RUN npm install

# copy rest of the files
COPY ./ ./

#Default command
CMD ["npm", "start"]