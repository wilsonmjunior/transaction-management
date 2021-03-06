<h1 align="center">
  <img src="https://res.cloudinary.com/dhqnvbd52/image/upload/v1595975364/GoFinances/logo.408488e0_qpx4dy.svg" width="400"/>
</h1>

<p align="center">
Transfer management application for Node.js training with TypeScript, database with TypeORM and sending files with Multer
</p>

## Project Status

<h4 align="center"> 
  ✔	Concluded ✔
</h4>

## Setting up Databases 

The project uses [PostgreSQL](https://www.postgresql.org/).

I recommend use [Docker](https://www.docker.com/)  to install and run the database.

## How to use

Tools that need to be installed

[Git](https://git-scm.com), [Node.js](https://nodejs.org/en/) and [Yarn](https://yarnpkg.com/) 

In addition to an editor to be able to work with the code [VSCode](https://code.visualstudio.com/)

### 🎲 Running the application 

```bash
# Clone this repository
$ git clone <https://www.github.com/wilsonmjunior/go-finances-api>

# Access the project folder 
$ cd go-finances-api

# Install dependencies
$ yarn

# Create the container in the Docker
docker-compose -f "docker-compose.yml" up -d --build

# Run migrations
yarn typeorm migration:run

# Run the application in development 
$ yarn dev:server

# The server will start at the port:3333 - access <http://localhost:3333>
```

## Testing api
Application routes

```bash
POST /transactions
{
  "id": "uuid",
  "title": "Salário",
  "value": 3000,
  "type": "income",
  "category": "Salario"  
}

GET /transactions
{
  "transactions": [
    {
      "id": "uuid",
      "title": "Salário",
      "value": 4000,
      "type": "income"
    },
    {
      "id": "uuid",
      "title": "Freela",
      "value": 2000,
      "type": "income"
    },
    {
      "id": "uuid",
      "title": "Pagamento da fatura",
      "value": 4000,
      "type": "outcome"
    },
    {
      "id": "uuid",
      "title": "Cadeira Gamer",
      "value": 1200,
      "type": "outcome"
    }
  ],
  "balance": {
    "income": 6000,
    "outcome": 5200,
    "total": 800
  }
}
```

## Technologies used

- [Node.js](https://nodejs.org/en/)
- [TypeScript](https://www.typescriptlang.org/)
- [TypeORM](https://typeorm.io/)
- [Docker](https://www.docker.com/)
- [PostgreSQL](https://www.postgresql.org/)

##  License

:memo: This project is under the MIT license. See the [LICENSE](https://github.com/wilsonmjunior/go-finances-api/blob/master/LICENSE) for more information.
