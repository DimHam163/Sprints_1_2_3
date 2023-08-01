# API для получение сведений о перевалах.
****
Пользователь, используя мобильное приложение, может отправить данные, вызывая метод submitData, который принимает данные в формате JSON.
****
В ходе разработки было реализовано:

# Модели

Users -
Модель пользователей, содержит информацию о пользователе: имя, фамилию, отчество, email, phone.

Coord -
Модель координат, содержит информацию о координатах перевалов: широту, долготу и высоту.

Level -
Модель уровней сложности, содержит информацию о: winter, summer, autumn, spring.

Pass -
Модель перевалов, содержит информацию о перевалах: название, координаты, уровень сложности в каждый сезон, изображения, статус, дата добавления, идентификатор пользователя, который добавил перевал.

Image -
Модель изображений перевалов, содержит информацию об изображении и его названии.
_______________________________________________________________________
# Методы:
GET /submitdata/ method - Возвращает список всех горных перевалов.

POST /submitdata/ method - Позволяет подавать один горный перевал.

GET /submitdata/{id} - Извлекает данные для определенного горного перевала.

PATCH /submitdata/{id} - Позволяет изменить значения атрибутов горного перевала:

state: '1' for successful update and '0' for unsuccessful update.

 message: explains why an update has failed.

GET /submitdata/?user__email=< email > - Возвращает список всех объектов, которые были отправлены в систему пользователем с указанным адресом электронной почты.

****
# Спринт №2:

GET /submitData/<id> 

PATCH /submitData/<id> 
 state: '1' for successful update and '0' for unsuccessful update.
 message: explains why an update has failed.
 
 GET /submitData/?user__email=< email >
 
****
# Спринт №3:

Добавлена документацию REST API в Readme.md

Реализована документация с Swagger

Код покрыт тестами
_______________________________________________________________________
# Тесты

Ran 11 tests in 0.130s

OK
Destroying test database for alias 'default'...

![image](https://github.com/DimHam163/Sprints/assets/90146637/6773ec2c-211e-4b2e-8524-5bfe28e7c511)

p.s. During the work on sprints 2-3, due to problems (system error) during testing, the application was renamed from Pass to Pereval.
 
