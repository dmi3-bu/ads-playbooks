# Playbooks RMS

Ansible playbooks для курса Ruby Microservices.

# Зависимости

+ Ansible `2.9+`

# Установка и запуск playbooks

1. Склонируйте репозиторий:

```
git clone git@github.com:dmi3-bu/ads-playbooks.git && cd ads-playbooks
```

2. Укажите хосты в файле `hosts`

3. Определине переменные окружения для доступа к Docker Registry:

+ `DOCKER_USER`
+ `DOCKER_PASSWORD`

4. Создайте файл `secrets.yml` с содержимым:

```
rabbitmq_user
rabbitmq_password
ansible_user
ansible_ssh_pass
ansible_become_password
ads_db_name
ads_db_user
ads_db_password
auth_db_name
auth_db_user
auth_db_password
```

5. Запустите playbook

```
ansible-playbook <playbook_name>.yml
```