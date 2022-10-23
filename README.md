# DevOps

Репозиторий курса DevOps.

## [Видеозаписи лекций в youtube](https://youtube.com/playlist?list=PLLELLTvDgUQ-iwnE9coLhb-ynyZUGzW6q)

## Лекции

* **Лекция 1**. [Введение в DevOps. Системы виртуализации и облачные решения (Михаил Кучеренко)](Лекции/Лекция1/АРЭПО-Л1-П.pdf)
* **Лекция 2**. Контейнеризация + БД (Михаил Кучеренко + Алексей Якубов)
* **Лекция 3**. [Контроль версий, Git, CI/CD (Дмитрий Аладин)](Лекции/Лекция3/Лекция%203.%20Контроль_версий_Git_CI_и_CD.md)
* **Лекция 4**. [Масштабируемость и отказоустойчивость + docker compose (Антон Балашов)](Лекции/Лекция4/Лекция_4_Масштабируемость_и_отказоустойчивость.pdf)
* **Лекция 5**. Мониторинг, логирование и оповещение событий (Михаил Кучеренко)
ELK и тд
* **Лекция 6**. [Конфигурационное управление. Ansible, Terraform (Антон Балашов)](Лекции/Лекция6/Лекция_6_ИТ_инфраструктура_Конфигурационное_управление.pdf)
* **Лекция 7**. Kubernetes (Алексей Якубов)
* **Лекция 8**. Облачная инфраструктура в общем. BASIS (Алексей Якубов)

Дополнительные лекции (список дополняется):

1. ML-ops (Гапанюк ЮЕ) для ДЗ
2. Terraform
3. [Думай как SRE (Михаил Кучеренко)](Лекции/Лекция1/Думай%20как%20SRE%20(simple).pdf)

## Практические занятия

### Занятие 1 (Лаб 1). Настройка виртуальной машины Linux

**Автор**: Михаил Кучеренко

[Задачи](Лабы/Лаб1/L1.pdf):

* Знакомство с Ubuntu 20.04.
* Поставить docker, через bash, сетевые интерфейсы.

### Занятие 2 (РК 1). Практические навыки работы с Docker - контейнер с PostgreSQL

**Авторы**: Михаил Кучеренко + Алексей Якубов

[Задачи](Лабы/Лаб2/L2.md):

* Первая половина:
  * Работа с PostgreSQL/MySQL
  * Docker Volume
* Вторая половина:
  * Php My Admin/Adminer во втором контейнере

### Занятие 3 (Лаб 2). Балансировка + docker-compose

**Автор**: Антон Балашов

[Задачи](Лабы/Лаб3/README.MD):

* Первая половина:
  * HTML страничка
  * Балансировщик nginx (HAProxy)
* Вторая половина:
  * веб-сервис с БД

Итог 4 взаимосвязанных контейнера в docker-compose:

1. субд postgresql, проверяем как работают volumes
2. микросервис-1, только отдает html страничку
3. микросервис-2, обращатеся в БД, сетевое взаимодействие
4. балансировщик (haproxy/nginx) с port-forwarding-ом, будет перенаправлять запросы на другие контейнеры

### Занятие 4 (ДЗ 1). Настройка CI/CD в GitLab

**Автор**: Дмитрий Аладин

[Задачи](Лабы/Лаб4):

* Первая половина:
  * Создание репозитория GitLab/GitHub
  * Управление репозиторием с помощью команд git
* Вторая половина:
  * Добавление в репозиторий проекта с юнит-тестами
  * Настройка Pipeline в GitLab/GitHub:
    * Проверка качества кода
    * Активация юнит-тестов
    * Сборка проекта в бинарник и публикация в артефакты Releases
  * Настройка Runner-ов
  * Активация настроенных Pipeline

### Занятие 5 (Лаб 3). Мониторинг: Prometehus + Grafana + Alertmanager

**Автор**: Михаил Кучеренко

Задачи:

* Установили Prometheus + Grafana + Alertmanager.
* Настроили мониторинг, написали конфиги.
* Если плохо - использовать готовый образ

### Занятие 6 (ДЗ 2). Ansible, Playbook

**Автор**: Антон Балашов

Задачи:

* Создаем виртуалку поменьше чтобы мониторить из первой виртуалки
* Пишем playbook, который автоматизирует развертывание виртуалки
* В конце выключаем 2 имеющихся виртуалки

### Занятие 7 (Лаб 4). Развертывание кластера Kubernetes

**Автор**: Алексей Якубов

Задачи:

* minikube - 8 RAM достаточно. Из коробки не заработает. Для тех, у кого мощные машины - у большинства, дадим в кластере
* В отдельной виртуалке кубер. Много манифестов написать

Итог - все контейнеры поднять в кубере и замониторить

### Занятие 8 (РК 2). Индивидуальное задание
Развернуть свой проект из 5 лабораторной курса РИП в контейнеры Docker Compose: Django + ORM + таблица в MySQL (без AJAX, SPA и React)

**Автор**: Алексей Якубов


### Задание на +1 балл

По вашей дипломной работе необходимо создать контейнеры Docker Compose, без Kubernetes
Например React, Django REST или что-то свое

## Практикум в BASIS
По ДЗ BASIS от Ростелеком: Helm, и тд - только для сертификата Ростелекома