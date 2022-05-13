Выполненные действия в ДЗ по уроку Prometheus, Alertmanager - работа с метриками (PromQL), написание алертов и их ротация.
1. Развернул 2 хоста : ubuntu-srv (192.168.0.105) и ubuntu-srv2 ((192.168.0.109).
2. На ubuntu-srv развернул django на порту 8080, nginx, php7.2-fpm.service, postgresql.
3. ![изображение](https://user-images.githubusercontent.com/53178698/168393669-441a6c6c-70e8-4a3e-ba21-f1b4fa949532.png)
4. Там же установил соответствующие экспортеры: nginx-exporter, node_exporter, php-fpm-exporter, postgres_exporter, blackbox-exporter.
5. На ubuntu-srv2 развернул прометеус с алертменеджером 
6. ![изображение](https://user-images.githubusercontent.com/53178698/168394729-7cb2289d-4753-4304-ba11-a4505378ea29.png)

6 а так же телеграмм бота для отправки алертов в телегу 


P.S.
так же на ubuntu-srv у меня был ранее развёрнут Zabbix на порту 80, я его так же замониторил через blackbox exporter

