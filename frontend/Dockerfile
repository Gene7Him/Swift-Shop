FROM node:18

WORKDIR /app

# Copy package.json and package-lock.json
COPY package*.json ./

# Install dependencies
RUN npm install

# Copy the rest of the application
COPY . .

# Build the application
RUN npm run build

# Expose the port the app runs on
EXPOSE 5173

# Command to run the application
CMD ["npm", "run", "preview", "--", "--host", "0.0.0.0"]