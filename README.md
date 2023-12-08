Apps-role
=========

Ansible role для установки Wordpress.
Состоит из следующих действий:
- Установка и настройка web-сервера nginx - [nginx.yml](https://github.com/roman-serdyukov/apps-server-role/blob/main/tasks/nginx.yml).
- Установка необходимых пакетов php - [php.yml](https://github.com/roman-serdyukov/apps-server-role/blob/main/tasks/php.yml).
- Установка Wordpress [wordpress.yml](https://github.com/roman-serdyukov/apps-server-role/blob/main/tasks/wordpress.yml).

Requirements
------------

Работоспособность протестирована на Ubuntu 20.04.


Role Variables
--------------

- domain_zones:   имя поддомена
- my_domain:      доменное имя
- mysql_host:     сервер mysql
- wp_version:     версия Wordpress
- db1_ip, db2_ip: для файла hosts
- Имена пользователей, баз данных и пароли в папке "vars" (приведены здесь только для демонстрации)

Example Playbook
----------------
```
- name: Install apps server
  hosts: servers
  roles:
    - apps-server-role
```

Before start
----------------

- Если нет внутрненнего DNS сервера, то раскоментировать play hosts.yml.

License
-------

MIT

Author Information
------------------

Сердюков Роман
reserdukov@gmail.com