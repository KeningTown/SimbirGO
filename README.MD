# Simbir.GO RESTFULL API

## Изменения в процессе выполнения задания


## Запуск сервера
Для запуска сервера требуется открыть основную директорую проекта и выполнить следующие команды:
```
    1. go mod download 
    2. go run ./cmd/main.go
```

## Поддерживаемые флаги
Команда `run ./cmd/main.go` также поддерживает определенный набор флагов, для настройки подключения к базе данных PostgreSQL:
- *username* - имя пользователя базы данных (использовать в случае, если имя пользователя отличается от postgres)
- *password* - пароль к пользователю (использовать в случае, если пароль отличается от стандартного postgres)
- *dbname* - имя базы данных (использовать, если подключение будет производится не к базе данных с именем postgres)
- *port* - порт подключения к базе данных (использовать, если порт подключения отличается от стандартного 5432)
- *sslmode* - использование ssl мода при подключении к базе данных (использовать, если отличается от значения disable)
- *host* - хост по которому происходит подключение к базе данных (использовать, если отличается от localhost)

**Если настройки подключения отличаются от настроек по умолчанию, то требуется использовать соответствующий флаг**

## Пример использования флагов
```
    go run ./cmd/main.go -username=user -password=veryStrongPassword -dbname=transportRents -port=2345 -host=localhost sslmode=disble
```

## Swagger URL
http://localhost/swagger/index.html