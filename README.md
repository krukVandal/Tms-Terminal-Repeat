# Задача: Повторение пройденного материала
# Работа с файлами

1. Определить модель процессора, используя в качестве источника данных файл `/proc/cpuinfo`

<img width="628" height="150" alt="image" src="https://github.com/user-attachments/assets/ad14f4b1-068d-481c-b59e-644c8a4b0c8f" />

2. Вывести список всех портов в состоянии `LISTEN` на `ВМ`

<img width="804" height="342" alt="image" src="https://github.com/user-attachments/assets/85e94f82-c0ba-4167-8df4-7ac02575be81" />

3. Найти процесс запущенного выше приложения и вывести его `PID`

<img width="638" height="164" alt="image" src="https://github.com/user-attachments/assets/780baeb0-db90-475b-859c-2b3f3cb92a27" />

4. Из вывода команды `ip -4 -o a` вывести только `ip-адреса`

<img width="1001" height="174" alt="image" src="https://github.com/user-attachments/assets/8c25a9c6-8bc5-449a-9345-f75790d12bdc" />

5. Отфильтровать из вывода команды `dmesg` только ошибки

<img width="1001" height="174" alt="image" src="https://github.com/user-attachments/assets/543e8748-8fb0-4479-bcce-a517fe9b703c" />

6. Создать файл `ssh_list.txt`, содержимым которого будет результат команды `ls -l /etc/ssh/`

<img width="670" height="435" alt="image" src="https://github.com/user-attachments/assets/8bf3ae37-bc35-477d-b2d9-e4e013b5197a" />

7. Выполнить команду `cat ssh_list.txt nosuchfile.txt`; стандартный поток ошибок `(stderr)` перенаправить в файл `errors.log`

<img width="751" height="447" alt="image" src="https://github.com/user-attachments/assets/bc855043-ad69-4612-b66c-7f9c3ad82c4a" />

8. Выполнить команду `cat ssh_list.txt nosuchfile.txt`, но теперь ОБА потока `(stdout и stderr)` перенаправить в файл `output.log`

<img width="751" height="447" alt="image" src="https://github.com/user-attachments/assets/764f45fc-3a86-48d1-8e8b-376e6b175bc9" />

9. В файле `ssh_list.txt` найти все строки, содержащие `config` и одновременно вывести результат на экран, и в файл `ssh_confs.txt`

<img width="667" height="278" alt="image" src="https://github.com/user-attachments/assets/0f5b135a-b0ce-45a8-8b89-f0d3d3258944" />

10. С помощью cat создать файл `hello_cat` с содержимым

<img width="455" height="368" alt="image" src="https://github.com/user-attachments/assets/b27b4140-0ea4-4ed0-9dce-c0fd2981b75d" />


# Работа с пользователями

1. Создать директорию `/opt/srv/backups` с владельцем `root` и группой владельцев `admins`; назнчить ей права, при которых
   - владелец может делать все
   - группа может делать все
   - все остальные не могут ничего

<img width="550" height="289" alt="image" src="https://github.com/user-attachments/assets/0a674244-ab4c-4c54-b9ce-fe6f429edf12" />

2. Создать пользователя `backup`, добавить его в группу `admins`

<img width="578" height="192" alt="image" src="https://github.com/user-attachments/assets/9f4b5b82-a6bc-414b-8664-9e2a3710cf32" />

3. Создать группу `web-users`

<img width="578" height="192" alt="image" src="https://github.com/user-attachments/assets/5b70dd1e-e4d1-48ca-8989-c61147b475de" />

4. Переключиться на пользователя backup и проверить доступ к директории `/opt/srv/backups` создав там файл `test-bkp` с содержимым `Test backup` --->> `(Недочитал написал 123 здесь создал без оболочки в следующем пример с оболочкой сделал)` 

<img width="598" height="533" alt="image" src="https://github.com/user-attachments/assets/2b86b431-8915-44ae-b113-08f8a5ba7f71" />

