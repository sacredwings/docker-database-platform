# Docker Voenset Platform

## Старт docker

```env
docker-compose up -d
```

## Стандартный .env

Создайте файл `.env` в корне проекта и заполните его следующими данными:

```env
# ==========================================
# Приложение
# ==========================================
NODE_ENV=development
PORT=3000

# ==========================================
# POSTGRES — контейнер
# (образ postgres читает эти переменные при первом старте)
# ==========================================
POSTGRES_USER=postgres
POSTGRES_PASSWORD=11111111
POSTGRES_DB=postgres

# ==========================================
# POSTGRES — для вашего приложения
# (host = имя сервиса в docker-compose)
# ==========================================
DB_HOST=postgres
DB_PORT=5432
DB_USER=postgres
DB_PASSWORD=11111111
DB_NAME=dbname

# ==========================================
# MONGO — контейнер
# (образ mongo читает эти переменные при первом старте)
# ==========================================
MONGO_INITDB_ROOT_USERNAME=root
MONGO_INITDB_ROOT_PASSWORD=11111111

# ==========================================
# MONGO — для вашего приложения
# (host = имя сервиса в docker-compose)
# ==========================================
MONGO_HOST=mongo
MONGO_PORT=27017
MONGO_USER=root
MONGO_PASSWORD=11111111
MONGO_DB=dbname
MONGO_AUTH_SOURCE=admin

# Готовая строка подключения (если удобнее использовать её вместо отдельных переменных)
MONGODB_URI=mongodb://root:11111111@mongo:27017/dbname?authSource=admin

# ==========================================
# MINIO — контейнер
# (образ minio читает эти переменные при старте)
# ==========================================
MINIO_ROOT_USER=minioadmin
MINIO_ROOT_PASSWORD=11111111

# ==========================================
# MINIO — для вашего приложения
# (если используете отдельные ключи, отличные от root)
# ==========================================
MINIO_ENDPOINT=minio
MINIO_PORT=9000
MINIO_USE_SSL=false
MINIO_ACCESS_KEY=minioadmin
MINIO_SECRET_KEY=11111111

# ==========================================
# MINIO — бакеты приложения
# ==========================================
MINIO_BUCKET_TEMP=bucketname-temp
MINIO_BUCKET_ASSETS=bucketname-assets
```