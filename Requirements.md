# Приложение для управления задачами

## Функциональные требования

## ФТ-1: Функции приложения

### ФТ-1.1:Приложение должно позволять создавать, редактировать и удалять следующие сущности:

1. Проект <->
      Название,
      Сокращенное название,
      Описание

2. Задача <->
     Название,
     Работа (ч),
     Дата начала,
     Дата окончания,
     Статус (Не начата | В процессе | Завершена | Отложена)

3. Сотрудник <->
     Фамилия,
     Имя,
     Отчество,
     Должность


## ФТ-2: Связи сущностей

### ФТ-2.1:	Между перечисленными объектами(см.  ФТ-1.1) необходимо реализовать следующие связи:

    • Проект может включать в себя от нуля до множества задач
    • Один сотрудник может быть назначен на множество задач
    • Дополнительное требование: одна и та же задача может выполняться множеством сотрудников
	

## ФТ-3: Приложение должно содержать следующие основные элементы:

### ФТ-3.1: Главное Меню

    • Проекты: Отображается форма “Список проектов”
    • Задачи: Отображается форма “Список задач”
    • Персоны: Отображается форма “Список сотрудников”


### ФТ-3.2: Форма “Список проектов”

#### ФТ-3.2.1: Колонки:

Идентификатор, Название, Сокращенное название, Описание

#### ФТ-3.2.2: Команды уровня формы:

    • Добавить: Отображается форма ввода проекта в режиме добавления
	
  
#### ФТ-3.2.3: Команды уровня записи:
    
    • Изменить: Отображается форма ввода проекта в режиме редактирования
    • Удалить: Текущая запись удаляется


### ФТ-3.3: Форма “Список задач”

#### ФТ-3.3.1: Колонки:
  
Идентификатор, Проект (Сокращенное название), Название, Дата начала, Дата окончания, Исполнитель (ФИО), Статус (Не начата | В процессе | Завершена | Отложена)

#### ФТ-3.3.2: Команды уровня формы:

    • Добавить: Отображается форма ввода задачи в режиме добавления


#### ФТ-3.3.3: Команды уровня записи

    • Изменить: Отображается форма ввода задачи в режиме редактирования
    • Удалить: Текущая запись удаляется


### ФТ-3.4: Форма “Список сотрудников”

#### ФТ-3.4.1: Колонки:

  Идентификатор,
  Фамилия,
  Имя,
  Отчество,
  Должность

#### ФТ-3.4.2: Команды уровня формы

    • Добавить: Отображается форма ввода сотрудника (см. ФТ-3.7) в режиме добавления


#### ФТ-3.4.3: Команды уровня записи

    • Изменить: Отображается форма ввода сотрудника (см. ФТ-3.7) в режиме редактирования
    • Удалить: Текущая запись удаляется


### ФТ-3.5: Форма ввода проекта

#### ФТ-3.5.1: Поля:

     Идентификатор: порядковый номер проекта; формируется автоматически; недоступно для изменения
     Название
     Сокращенное название
     Описание

#### ФТ-3.5.2: Список задач, принадлежащих проекту:

##### ФТ-3.5.2.1: Колонки:
     Идентификатор,
     Название,
     Работа (ч),
     Дата начала,
     Дата окончания,
     Исполнитель (ФИО),
     Статус (Не начата | В процессе | Завершена | Отложена)

##### ФТ-3.5.2.2: Команды уровня формы
    
    • Добавить: Отображается форма ввода задачи в режиме добавления (поле ввода проекта установлено равным текущему проекту и недоступно для редактирования)


##### ФТ-3.5.2.3: Команды уровня записи
    
    • Изменить: Отображается форма ввода задачи в режиме редактирования
    • Удалить: Текущая запись удаляется

#### ФТ-3.5.3: Команды:
    
    • Сохранить: введенные данные сохраняются в базе; управление передается в форму “Список проектов”
    • Отмена: управление передается в форму “Список проектов”


### ФТ-3.6: Форма ввода задачи

#### ФТ-3.6.1: Поля:
    
     Идентификатор: порядковый номер задачи; формируется автоматически; недоступно для изменения,
     Проект: выбирается из списка проектов; если форма открыта из списка задач “Формы ввода проектов”, то данное поле установлено равным текущему проекту и недоступно для редактирования,
     Название,
     Работа (количество времени необходимого для выполнения задачи, часы),
     Дата начала,
     Дата окончания,
     Статус (Не начата | В процессе | Завершена | Отложена),
     Исполнитель: выбирается из списка персон

#### ФТ-3.6.2: Команды:
    
    • Сохранить: данные сохраняются в базе (в случае вызова из списка задач) либо в проекте (в случае вызова из формы ввода проекта); управление передается в предыдущую форму: форму списка задач либо форму ввода проекта.
    • Отмена: управление передается в предыдущую форму: форму списка задач либо форму ввода проекта.


### ФТ-3.7: Форма ввода персоны (исполнителя)

#### ФТ-3.7.1: Поля:
    
     Идентификатор; формируется автоматически; недоступно для изменения,
     Фамилия,
     Имя,
     Отчество,
     Должность

#### ФТ-3.7.2: Команды:
    
    • Сохранить: введенные данные сохраняются в базе; управление передается в форму “Список персон”
    • Отмена: управление передается в форму “Список персон”


#### Замечание по терминологии: “команда” обозначает любой элемент управления,используемый для запуска операции, к примеру, это может быть кнопка, пиктограмма, гиперссылка и т.п.



## Вопросы на уточнение/изменение требований заказчика

