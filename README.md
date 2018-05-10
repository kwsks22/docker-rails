# docker-rails

## rails projectの作成
    docker-compose run web rails new . --force --database=postgresql
    
## build
    docker-compose build
    
## databaseの設定

```yml:database.yml
default: &default
adapter: postgresql
encoding: unicode
host: db
username: postgres
password:
pool: 5
```

## databaseの作成
    docker-compose run web rake db:create
    
## 起動
    docker-compose up
