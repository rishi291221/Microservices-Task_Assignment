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
<img width="469" height="138" alt="image" src="https://github.com/user-attachments/assets/9e1cb7d0-46ee-44c8-af83-5c7d6eab04bb" />



Include .dockerignore:
 

 <img width="940" height="585" alt="image" src="https://github.com/user-attachments/assets/5f5ff5f3-ef97-4eea-81ed-1130986eaf2f" />



Create docker-compose.yml
 <img width="940" height="623" alt="image" src="https://github.com/user-attachments/assets/9c036bc3-3016-49fc-82d9-c63bd03623a1" />


To build images using docker compose.yml
docker compose build --no-cache
To start containers
docker compose up -d
docker ps
 

 
     



Through Gateway all the services are reachable:
  
 <img width="940" height="282" alt="image" src="https://github.com/user-attachments/assets/78226e31-d354-415d-8bcb-e1c1caeb745f" />


Verification:

<img width="632" height="244" alt="image" src="https://github.com/user-attachments/assets/23d4fcbf-9b4c-4a0c-861b-e18da17c7e6a" />

<img width="673" height="214" alt="image" src="https://github.com/user-attachments/assets/90568749-e0c9-4c5b-b60f-94464f483b08" />


<img width="625" height="254" alt="image" src="https://github.com/user-attachments/assets/a5e60a07-b009-4b1f-8e11-59bba3f8bf9b" />

 
 <img width="659" height="239" alt="image" src="https://github.com/user-attachments/assets/f4c6cb83-4744-499d-b3e7-63695fd30441" />

<img width="726" height="214" alt="image" src="https://github.com/user-attachments/assets/aaaf5571-3f7b-4aad-9e6e-ba8a27830d91" />


<img width="940" height="269" alt="image" src="https://github.com/user-attachments/assets/8ce18804-b3de-4bfc-9afc-3e489c446d40" />

<img width="594" height="220" alt="image" src="https://github.com/user-attachments/assets/dd86462f-36c9-451e-af53-4b9572456dc3" />







     



Through Gateway all the services are reachable:
  
 