5. Создать директорию `/opt/srv/nginx`, установить владельцем директории `www-data`, а группой `web-users`; назначить права на директорию
   - владелец может все
   - группа может читать и исполнять
   - все остальные не могут ничего

<img width="596" height="240" alt="image" src="https://github.com/user-attachments/assets/ef0c5929-b3a1-41f4-be87-69659298c784" />

6. Создать пользователя `designer` и добавить его в группу `web-users`

<img width="596" height="240" alt="image" src="https://github.com/user-attachments/assets/46024260-2268-4304-a00c-5c7e94608a15" />

7. Переключиться на пользователя `designer` и проверить доступ к директории `/opt/srv/nginx` - создать в ней файл `server.conf` с любым содержимым Выйти из под пользователя `designer` и добавить группе `web-users` права на запись в `/opt/srv/nginx`; снова переключиться на `designer` и попробовать создать `server.conf` с любым содержимым

<img width="614" height="494" alt="image" src="https://github.com/user-attachments/assets/b5b7951e-ae0f-4ea0-9478-b1d23b7e49dd" />

8. Создать сервисного (служебного) пользователя `backend` без возможности входа в систему

<img width="618" height="135" alt="image" src="https://github.com/user-attachments/assets/9c4d0d7e-f9a3-4e4e-b80d-fe2a331b0c28" />

9. Переименовать пользователя `backend` в `apps-user`. Изменился ли `UID`? `UID` не изменился

<img width="454" height="134" alt="image" src="https://github.com/user-attachments/assets/e203ea53-b793-4515-9a6f-26d8b6e7e1f3" />

# Запуск Демона-1 Оранжевые Кнопки

   - Клонировал репозиторий
   - Создал виртуальное окружение `-m venv /opt/srv/orange-buttons/.venv`
   - Активировал виртуальное окружение source `/opt/srv/orange-buttons/.venv/bin/activate`
   - Установил зависимости и деактивировал виртуальное окружение.

<img width="902" height="357" alt="image" src="https://github.com/user-attachments/assets/9945e7f8-b7d5-4ad5-baa7-651bb912cc62" />

<img width="1157" height="649" alt="image" src="https://github.com/user-attachments/assets/9d57e3b7-85dd-418c-98bc-62e49f9167ae" />

<img width="1211" height="700" alt="image" src="https://github.com/user-attachments/assets/9601c220-3c14-4bd7-8b7c-191ff3cc7ad1" />


# Запуск Демона-2 Http-server

1. Клонировал репозиторий, создал пользователя, создал группу, добавил пользователя в группу и сменил владельцев директории

<img width="814" height="252" alt="image" src="https://github.com/user-attachments/assets/d5cffca0-7120-4955-9d9b-da2bec8f6f61" />

2. Создал виртуальное окружение и показал владельцев

<img width="815" height="275" alt="image" src="https://github.com/user-attachments/assets/8634888c-5f9c-4424-b054-dd8cc4ab51c4" />

3. Конфиг unit

<img width="805" height="657" alt="image" src="https://github.com/user-attachments/assets/3e954b45-ea13-4d19-b4f6-b38b3db2d135" />

4. На первом запуске получил ошибку no such directory

<img width="1010" height="492" alt="image" src="https://github.com/user-attachments/assets/22379d41-b91d-4f97-8910-61783cb2a5c4" />

5. Отредактировал файл app.py, а именно метод os.chdir() - возможно намеренно была допущена ошибка в директории и создал папку content

<img width="651" height="477" alt="image" src="https://github.com/user-attachments/assets/74a956ab-6c4b-47fc-8269-0427a2591ef3" />

6. Демон запустился без ошибок

<img width="834" height="332" alt="image" src="https://github.com/user-attachments/assets/b03c9281-ed6b-4968-ae63-58dfcad838f9" />

