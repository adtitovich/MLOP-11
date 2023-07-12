# Домашняя работа к занятию “ CI/CD”

# Задание:
Сделать playbook .gitlab-ci.yaml по следующим критериям:<br>
1. Используем в тасках tag - netology<br>
2. Шаги - build, test<br>
3. В билде должен выполняться скрипт из шагов:<br>
 - начало Building<br>
 - создание папки build<br>
 - создание файла в этой папке info.txt<br>
4. В тесте:<br>
 - выводим Testing<br>
 - проверяем наличие файла info.txt в папке build<br>


> hosts - inventory<br>
> homework.yaml, groups_users.yml - playbooks<br>
> Dockerfile - для образа Ubuntu с Openssh<br>
> result.png - скрин результата выполнения playbook<br>
