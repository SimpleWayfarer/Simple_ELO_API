Мониторинг API с помощью Alloy + Loki + Prometheus + Grafana

# Для запуска:
1) Создать папку для БД
```
mkdir db/data
```
2) Развернуть 
```
sudo docker compose up -d
```
3) Для просмотра дашборда Grafana перейти на 
```
http://localhost:3000/
```
Логин - admin, пароль - admin

# Запросы к API:
1) GET запрос всех пользователей
```
curl http://localhost/users
```
2) POST запрос добавления нового пользователя
```
curl -X POST http://localhost/users \
  -H "Content-Type: application/json" \
  -d '{"name": "Alice", "elo": 1200}'
```
2) POST запрос обработки результата партии между пользователями
```
curl -X POST http://localhost/match \
-H "Content-Type: application/json" \
-d '{"user_a":"Alice","user_b":"Bob","score_a":1}'
```
