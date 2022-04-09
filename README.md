# Docker cache image

Example for How to use cache image from docker ?

### version image

- Docker version 20.10.13
- Node version 16.3.0

### structure

```
app
|
├── src

    └── index.js

    └── package.json

    └── package-lock.json

├── dockerfile.cache

├── dockerfile.no-cache

└── README.md
```

### build & run image

- cache
  - `docker build -f ./Dockerfile.cache -t docker-cache:0.0.1 .`
  - `docker run -p 3000:3000 docker-cache:0.0.1`
- no cache
  - `docker build -f ./Dockerfile.no-cache -t docker-no-cache:0.0.1 .`
  - `docker run -p 3000:3000 docker-no-cache:0.0.1`

### How to test

After change code index.js run build from Dockerfile.cache and Dockerfile.no-cache after that expect result.

### result

- cache
  <img src="https://i.imgur.com/jPl9kJ6.jpeg" />
  <img src="https://i.imgur.com/mgPZXAV.jpeg" />
- no cache
  <img src="https://i.imgur.com/g3p5tHl.jpeg" />
  <img src="https://i.imgur.com/Qm2HAc1.jpeg" />
