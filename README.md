This project was bootstrapped with [Create React App](https://github.com/facebook/create-react-app).

## Available Scripts

Develop with Docker-compose.yml

```$xslt
# for local development
version: '3.7'
services:
  react-game:
    build:
      context: .
      target: 'develop-stage'
    ports:
    - '8080:8080'
    volumes:
    - '.:/app'
    command: /bin/sh -c "yarn && yarn start"
```

Build and run the application in development mode with docker-compose:

```$xslt
docker-compose up --build
```

Build this container with command:

```$xslt
docker build -t react-pharser-game .
```

Run this command:

```$xslt
docker run -it -p 3000:3000 --rm react-pharser-game
```