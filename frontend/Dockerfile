FROM node:18-alpine AS build
WORKDIR /app 
COPY . .
RUN npm install
RUN npm run build 

# Serving the app with nginx
FROM nginx:alphine
COPY --from=build /app/dist /usr/share/nginx/html 
EXPOSE 80 
CMD ["nginx","-g","daemon off;"]
