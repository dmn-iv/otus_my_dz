===================================================================================================
ДЗ по уроку Prometheus, Alertmanager - работа с метриками (PromQL), написание алертов и их ротация.

1. Развернул 2 хоста : ubuntu-srv (192.168.0.105) и ubuntu-srv2 ((192.168.0.109).
2. На ubuntu-srv развернул django на порту 8080, nginx, php7.2-fpm.service, postgresql.
 ![изображение](https://user-images.githubusercontent.com/53178698/168393669-441a6c6c-70e8-4a3e-ba21-f1b4fa949532.png)
3. Там же установил соответствующие экспортеры: nginx-exporter, node_exporter, php-fpm-exporter, postgres_exporter, blackbox-exporter.
4. На ubuntu-srv2 развернул прометеус с алертменеджером 
 ![изображение](https://user-images.githubusercontent.com/53178698/168394729-7cb2289d-4753-4304-ba11-a4505378ea29.png)

5. а так же телеграмм бота для отправки алертов в телегу https://github.com/dmn-iv/otus_my_dz/blob/main/%D0%94%D0%97-1/GAP-1/%D1%82%D0%B5%D0%BB%D0%B5%D0%B3%D1%80%D0%B0%D0%BC%D0%BC%D0%B1%D0%BE%D1%82_%D0%B0%D0%BB%D0%B5%D1%80%D1%82.JPG?raw=true


P.S.
так же на ubuntu-srv у меня был ранее развёрнут Zabbix на порту 80, я его так же замониторил через blackbox exporter

========================================================================================================================
ДЗ Grafana - продвинутое использование

1. Установил grafana server v.8.5.2, внутри графаны создал папки app и infra
2. В папку app импортировал дашборд Node Exporter Full для мониторинга инфраструктуры.
3. В папке app создал дашборд Django status для мониторинга доступности CMS Django.
4. Сделал алерты на http_status_code и CPU load.
5. Настроил алерты в телеграм.
6. Файлы со скриншотами закинул в папку GAP-2 в репозитории 
