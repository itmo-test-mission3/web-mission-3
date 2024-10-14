                                                             
# Mission 2

## Part 0

[Link to video](https://drive.google.com/drive/folders/17cG03wHaxsOP9Cz8LHx_p6ZBMkbx58l8?usp=sharing)

## Part 1

- Вопрос 1
Зачем нужен ssh? Ответ на пару предложений.
>Ответ:
SSH (Secure Shell) — это сетевой протокол, используемый для безопасного удаленного доступа к компьютерам и серверам. Он обеспечивает шифрование данных, что защищает информацию от перехвата и атак.


- Вопрос 2
Предположим, у вас есть прямой доступ к серверу(терминалу) под управлением ubuntu. У вас есть коллега Вася, который хочет получить доступ к этому серверу. Он генерирует пару ssh ключей с помощью команды ssh-keygen и дает вам свой публичный ключ. В какой файл на сервере нужно записать ключ, чтобы Вася смог подключиться к терминалу сервера?
>Ответ:
Открытый ключ нужно положить в файл ~/.ssh/authorized_keys в корневой директории пользователя. Также необходимо настроить права доступа, чтобы файл был недоступен для записи посторонним пользователям, иначе SSH его не примет.


- Вопрос 3
Тут вопрос про АПИ. Разберитесь, что такое long polling и webhooks, опишите сами в нескольких предложениях, как они работают. https://grammy.dev/guide/deployment-types 
Ответ
Long polling — это метод, при котором клиент отправляет запрос на сервер и остаётся в ожидании ответа. Сервер не отвечает сразу, а удерживает соединение открытым до тех пор, пока не появятся новые данные. Как только сервер отправляет ответ, клиент снова отправляет запрос, создавая иллюзию постоянного соединения.
Webhooks — это метод, позволяющий серверам отправлять данные или уведомления в реальном времени по заранее заданному URL, который указывает клиент или другой сервис. Вместо того чтобы клиент запрашивал данные, сервер отправляет их сразу, когда происходят изменения, что делает взаимодействие более эффективным.



- Вопрос 4
Найдите информацию, что такое issues на гитхабе и для чего нужны. Также вставьте ссылки на пару примеров issues в популярных open source проектах.
> Ответ
Issues на GitHub — это система для отслеживания задач, ошибок и запросов, помогающая управлять разработкой проекта. Она используется для обсуждения и планирования работы, где участники могут сообщать об ошибках, предлагать новые функции и задавать вопросы.
kubernetes/kubernetes#127538 


- Вопрос 5
Ваш проект используется пустую папку images, но гит не поддерживает отслеживание пустых директорий. Что делать?
> Ответ
В images необходимо создать пустой файл с именем .gitkeep. Это позволит Git учитывать каталог, даже если он не содержит файлов.


