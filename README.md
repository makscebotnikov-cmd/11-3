# Домашнее задание к занятию «ELK» - `Чеботников М.Б.`

### Инструкция по выполнению домашнего задания

1. Сделайте fork [репозитория c шаблоном решения](https://github.com/netology-code/sys-pattern-homework) к себе в Github и переименуйте его по названию или номеру занятия, например, https://github.com/имя-вашего-репозитория/gitlab-hw или https://github.com/имя-вашего-репозитория/8-03-hw).
2. Выполните клонирование этого репозитория к себе на ПК с помощью команды `git clone`.
3. Выполните домашнее задание и заполните у себя локально этот файл README.md:
   - впишите вверху название занятия и ваши фамилию и имя;
   - в каждом задании добавьте решение в требуемом виде: текст/код/скриншоты/ссылка;
   - для корректного добавления скриншотов воспользуйтесь инструкцией [«Как вставить скриншот в шаблон с решением»](https://github.com/netology-code/sys-pattern-homework/blob/main/screen-instruction.md);
   - при оформлении используйте возможности языка разметки md. Коротко об этом можно посмотреть в [инструкции по MarkDown](https://github.com/netology-code/sys-pattern-homework/blob/main/md-instruction.md).
4. После завершения работы над домашним заданием сделайте коммит (`git commit -m "comment"`) и отправьте его на Github (`git push origin`).
5. Для проверки домашнего задания преподавателем в личном кабинете прикрепите и отправьте ссылку на решение в виде md-файла в вашем Github.
6. Любые вопросы задавайте в чате учебной группы и/или в разделе «Вопросы по заданию» в личном кабинете.

Дополнительные ресурсы
При выполнении задания используйте дополнительные ресурсы:

docker-compose elasticsearch + kibana;
поднимаем elk в docker;
поднимаем elk в docker с filebeat и docker-логами;
конфигурируем logstash;
плагины filter для logstash;
конфигурируем filebeat;
привязываем индексы из elastic в kibana;
как просматривать логи в kibana;
решение ошибки increase vm.max_map_count elasticsearch.
Примечание: если у вас недоступны официальные образы, можете найти альтернативные варианты в DockerHub, например, такой.

---

### Задание 1. Elasticsearch
Установите и запустите Elasticsearch, после чего поменяйте параметр cluster_name на случайный.

Приведите скриншот команды 'curl -X GET 'localhost:9200/_cluster/health?pretty', сделанной на сервере с установленным Elasticsearch. Где будет виден нестандартный cluster_name.

#### ОТВЕТ:

<img width="802" height="299" alt="1" src="https://github.com/user-attachments/assets/69c83174-4c56-43c9-8b22-5cd542c26525" />


---

### Задание 2. Kibana
Установите и запустите Kibana.

Приведите скриншот интерфейса Kibana на странице http://<ip вашего сервера>:5601/app/dev_tools#/console, где будет выполнен запрос GET /_cluster/health?pretty.

#### ОТВЕТ:

<img width="1226" height="368" alt="2" src="https://github.com/user-attachments/assets/b59ade51-65a4-48e2-921e-be6792af0647" />


---

### Задание 3. Logstash
Установите и запустите Logstash и Nginx. С помощью Logstash отправьте access-лог Nginx в Elasticsearch.

Приведите скриншот интерфейса Kibana, на котором видны логи Nginx.

#### ОТВЕТ:

<img width="1275" height="602" alt="3" src="https://github.com/user-attachments/assets/ffff6797-d921-4aaf-8fa3-6ce0c570e061" />


---

### Задание 4. Filebeat.
Установите и запустите Filebeat. Переключите поставку логов Nginx с Logstash на Filebeat.

Приведите скриншот интерфейса Kibana, на котором видны логи Nginx, которые были отправлены через Filebeat.

#### ОТВЕТ:

<img width="1271" height="603" alt="4" src="https://github.com/user-attachments/assets/056e9cb0-87d2-4747-983f-44a45c97249b" />


---

### Задание 5*. Доставка данных
Настройте поставку лога в Elasticsearch через Logstash и Filebeat любого другого сервиса , но не Nginx. Для этого лог должен писаться на файловую систему, Logstash должен корректно его распарсить и разложить на поля.

Приведите скриншот интерфейса Kibana, на котором будет виден этот лог и напишите лог какого приложения отправляется.

#### ОТВЕТ:

---
