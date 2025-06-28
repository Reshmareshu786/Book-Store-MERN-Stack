FROM node:18-alpine 
WORKDIR /app
COPY package*.json ./
RUN npm install --production

# Copying the rest of the app files
COPY . .

# Expose the app port
EXPOSE 5555

# To run the app
CMD ["node","index.js"]