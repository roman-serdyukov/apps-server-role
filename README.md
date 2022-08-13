Apps-role
=========

Ansible role для установки Wordpress.
Состоит из следующих действий:
- Установка и настройка web-сервера nginx - nginx.yml.
- Установка необходимых пакетов php php.yml.
- Установка Wordpress.

Requirements
------------

Работоспособность протестирована на Ubuntu 20.04.


Role Variables
--------------

- domain_zones: имя поддомеена
- my_domain:    доменное имя
- mysql_host: сервер mysql
- wp_version: версия Wordpress
- db1_ip, db2_ip: для файла hosts
- Имена пользователей, баз данных и пароли в папке "vars"

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