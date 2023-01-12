# Instructions to execute when _building_ an image
FROM node

# where to be in the image
WORKDIR /app

COPY package.json /app

# make sure the image working directory is correct
# RUN this command on image create
RUN npm install

# optimize the ordering to cache the image layer result prior

# copy this current directory to the root directory of the image
# COPY . . 
# put things into a "/app" dir in the image. Explicit path
COPY . /app



# indicate what port needs to be available for the image to access
# optional to declare but recommended for documentation 
EXPOSE 80

# on image instantiation, run this command
CMD ["node", "server.js"]