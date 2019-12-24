FROM node:12
ENV POSTGRES_USERNAME="username"
ENV POSTGRES_PASSWORD="userpass"
ENV POSTGRES_DATABASE="db"
ENV POSTGRES_HOST="host.rds.amazonaws.com"
ENV AWS_REGIONS="us-east-1"
ENV AWS_PROFILE="default"
ENV AWS_MEDIA_BUCKET="username"
ENV JWT_SECRET="jwt_secret"
# Create app directory
WORKDIR /usr/src/app
# Install app dependencies
# A wildcard is used to ensure both package.json AND package-lock.json are copied
# where available (npm@5+)
COPY package*.json ./
RUN npm ci
# Bundle app source
COPY . .
EXPOSE 8081
CMD [ "npm", "run", "dev" ]