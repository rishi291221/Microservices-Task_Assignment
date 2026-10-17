Pull the files from Git.

 <img width="940" height="291" alt="image" src="https://github.com/user-attachments/assets/ae389f41-18aa-4c5b-bcb6-2779e839f3bf" />


Create a docker file based on service.
Gateway service – 3000 

FROM node:20-alpine
WORKDIR /app
COPY package*.json ./
RUN npm install 
COPY . .
EXPOSE 3000
CMD ["node", "app.js"]
--------------------------------------------
User service – 3001

FROM node:20-alpine
WORKDIR /app
COPY package*.json ./
RUN npm install 
COPY . .
EXPOSE 3001
CMD ["node", "app.js"]
---------------------------------------------
Product service- 3002
FROM node:20-alpine
WORKDIR /app
COPY package*.json ./
RUN npm install 
COPY . .
EXPOSE 3002
CMD ["node", "app.js"]





Order service-3003
FROM node:20-alpine
WORKDIR /app
COPY package*.json ./
RUN npm install 
COPY . .
EXPOSE 3003
CMD ["node", "app.js"]



Include .dockerignore:
 

 


Create docker-compose.yml
 

To build images using docker compose.yml
docker compose build --no-cache
To start containers
docker compose up -d
docker ps
 

 
     



Through Gateway all the services are reachable:
  
 




