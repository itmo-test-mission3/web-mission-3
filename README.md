                                                              
# Mission 2

## Part 0

[Link to video](https://www.youtube.com/watch?v=UUhavvMO2FQ)

## Part1

- Вопрос 1
Зачем нужен ssh? Ответ на пару предложений.
>Ответ:
SSH (Secure Shell) — это сетевой протокол, используемый для безопасного удаленного доступа к компьютерам и серверам. Он обеспечивает шифрование данных, что защищает информацию от перехва$


- Вопрос 2
Предположим, у вас есть прямой доступ к серверу(терминалу) под управлением ubuntu. У вас есть коллега Вася, который хочет получить доступ к этому серверу. Он генерирует пару ssh ключей с$
>Ответ:
Открытый ключ нужно положить в файл ~/.ssh/authorized_keys в корневой директории пользователя. Также необходимо настроить права доступа, чтобы файл был недоступен для записи посторонним $


- Вопрос 3
Тут вопрос про АПИ. Разберитесь, что такое long polling и webhooks, опишите сами в нескольких предложениях, как они работают.
Ответ
Long polling — это метод, при котором клиент отправляет запрос на сервер и остаётся в ожидании ответа. Сервер не отвечает сразу, а удерживает соединение открытым до тех пор, пока не появ$Webhooks — это метод, позволяющий серверам отправлять данные или уведомления в реальном времени по заранее заданному URL, который указывает клиент или другой сервис. Вместо того чтобы кл$


- Вопрос 4
Найдите информацию, что такое issues на гитхабе и для чего нужны. Также вставьте ссылки на пару примеров issues в популярных open source проектах.
> Ответ
Issues на GitHub — это система для отслеживания задач, ошибок и запросов, помогающая управлять разработкой проекта. Она используется для обсуждения и планирования работы, где участники м$
kubernetes/kubernetes#127538


- Вопрос 5
Ваш проект используется пустую папку images, но гит не поддерживает отслеживание пустых директорий. Что делать?
> Ответ
В images необходимо создать пустой файл с именем .gitkeep. Это позволит Git учитывать каталог, даже если он не содержит файлов.


