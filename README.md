# ChillAndCoworkMoscow

# ТЗ

## 1. Цель проекта
Создать приложение для поиска мест для отдыха и работы в мск

## 2. Пользователи
1. Туристы
2. Удаленщики/фрилансеры
3. Владельцы заведений

## 3. Основной функционал

*Место - точка на карте, коворкинг, достопримечательность, ресторан или кафе*

1. Авторизация/регистрация
2. Настройка профиля(выбор имени и аватара)
3. Отобржаение мест на карте
4. Составление рандомного маршрута для прогулки(если будет техническая возможность)
5. Проложение маршрута до искомого места(если будет техническая возможность)
6. Отображение детальной информации о месте(описание, отзывы, рейтинги, фото)
7. Возможность для пользователя оставить отзыв и поставить рейтинг месту
8. Возможность для пользователя отметить новое место в приложении
9. Поддержка цветовой темы темная/светлая


### 3.1 Вход
1. Полдьзователь видит приветсвенный экран на котором предлагается либо залогинится, либо войти
2. При нажании на кноку войти пользователь видит экран входа
3. Вводит логин и пароль
    1. Логин и пароль валидные и пользователь не существует -> Входит
    2. Логин или пароль невалидные или пользователя не существует -> Показываем пользователю ошибку авторизации
   
### 3.2 Регисрация
1.  Полдьзователь видит приветсвенный экран на котором предлагается либо залогинится, либо войти
2.  При нажатии на кнопку регистрации пользователь видит экран регистрации
3.  Вводит логин, пароль, имя
    1.  Логин и пароль валидные, пользователя не сущетсвует -> успешная регистрация и вход
    2.  Логин или пароль невалидные или пользователь с таким логином уже существет -> сообщение об ошибке при регистрации

### 3.3 Отображение и поиск мест
1. Пользователь видит две вкладки(Работа/Отдых)
2. На вкладке пользователь видит карту, на которой оторбажены ближайшие к нему места, серчбар для поиска конкретного места, и кнопку "Отметить место"
3. Так же на вкладке "Отдых" должна быть кнопка "Составить маршрут прогулки"
4. Если пользователь выбирает место на карте он видит детальное окно

### 3.4 Добавить место
1. При нажатии на кнопку "Добавить место" пользователь видит окно с возможность добавить место
2. Ползователь вводит название
3. Вводит описание
4. Ставит рейтинг
5. Прикладывает изображения
6. Сохраняет
    1. Место сохраняется
    2. Происходит ошибка -> пользователь видит сообщение от ошибке
### 3.5 Отображение детальной информации
1. Пользователь выбирает точку на карте
2. Открывается окно детальной информации
3. Видит название места
4. Описание
5. Фото
6. Рейтинг 
7. Видит кнопку составить маршрут
### 3.5 Составления маршрута для прогулки
1. Пользователь нашимает конпку "Составить маршрут для прогулки"
2. Указывает желаемое расстояние
3. При выборе растояния пользователю будет показано, сколько примерну займет прогулка
4. Выбирает хочет ли он, чтобы маршрут был замкнутым
5. Далее кользователь подтверждает выбранные параметры
6. И видит на карте положенный маршрут

### 3.5 Составления маршрута до искомого места
1. В деталке пользователь жмет "Проложить маршрут"
2. На карте пользователь видит маршрут до места
### 3.6 Оставить отзыв
1. В деталке пользователь выбирает контрол для воода отзыва
2. Жмет подтвердить
3. Если поле не пустое, отправляется отзыв на место 
### 3.9 Цветовая тема
1. Можно выбрать тему (темная/светлая/системная)

## Предполагаемый стэк технологий

Архитектура: MVP+C(Presentation) + Сервисы(Subject logic) + Core(Network+Cache)
Сеть: (URLSession, async/await)/Alamofire??? Codable
Хранение данных в облаке, авторизация: Firebase
Кэширование данных: Realm, Nuke 

## Пожелания по дизайну
1. Все деталки и можалки должны показываться как шторка снизу
2. Экран пользователя должен быть отдльным экраном
3. Поиск коворкингов и поиск мест для отдыха должен быть на разных вкладках
