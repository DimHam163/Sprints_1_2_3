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

Name                                 Stmts   Miss  Cover

--------------------------------------------------------

Passes\__init__.py                       0      0   100%

Passes\asgi.py                           4      4     0%

Passes\settings.py                      26      0   100%

Passes\urls.py                           5      0   100%

Passes\wsgi.py                           4      4     0%

manage.py                               12      2    83%

pereval\__init__.py                      0      0   100%

pereval\admin.py                         7      0   100%

pereval\apps.py                          4      0   100%

pereval\migrations\0001_initial.py       6      0   100%

pereval\migrations\__init__.py           0      0   100%

pereval\models.py                       35      0   100%

pereval\serializers.py                  44      1    98%

pereval\tests\__init__.py                0      0   100%

pereval\tests\payloads.py                6      0   100%

pereval\tests\test_api.py               75      0   100%

pereval\urls.py                          8      0   100%

pereval\views.py                        25      1    96%

pereval\yasg.py                          6      0   100%

--------------------------------------------------------

TOTAL                                  267     12    96%


p.s. During the work on sprints 2-3, due to problems (system error) during testing, the application was renamed from Pass to Pereval.
 
