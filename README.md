# kinoshki-RFE
repo for kinoshki "register for everything" bot

# Киношкинсы

## Что?

Бот для регистрации на все мероприятия киношек

## Когда?

Сроков нет, задача на повышение понимания и квалификации активистов/стажеров

## Краткое описание

Регистрация на мероприятия Киношек (Киноигры, Киновечера, Выезды), сохранение данных пользователей, создание новых мероприятий, открытие и закрытие регистрации, массовая рассылка

## Виды мероприятий

### Киновечера

Инфо от админа:

- Название
- Краткая инфа
- Дата, время
- Место
- Ссылка на чат-обсуждение
- Дата-время открытия и закрытия регистрации

Инфо от участников:

- ФИО
- Учебная группа
- Из/не из Бауманки
- Телефон
- Tg

Пайплайн регистрации:

- Регистрация появляется
- Человек регается, ему дают ссылку на чат
- Регистрация заканчивается

### Киноигры

Инфо от админа:

- Название
- Краткая инфа
- Дата, время
- Место
- Дата-время открытия и закрытия регистрации

Инфо от участников:

Регается только капитан

- ФИО капитана
- Учебная группа
- Есть ли в команде участники не из Бауманки (Да/Нет)
- Название команды
- Количество человек
- Телефон
- Tg

Пайплайн регистрации:

- Регистрация появляется
- Человек регается
- За два дня до меро рассылаются уведомления с напоминанием и вопросом, придет ли человек (Да - круто/ Нет - отмена регистрации)
- Регистрация заканчивается

### Выезды

Инфо от админа:

- Название
- Краткая инфа
- Дата, время
- Место сбора
- Ссылка на обратную связь
- Дата-время открытия и закрытия регистрации

Инфо от участников:

- ФИО
- Учебная группа
- Телефон
- Tg
- Дата рождения
- VK
- Особенности питания:
    - Не ем мясо
    - Не ем молоко
    - Не ем то на что у меня аллергия: человек вводит свои аллергены сам
- Особенности здоровья: текст

Пайплайн регистрации:

- Регистрация появляется
- Человек регается
- В понедельник на неделе выезда рассылаются уведомления с напоминанием и вопросом, придет ли человек (Да - круто/ Нет - отмена регистрации)
- Регистрация заканчивается

## Функциональность

### Пользователь

Все возможные данные пользователя хранятся в базе и используются при повторной регистрации

Интерфейс пользователя:
- **Показать доступные меро** - выводит список доступных регистраций, напротив меро, на которые пользователь зареган - галочка
    - **Нажатие на меро, на которые пользователь зареган** - хотите ли вы отменить регистрацию?
    - **Нажатие на меро на которые пользователь еще не зареган** - регистрация - находящиеся в базе данные автоматически заполняются, остальные запрашиваются - в конце подтверждение со всеми данными с возможностью изменить в том числе данные, подтянутые из базы
- **Изменить данные о себе**

Если до того как пользователь зарегистрировался на меро участникам отправлялись какие-либо уведомления, после регистрации пользователь получает все **пропущенные** им уведомления

### Админ

Админы могут иметь доступ только к конкретным видам мероприятий. Напиример админ1 может управлять только киновечерами, админ2 только киноиграми и выездами, а админ3 любыми меро 

Интерфейс админа:
- **Создать меро**
- **Показать меро** - выводится список доступных меро - при нажатии на меро:
    - **Изменить** - при внесении изменений - уведомление зареганным
    - **Удалить** - при удалении - уведомление зареганным
    - **Рассылка** сообщения всем зареганным на меро
