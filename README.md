# TODO
- [ ] Admin can add/remove student or mentor (Backend: Admin still can remove student or mentor with API)
- [ ] Deploy the application to AWS

# Client
```
cd client
npm install
```

Create `.env` file with the content
```
NEXT_PUBLIC_API_URL=http://localhost:3002
NEXT_PUBLIC_JWT_SECRET=mentor_123
```

# Server
```
cd server
npm install
```

- Start the MySQL server using Docker container
```
docker run --name mysql-db -e MYSQL_ROOT_PASSWORD=root -d mysql:8
```
Then, create a database named `mentor`

- Environment variables
Create `.env` file with the content
```
PORT=3002
JWT_SECRET=mentor_123

DB_HOST=localhost
DB_PORT=3306
DB_USERNAME=root
DB_PASSWORD=root
DB_NAME_MENTOR=mentor
```

- Start the server
```
npm run start:dev
```
