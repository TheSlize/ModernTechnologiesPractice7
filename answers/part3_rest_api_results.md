# Часть 3: REST CRUD

Запишите ответы и HTTP-коды.

| Запрос | HTTP-код | Тело ответа / заметки |
|---|---:|---|
| POST `/api/students` | 201 Created | `{"id":5,"name":"NewStudent","surname":"Test"}` — новый студент добавлен в БД. Тело запроса: `{"name":"NewStudent","surname":"Test"}`. Требуется роль `ADMIN`. |
| GET `/api/students` | 200 OK | `[{"id":1,"name":"Sash","surname":"Brown"},{"id":2,"name":"Jone","surname":"Smith"},{"id":3,"name":"Deema","surname":"Johnson"},{"id":4,"name":"Ekatrena","surname":"Wilson"}]` |
| GET `/api/students/1` | 200 OK | `{"id":1,"name":"Sash","surname":"Brown"}`. Если студент с таким id не существует — `404 Not Found`. |
| PUT `/api/students/1` | 200 OK | `{"id":1,"name":"Sasha","surname":"Brown"}` — данные обновлены. Если студент не найден — `404 Not Found`. Требуется роль `ADMIN`. |
| DELETE `/api/students/1` | 204 No Content | Тело ответа пустое. Студент с id=1 удалён. Требуется роль `ADMIN`. |