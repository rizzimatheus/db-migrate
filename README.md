# Database Migration in GO

- Library: [Golang Migrate](https://github.com/golang-migrate/migrate)
- [Instalation](https://github.com/golang-migrate/migrate/tree/master/cmd/migrate): 
    ```bash
    curl -L https://github.com/golang-migrate/migrate/releases/download/v4.15.2/migrate.linux-amd64.tar.gz | tar xvz
    ```
    ```bash
    mv migrate $GOPATH/bin/migrate
    ```
## Create Migration File
```bash
migrate create -ext sql -dir db/migration -seq init_schema
```

## Migrate Up
```
migrate -path db/migration -database "postgresql://USER:PASSWORD@HOST:PORT/DATA_BASE?sslmode=disable" -verbose up
```
## Migrate Down
```
migrate -path db/migration -database "postgresql://USER:PASSWORD@HOST:PORT/DATA_BASE?sslmode=disable" -verbose up
```