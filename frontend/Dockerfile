#Build phase 
FROM node:alpine  as builder 
WORKDIR ./app/
COPY package.json ./  
RUN npm install 
COPY ./ ./ 
RUN npm run build 

# Run phase 
FROM nginx as run 
EXPOSE 80 
COPY --from=builder ./app/build/ ./usr/share/nginx/html
# nginx starts automatically 