### Базовые вопросы:
    
    1. Какой тип приложения требуется разработать: браузерное, мобильное, десктопное?
    2. Если браузерное, то под какие браузеры необходимо разрабатывать: Google Chrome, Opera, Microsoft Edge, Mozilla Firefox и каких версий?
    3. Если мобильное, то под какую мобильную ОС: Android, iOS и каких версий?
    4. Если десктопное, то под какое окружение: Windows, macOS, Linux, иные ОС и каких версий: Windows 7, Ubuntu 18.04, macOS Catalina ….?
    5. Требуемые языки интерфейса приложения?
    6. Инструменты разработки:
        1. Какой стек технологий для фронтенда, для бэкенда? 
        2. Поддержка БД!
        3. Сторонние API? 

### Требования к сущностям:
#### Проект (Название, Сокр. название, Описание) 
    
    1. Являются ли данные поля сущности требуемыми к заполнению? Какие да, какие не обязательны?
    2. Возможно ли отсутствие одного поля при наличии другого(например, сокращенного названия при наличии полного)?
    3. Требуется ли чтобы все поля Проекта были текстовыми?
    4. Все поля должны быть введены вручную? Или стоит предусмотреть наличие выпадающих списков для выбора?
    5. Какие требования по максимальной длине каждого поля?

#### Задача (Название, Работа(ч), Дата начала, Дата окончания, Статус)
    
    1. Какие поля сущности обязательны к заполнению пользователем?
    2. Какие ограничения по длине полей Название?
    3. Какой диапазон вводимых значений для поля Работа?
    4. Каков требуемый тип данных для полей Дата начала, Дата окончания?
    5. Какое ожидается поведение системы при вводе недействительного диапазона дат (например, дата начала больше даты окончания)?
    6. Какие символы, спец.символы разрешены для поля Название? 

#### Сотрудник (Фамилия, Имя, Отчество, Должность)
    
    1. Какие поля обяз-ны к заполнению?
    2. Поле Отчество лучше сделать необязательным ввиду отсутствия его у многих невосточно-европейских сотрудников.
    3. Необходимо уточнить алфавит и макс. длину для данных полей?

### Требования к связям между сущностями:
    
    1. Какое максимальное кол-во задач может содержать проект?
    2. Какие есть ограничения по кол-ву задач, назначенных на одного сотрудника?

### Требования к основным элементам приложения:
#### Главное меню
    
    1. Как приложение должно отображать пустой список (список *) ?

#### Поле  “Идентификатор”:
    
    1. Из какого набора символов формируется идентификатор: цифры 0-9, буквы латиницы, кириллицы или цифры+символы ?
    2. Уточните, что значит “Идентификатор формируется автоматически”: должен применяться алгоритм генерации идентификатора или достаточно инкрементировать идентификатор предыдущей записи ?
    3. Каким должен быть по умолчанию идентификатор первой записи ? 

#### Команда “Добавить” на формах списков:
    
    1. Уточните, при каких ситуациях новая запись может быть добавлена в список: наличие каких полей обязательно, каких вспомогательно для каждой из форм?
    2. Необходимо ли валидировать обязательные поля на соответствие, например, дате или числу ?

#### Команда “Удалить” на формах списков:
    
    1. Предлагаем Удаление записи сделать отменяемым либо просить пользователя подтвердить данное решение нажатием кнопки Подтвердить, на случай если пользователь допустил ошибку и случайно попытался удалить запись из списка.

#### Команда “Изменить” на формах списков:
    
    1. Уточните, какие поля должны быть доступны к изменению в момент редактирования записи в таблице на каждой из форм?

#### Форма “Список проектов” (ID, Название, Сокр.название, Описание)
    
    1. Каковы ограничения на длину строки для колонки Название ?
    2. Чтобы сэкономить время ответа приложения на запросы с помощью кэширования данных, предлагаем Вам ограничить длину строки поля Описание до 250 символов.

#### Форма “Список задач” (ID, Сокр.назв проекта, название, дата начала, дата окончания, ФИО исполнителя, статус)
    
    1. Могут ли возникнуть задачи, не принадлежащие ни одному проекту или принадлежащие нескольким одновременно ?
    2. Каковы ограничения на длину строки для поля Название ?
    3. Какие у заказчика требования по типу данных для полей ?

#### Форма “Список сотрудников” (ID, ФИО, Должность)
    
    1. Какое ожидается поведение приложения при добавлении двух сотрудников с одинаковыми данными(кроме ID) ? (Кроме ID и Должность) ? 
    2. Поле Должность: drop-down или ввод на форме добавления сотрудника ?

### Требования по формам ввода:
#### Команда “Сохранить” на формах ввода:
    
    1. Какова реакция приложения на таймаут ожидания ответа от БД или разрыв соединения с сервером после попытки Сохранить сущность?

#### Форма ввода проекта (ID, Название, Сокр. Название, Описание, Список задач)
    
    1. Какова ожидаемая реакция приложения на добавление проекта без задач ?
    2. См. требования к полям объекта Проект
    3. См. требования к полям объекта Задача

#### Форма ввода задачи (ID, Проект(сокр.), Название, Работа(ч), Дата начала, Дата окончания, Статус, Исполнитель(Сотрудник))
    
    1. См. требования по объекту Задача
    2. Каково поведение приложения при отсутствии исполнителей для задачи? Обязательно ли наличие исполнителя для задачи на момент её создания ?
    3. Уточните из каких мест приложения должна быть доступна форма?

#### Форма ввода исполнителя(сотрудника) (ID, ФИО, Должность)
    
    1. См. требования к полям объекта Сотрудник(в том числе к полю Идентификатор)
