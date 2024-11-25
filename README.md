# Welcome to Inosoft University Registration Platform
this is a simple system for student registration with microservice architecture

# Architecture design
![architecture-design](inosoft-university-registration-Architecture.drawio.png)

# ERD Schema
![ERD](./inosoft-university-registration-ERD.drawio.png)

# Stack used
- [Laravel 5.8.5](https://laravel.com/)
- [Php 8.3.12](https://www.php.net/)
- [MySQL 5.7](https://www.mysql.com/)
- [Redis](https://redis.io/)
- [RabbitMQ](https://www.rabbitmq.com/)
- [Docker](https://www.docker.com/)
- [Docker Compose](https://docs.docker.com/compose/)

# How to contribute
1. Fork the repository
2. Create a new branch for your feature
3. Make your changes
4. Commit your changes
5. Push your changes to your branch
6. Create a pull request
7. Wait for review and merge
8. Deploy to production
9. Test and verify
10. Repeat the process

# How to run locally
## Make sure to install all dependencies stack used especially Docker and Docker compose
1. Clone the repository
```bash
$ git clone https://github.com/dijekarim/inosoft-university-registration.git
$ cd inosoft-university-registration
```

2. Clone `inosoft-department-service`
```bash
$ git clone https://github.com/dijekarim/inosoft-department-service.git
$ cd inosoft-department-service
$ cp .env.example .env
```

3. Clone `inosoft-user-service`
```bash
$ git clone https://github.com/dijekarim/inosoft-user-service.git
$ cd inosoft-user-service
$ cp .env.example .env
```

4. Clone `inosoft-notification-service`
```bash
$ git clone https://github.com/dijekarim/inosoft-notification-service.git
$ cd inosoft-notification-service
$ cp .env.example .env
```

5. Run `docker-compose up -d` to start the containers
```bash
$ docker compose up --build
```

6. Connect to MySQL db with your local client, MySQL workbench, Sequelace, etc. Then, insert credentials based on `docker-compose.yml` under mysql service

7. Create databse give it name as `university-dev`

8. Run migration from container `user-service`
```bash
$ docker compose exec user-service php artisan migrate
```

9. Then, you can use my simple default seeder from `user-service`
```bash
$ docker compose exec user-service php artisan db:seed
```

10. Happy Coding!!!

### Last but no least you can get my sample postman collection [here!](InoSoft.postman_collection.json)