# Домашнее задание к занятию 1 «Введение в Ansible» - Виктория Задвинская

## Подготовка к выполнению

1. Установите Ansible версии 2.10 или выше.
2. Создайте свой публичный репозиторий на GitHub с произвольным именем.
3. Скачайте [Playbook](./playbook/) из репозитория с домашним заданием и перенесите его в свой репозиторий.

## Основная часть

1. Попробуйте запустить playbook на окружении из `test.yml`, зафиксируйте значение, которое имеет факт `some_fact` для указанного хоста при выполнении playbook.

![ans-1.jpg](https://github.com/Vi-Mars/ansible-base/blob/main/ans-1.jpg)

2. Найдите файл с переменными (group_vars), в котором задаётся найденное в первом пункте значение, и поменяйте его на `all default fact`.

![ans-2.jpg](https://github.com/Vi-Mars/ansible-base/blob/main/ans-2.jpg)

3. Воспользуйтесь подготовленным (используется `docker`) или создайте собственное окружение для проведения дальнейших испытаний.

![ans-3.jpg](https://github.com/Vi-Mars/ansible-base/blob/main/ans-3.jpg)

4. Проведите запуск playbook на окружении из `prod.yml`. Зафиксируйте полученные значения `some_fact` для каждого из `managed host`.

![ans-4.jpg](https://github.com/Vi-Mars/ansible-base/blob/main/ans-4.jpg)

5. Добавьте факты в `group_vars` каждой из групп хостов так, чтобы для `some_fact` получились значения: для `deb` — `deb default fact`, для `el` — `el default fact`.

![ans-5.jpg](https://github.com/Vi-Mars/ansible-base/blob/main/ans-5.jpg)

6.  Повторите запуск playbook на окружении `prod.yml`. Убедитесь, что выдаются корректные значения для всех хостов.

![ans-6.jpg](https://github.com/Vi-Mars/ansible-base/blob/main/ans-6.jpg)

7. При помощи `ansible-vault` зашифруйте факты в `group_vars/deb` и `group_vars/el` с паролем `netology`.

![ans-7.jpg](https://github.com/Vi-Mars/ansible-base/blob/main/ans-7.jpg)

8. Запустите playbook на окружении `prod.yml`. При запуске `ansible` должен запросить у вас пароль. Убедитесь в работоспособности.

![ans-8.jpg](https://github.com/Vi-Mars/ansible-base/blob/main/ans-8.jpg)

9. Посмотрите при помощи `ansible-doc` список плагинов для подключения. Выберите подходящий для работы на `control node`.

![ans-9.jpg](https://github.com/Vi-Mars/ansible-base/blob/main/ans-9.jpg)

10. В `prod.yml` добавьте новую группу хостов с именем  `local`, в ней разместите localhost с необходимым типом подключения.

![ans-10.jpg](https://github.com/Vi-Mars/ansible-base/blob/main/ans-10.jpg)

11. Запустите playbook на окружении `prod.yml`. При запуске `ansible` должен запросить у вас пароль. Убедитесь, что факты `some_fact` для каждого из хостов определены из верных `group_vars`.

![ans-11.jpg](https://github.com/Vi-Mars/ansible-base/blob/main/ans-11.jpg)

12. Заполните `README.md` ответами на вопросы. Сделайте `git push` в ветку `master`. В ответе отправьте ссылку на ваш открытый репозиторий с изменённым `playbook` и заполненным `README.md`.

![ans-12.jpg](https://github.com/Vi-Mars/ansible-base/blob/main/ans-12.jpg)  

13. Предоставьте скриншоты результатов запуска команд.

![ans-13.jpg](https://github.com/Vi-Mars/ansible-base/blob/main/ans-13.jpg)







НЕ ВЫПОЛНЯЛА:
## Необязательная часть

1. При помощи `ansible-vault` расшифруйте все зашифрованные файлы с переменными.
2. Зашифруйте отдельное значение `PaSSw0rd` для переменной `some_fact` паролем `netology`. Добавьте полученное значение в `group_vars/all/exmp.yml`.
3. Запустите `playbook`, убедитесь, что для нужных хостов применился новый `fact`.
4. Добавьте новую группу хостов `fedora`, самостоятельно придумайте для неё переменную. В качестве образа можно использовать [этот вариант](https://hub.docker.com/r/pycontribs/fedora).
5. Напишите скрипт на bash: автоматизируйте поднятие необходимых контейнеров, запуск ansible-playbook и остановку контейнеров.
6. Все изменения должны быть зафиксированы и отправлены в ваш личный репозиторий.

---

