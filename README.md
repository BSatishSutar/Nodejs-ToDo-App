# node-todo-cicd

Run these commands for Ubuntu machine:


`sudo apt install nodejs`


`sudo apt install npm`


`npm install`

`node app.js`

or Run by docker compose

test


# Run these commands if you are using Amazon Linux-2 machine, to install nodejs and npm:

yum update -y

curl -sL https://rpm.nodesource.com/setup_14.x | sudo bash -

yum install -y nodejs

node -v

npm -v

sudo yum groupinstall -y "Development Tools"

yum install npm

npm -v

npm install

npm ci

npm audit

npm audit fix

npm audit fix --force

# Dockerfile

FROM node:12.2.0-alpine

WORKDIR /app

COPY . .

RUN npm install
RUN npm run test

EXPOSE 8000

CMD ["node", "app.js"]




