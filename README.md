# Requirements

To build and run this app locally you will need to install the following:

- Install [Node.js](https://nodejs.org/en/)
- Install [MongoDB](https://docs.mongodb.com/manual/installation/)

# Getting started

- Clone the repository

```
git clone https://github.com/aagalyoon/WeatherStationAPI
```

- Install dependencies

```
cd WeatherStationAPI
npm install
```

- Configure your mongoDB server

```bash
# create the db directory
sudo mkdir -p /data/db
# give the db correct read/write permissions
sudo chmod 777 /data/db

# starting from macOS 10.15 even the admin cannot create directory at root
# so lets create the db directory under the home directory.
mkdir -p ~/data/db
# user account has automatically read and write permissions for ~/data/db.
```

- Start your mongoDB server (you'll probably want another command prompt)

```bash
mongod

# on macOS 10.15 or above the db directory is under home directory
mongod --dbpath ~/data/db
```

- Build and run the project

```
npm run build
npm start
```

# API Documentation

- GET call or Navigate in a browser to `http://localhost:3000` and you should see the API documentation!
<img width="682" alt="Screenshot 2023-03-20 at 1 46 50 AM" src="https://user-images.githubusercontent.com/112532004/226257328-58f777a9-2af7-43a5-88da-657fa64d6647.png">

# Unit Tests

```
npm run test
```

# Docker Container

```
docker-compose up --build
docker-compose run --rm app npm run test
```
