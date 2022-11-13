# Дипломный проект профессии «Тестировщик»

## Документация
1. [План автоматизации](https://github.com/unicornfraaa/diploma-QA/blob/master/Plan.md)

1. [Отчётные документы по итогам тестирования](https://github.com/unicornfraaa/diploma-QA/blob/master/Report.md)

1. [Отчётные документы по итогам автоматизации](https://github.com/unicornfraaa/diploma-QA/blob/master/Summary.md)



## Запуск SUT, авто-тестов и генерация репорта
Подключение SUT к PostgreSQL
1.	Запустить Docker Desktop
2.	Открыть проект в IntelliJ IDEA
3.	В терминале в корне проекта запустить контейнеры:

`docker-compose up -d`

4.	Запустить приложение:
	`java -jar artifacts/aqa-shop.jar --spring.datasource.url=jdbc:postgresql://localhost:5432/app `

6.	Открыть второй терминал
7.	Запустить тесты:

`./gradlew clean test -DdbUrl=jdbc:postgresql://localhost:5432/app`

8.	Создать отчёт Allure и открыть в браузере

`./gradlew allureServe`

9.	Закрыть отчёт:
**CTRL + C -> y -> Enter**
10.	Перейти в первый терминал
11.	Остановить приложение:
 **CTRL + C**
12.	Остановить контейнеры:

`docker-compose down`

## Подключение SUT к MySQL
1.	Запустить Docker Desktop
2.	Открыть проект в IntelliJ IDEA
3.	В терминале в корне проекта запустить контейнеры:

docker-compose up -d
4.	Запустить приложение:

`java -jar artifacts/aqa-shop.jar --spring.datasource.url=jdbc:mysql://localhost:3306/app`

5.	Открыть второй терминал
6.	Запустить тесты:

`./gradlew clean test -DdbUrl=jdbc:mysql://localhost:3306/app`

7.	Создать отчёт Allure и открыть в браузере

`./gradlew allureServe`

8.	Закрыть отчёт:
**CTRL + C -> y -> Enter**
9.	Перейти в первый терминал
10.	Остановить приложение:
**CTRL + C**
11.	Остановить контейнеры:

`docker-compose down`
