# Docker Voenset Platform

## Стандартный .env

Создайте файл `.env` в корне проекта и заполните его следующими данными:

```env
POSTGRES_USER=postgres
POSTGRES_PASSWORD=11111111
POSTGRES_DB=postgres

MONGO_INITDB_ROOT_USERNAME=root
MONGO_INITDB_ROOT_PASSWORD=11111111

MINIO_ENDPOINT="minio"
MINIO_PORT="9000"
MINIO_USE_SSL="false"
MINIO_ROOT_USER=minioadmin
MINIO_ROOT_PASSWORD=11111111
MINIO_BUCKET_NAME=test

NODE_ENV=production
```