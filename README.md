                                                             
# Mission 3

## Part 1 - Авторизация

[Link to video](https://drive.google.com/file/d/1ovCeGn2VdgDO5sDKxyE3ox7ohzXg8f1H/view?usp=drive_link)

## Part 2 - Отправка сообщения

[Link to video](https://drive.google.com/file/d/1KQE20_Zb59XLIDGHCMMz49br943I2ruK/view?usp=drive_link)

## Part 3 - Select’ы
[Link to video](https://drive.google.com/file/d/1lJ838N6PGIEiPyBElV5xgM-dYozrVEWl/view?usp=sharing)

### Получить список юзернеймов пользователей
```sql
SELECT username FROM users;

**### Получить количество отправленных сообщений каждым пользователем:**

username - number of sent messages
SELECT username, COUNT(*) AS number_of_sent_messages
FROM users AS u 
JOIN messages AS m ON u.id = m.from
GROUP BY username;

**### Получить пользователя с самым большим количеством полученных сообщений и само количество:**
 username - number of received messages
SELECT username, COUNT(*) AS number_of_received_messages
FROM users AS u 
JOIN messages AS m ON u.id = m.to
GROUP BY username
ORDER BY number_of_received_messages DESC
LIMIT 1;

### **Получить среднее количество сообщений, отправленное каждым пользователем**
SELECT ROUND(
    (SELECT AVG(t.number_of_sent_messages)
     FROM (
         SELECT username, COUNT(*) AS number_of_sent_messages
         FROM users AS u 
         JOIN messages AS m ON u.id = m.from
         GROUP BY username
     ) AS t), 2
);
rfr 
