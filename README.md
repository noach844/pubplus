
# Pub Plus

The project is a simple team availabilty system powerd by React.js and Flask, using JWT for Auth and a PostgressDB.




## Deployment

To deploy this project run

```bash
  git clone --recursive <repository-url>
  cd pubplus
  docker-compose up --build
```
Thats All!




## Environment Variables

There are Environment Variables in multiple places.

### docker-compose.yml:

`POSTGRES_USER` - username for db

`POSTGRES_PASSWORD` - password for db

`POSTGRES_DB` - db name

`DATABASE_URI` - in the flask-app service, needs to match the above env vars

### client/.env 
we have 2 vars here due to react build process.

#### both need change when changing server port


`VITE_REFRESH_TOKEN_API` - refresh token endpoint (auth server on bigger architectures)

`VITE_SERVER_API` - api endpoint

### server/Dockerfile

`SECRET_KEY` - key used to create the jwt

`ACCESS_TOKEN_EXPIRE_SEC` - access token expire time in seconds
