# tg_bot_net

Этот проект создан что бы можно было развернуть телеграмм бота внутри локальной сети
Предоставляет возможность выполнять на данный момент минимальные сетевые проверки\
\
Все модули необходимые для работы бота описаны в requirements.txt\
\ 
Проект мой личный, им занимаюсь исключительно я, он находится в состоянии дополнения \
по необходимсоти, переодически возвращаюсь к нему чтобы навести красоту или добавить \
функционал. \
\
Работает  на Ubuntu 22.04 + Python3.10\
\
Может выполнять  
-  ping
-  tracert
-  port ping
-  nslookup
-  generate password
-  Check zabbix status
-  whois
-  speedtest
 
###             ВАЖНЫЕ УСЛОВИЯ            

* Формат заполнения conf.ini :
    - [dns]\
       server=ip_вашего_dns_сервера,ip_вашего_2-го_dns_сервера
>Если необходимо указать несколько значений в настройках, то используйте этот шаблон(но не везде это сработает)\
>Для работы с ботом обязательно надо ввести свой id telegram в файл conf.ini\
>Для работы nslookup требуется вести dns сервер

* nslookup.py
> name = f'{name}.local' -  Вместо local надо ввести свой dns суфикс сети или внутренего домена

* port_ping.py
> whois - функция использует локальный софт whois, установить его можено sudo apt-get install whois

* get_speedtest.py
> Для работы этого скрипта необходимо установить программу speedtest-cli\
    ```
    sudo apt-get update && sudo apt-get upgrade && sudo apt-get install speedtest-cli
    ```