Входящие параметры:

1. Имя папки для мониторинга.

2. Интервал времени мониторинга.

3. E-mail адрес для отправки уведомления.

4. Вышеперечисленные параметры должны считываться из конфигурационного файла(пример добавлю)

Постановка задачи:

При старте скрипт перечитывает конигурационный файл 4 и получает из него входящие параметры 1,2,3.

Далее скрипт мониторит (просматривает) входящую папку 1 с интервалом времени 2.

При появлении нового файла или директории в папке, пользователю отправляется почтовое сообщение на адрес 3.

В сообщении должно быть указано имя нового файла, его размер и время появления в папке(или время создания самого файла или директории).


P.S.
Для отправки сообщений электронной почты рекомендую использовать Net::SMTP( require 'net/smtp' )

[20120711]
1. Для того, что б и у Вас работало нужно поправить настройки почты и конф файл.
    1.1 В идеале нужно сделать чтоб все параметры настройек были прописаны в конф файле.
2. Для работы с конф файлом использовал гем parseconfig( с целью обучения конечно можна написать свой).
3. Ожидаю шквал критики, замечаний, лучше так, чем вообще ничего не далать...