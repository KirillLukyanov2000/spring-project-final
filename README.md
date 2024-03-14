## [REST API](http://localhost:8080/doc)

## Концепция:

- Spring Modulith
    - [Spring Modulith: достигли ли мы зрелости модульности](https://habr.com/ru/post/701984/)
    - [Introducing Spring Modulith](https://spring.io/blog/2022/10/21/introducing-spring-modulith)
    - [Spring Modulith - Reference documentation](https://docs.spring.io/spring-modulith/docs/current-SNAPSHOT/reference/html/)

```
  url: jdbc:postgresql://localhost:5432/jira
  username: jira
  password: JiraRush
```

- Есть 2 общие таблицы, на которых не fk
    - _Reference_ - справочник. Связь делаем по _code_ (по id нельзя, тк id привязано к окружению-конкретной базе)
    - _UserBelong_ - привязка юзеров с типом (owner, lead, ...) к объекту (таска, проект, спринт, ...). FK вручную будем
      проверять

## Аналоги

- https://java-source.net/open-source/issue-trackers

## Тестирование

- https://habr.com/ru/articles/259055/

## Список выполненных задач:
1. Разобраться со структурой проекта. <p align="right">++</p>
2. Удалить социальные сети: vk, yandex. <p align="right">++</p>
3. Вынести чувствительную информацию в отдельный проперти файл. <p align="right">--</p>
4. Переделать тесты так, чтоб во время тестов использовалась in memory БД (H2). <p align="right">--</p>
5. Написать тесты для всех публичных методов контроллера ProfileRestController. <p align="right">++</p>
6. Сделать рефакторинг метода com.javarush.jira.bugtracking.attachment.FileUtil#upload. <p align="right">++</p>
7. Добавить новый функционал: добавления тегов к задаче (REST API + реализация на сервисе). <p align="right">--</p>
8. Добавить подсчет времени сколько задача находилась в работе и тестировании. <p align="right">--</p>
9. Написать Dockerfile для основного сервера. <p align="right">--</p>
10. Написать docker-compose файл для запуска контейнера сервера вместе с БД и nginx. <p align="right">--
11. Добавить локализацию минимум на двух языках для mails и стартовой страницы index.html. <p align="right">++
12. Переделать механизм распознавания «свой-чужой» между фронтом и беком с JSESSIONID на JWT. <p align="right">--
##### Всего выполнено задач: 5