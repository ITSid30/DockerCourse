# to create image based on a parent image this dockerfile is used

# Parent Layer
FROM node:16-alpine  

RUN npm install -g nodemon

# to set workingDir to run commands in folder
# every instructions below this will havve relative path as /app
WORKDIR /app

# make caching upto 3 layers to npm install to save build time
COPY package.json .

# to run commmands at compile time
RUN npm install 

# set the path of files at which dockerFile is present to copy in destination path = '/app'
COPY . .

# what port is going to be exposed by container
EXPOSE 4000

# to run commands at Runtime ie. when container runs
# CMD ["node", "app.js"]

# to create volumes to watch for changes 
CMD ["npm", "run", "dev"]