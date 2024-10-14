                                                             
# Mission 3

## Part 1 - Авторизация

[Link to video](https://drive.google.com/file/d/1ovCeGn2VdgDO5sDKxyE3ox7ohzXg8f1H/view?usp=drive_link)

## Part 2 - Отправка сообщения

[Link to video](https://drive.google.com/file/d/1KQE20_Zb59XLIDGHCMMz49br943I2ruK/view?usp=drive_link)

## Part 3 - Select’ы
[Link to video](https://drive.google.com/file/d/1lJ838N6PGIEiPyBElV5xgM-dYozrVEWl/view?usp=sharing)

1. получить список юзернеймов пользователей
   ```sql
   select username from users
   ```
2. получить кол-во отправленных сообщений каждым пользователем:
   username - number of sent messages
   ```sql
   select username, count(*) as number_of_sent_messages
   from users as u join messages as m on u.id = m.from
   group by username
   ```
    
3. получить пользователя с самым большим кол-вом полученных сообщений и само количество
   username - number of received messages
   ```sql
   select username, count(*) as number_of_received_messages
   from users as u join messages as m on u.id = m.to
   group by username
   order by number_of_received_messages desc
   limit 1
   ```
4. Получить среднее кол-во сообщений, отправленное каждым пользователем
   ```sql
   select round(
   (select avg(t.number_of_sent_messages)
   from
   (select username, count(*) as number_of_sent_messages
   from users as u join messages as m on u.id = m.from
   group by username) as t)
   , 2)
   ```

