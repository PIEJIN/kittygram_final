
# Kittygram

Kittygram is a web application for sharing cat photos and achievements. It allows users to create profiles for their cats, upload photos, and earn achievements. The project is built using Django and Django REST framework for the backend, as well as React for the frontend, all running in Docker containers.


## Getting Started

### Running with Docker

1. Install [Docker](https://www.docker.com/get-started) on your computer if you haven't already.

2. Clone the Kittygram repository:

   ```bash
   git clone https://github.com/PIEJIN/kittygram.git
   cd kittygram
   ```

3. Create a `.env` file in the project's root directory and specify the necessary environment variables such as `SECRET_KEY`, `DEBUG`, and PostgreSQL database credentials. Example `.env` file:

   ```plaintext
   SECRET_KEY=your_secret_key
   DEBUG=True
   POSTGRES_USER=django_user
   POSTGRES_PASSWORD=django_password
   POSTGRES_DB=django_db
   ```

4. Start Docker Compose to build and run all containers:

   ```bash
   docker-compose up -d
   ```

   This will launch containers for the backend, frontend, PostgreSQL database, and web gateway.

5. After a successful launch, the application will be accessible at http://localhost:9000/.

6. To stop the application, run the following command:

   ```bash
   docker-compose down
   ```

## API Examples

Examples of API requests to the backend:

- Get a list of all cats:

  ```http
  GET http://localhost:9000/api/cats/
  ```

- Create a new cat:

  ```http
  POST http://localhost:9000/api/cats/
  ```

- Upload a cat's photo:

  ```http
  POST http://localhost:9000/api/cats/<cat_id>/upload/
  ```

- Get a list of achievements:

  ```http
  GET http://localhost:9000/api/achievements/
  ```

## Technologies Used

- Django
- Django REST framework
- React
- Docker
- PostgreSQL

## Author

This project is created and maintained by PIEJIN (Radislav Korolev).
```
