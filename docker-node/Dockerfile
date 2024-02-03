FROM ubuntu
# First select a base image for example select an working env or OS

# it gives the commands which should run inside the base image/ container
RUN apt-get update
RUN apt-get install -y curl
RUN curl -sL https://deb.nodesource.com/setup_18.x | bash -
RUN apt-get upgrade -y
RUN apt-get install -y nodejs
WORKDIR /app agar yeah yse karte hai toh baar baar har command mai /app nhi likhna padega
COPY package.json package.json
# COPY package.json /app/package.json
COPY package-lock.json package-lock.json
# COPY package-lock.json /app/package-lock.json
    # after optimization it says that do npm run only when there is any change in the above 2 files. and agar hum sirf code ko hi change kar rhe hai toh waapis npm install kyun karna

# RUN cd app && npm install
# COPY main.js index.js
COPY main.js main.js
# COPY main.js /app/main.js
# COPY . .
# yaha se saari files utha k copy kar do, magar . . use karne se nodemodules and docker-compose bhi chalejaayega, so hume ek .dockerignore file bhi create karni padegi


ENTRYPOINT [ "node" ,"main.js" ]
# optimized approach
# FROM node

# COPY package.json package.json
# COPY package-lock.json package-lock.json
# # COPY main.js index.js

# COPY main.js main.js
# RUN npm install

# ENTRYPOINT [ "node" ,"main.js" ]

