# Set the base image
FROM node:12
# Create app directory
WORKDIR /usr/src/app
#Define the environment variables
ENV POSTGRESS_USERNAME=udagramamiteshdev
ENV POSTGRESS_PASSWORD=PostGres#2020
ENV POSTGRESS_DB=udagramamiteshdev
ENV POSTGRESS_HOST=udagramamiteshdev.cejeaasmtagr.ap-south-1.rds.amazonaws.com
ENV AWS_REGION=ap-south-1
ENV AWS_PROFILE=default
ENV AWS_BUCKET=udagram-amitesh-dev
ENV JWT_SECRET=helloworld
# Copy package.json AND package-lock.json
COPY package*.json ./
# Install all dependencies
RUN npm ci 
# Copy the rest of the code
COPY . .
# Expose the port 
EXPOSE 8080
# Define the command that should be executed
CMD [ "npm", "run", "dev" ]