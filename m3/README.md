# Домашняя работа к занятию “Ansible”

# Задание:
Необходимо написать playbook Ansible, который будет в себе содержать:<br>
1. Имя плейбука homework.yaml<br>
2. inventory, из минимум 1 хоста, если есть возможность, то 2 лучше <br>
3. Авторизация должна быть настроена через техническую уз ansible <br>
4. Наименование netology-ml<br>
5. Проверка через метод ping доступность хостов<br>
6. Через var установка пакетов net_tools, git, tree, htop, mc, vim<br>
7. Использование update<br>
8. Копирование текстового файла test.txt<br>
9. Создание в цикле групп пользователей devops_1, test_1 с созданием пользователей и директорий home devops_1, test_1<br>

> hosts - inventory<br>
> homework.yaml, groups_users.yml - playbooks<br>
> Dockerfile - для образа Ubuntu с Openssh<br>
> relult.png - скрин результата выполнения playbook<br>
