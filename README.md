# Описание плэйбуков
## monitoring.yml
Копируем конфиги с локальной машины на удаленный хосты для Zabbix мониторинга. Перезапускаем Zabbix агент, чтобы подцепить изменения. Шаблон с элементами данных и тригеррами уже готов. После запуска плэйбука через пару минут срабатывают триггеры, если версия Ubuntu и(или) Nginx неактуальная.

## get_data.yml
Делаем запрос на хосты о текущих версиях Ubuntu и  Nginx для проверки актуальности.

## update.yml
Копируем необходимые конфиги для последующего бэкапа, который перенесем на локальный хост. После чего копируем на удаленные хосты актуальный sources.list для обновления через Nexus. Запускаем обновление, после которого делаем перезагрузку системы.
