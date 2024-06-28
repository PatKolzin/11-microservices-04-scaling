
# Домашнее задание к занятию «Микросервисы: масштабирование»

Вы работаете в крупной компании, которая строит систему на основе микросервисной архитектуры.
Вам как DevOps-специалисту необходимо выдвинуть предложение по организации инфраструктуры для разработки и эксплуатации.

## Задача 1: Кластеризация

Предложите решение для обеспечения развёртывания, запуска и управления приложениями.
Решение может состоять из одного или нескольких программных продуктов и должно описывать способы и принципы их взаимодействия.

Решение должно соответствовать следующим требованиям:
- поддержка контейнеров;
- обеспечивать обнаружение сервисов и маршрутизацию запросов;
- обеспечивать возможность горизонтального масштабирования;
- обеспечивать возможность автоматического масштабирования;
- обеспечивать явное разделение ресурсов, доступных извне и внутри системы;
- обеспечивать возможность конфигурировать приложения с помощью переменных среды, в том числе с возможностью безопасного хранения чувствительных данных таких как пароли, ключи доступа, ключи шифрования и т. п.

Обоснуйте свой выбор.
### Ответ:
Для обеспечения развёртывания, запуска и управления приложениями, удовлетворяющего указанным требованиям, я предлагаю использовать следующее решение:

Kubernetes: платформа для оркестрации контейнеров, которая обеспечивает управление и автоматизацию развёртывания, масштабирования и управления контейнеризированными приложениями. Kubernetes поддерживает контейнеры и обеспечивает горизонтальное и автоматическое масштабирование приложений.

Service Discovery и Ingress Controller: Для обнаружения сервисов и маршрутизации запросов внутри кластера можно использовать встроенный механизм Service Discovery в Kubernetes. Для маршрутизации запросов извне кластера можно использовать Ingress Controller, который позволяет управлять входящим трафиком и настраивать правила маршрутизации.

Horizontal Pod Autoscaler (HPA): HPA - это механизм в Kubernetes, который позволяет автоматически масштабировать количество экземпляров приложений на основе наблюдаемых метрик, таких как загрузка CPU или количество запросов. HPA обеспечивает горизонтальное масштабирование приложений в зависимости от текущей нагрузки.

Secrets и ConfigMaps: Kubernetes предоставляет механизмы Secrets и ConfigMaps для хранения конфигурационных данных и чувствительных данных, таких как пароли, ключи доступа и ключи шифрования. Secrets и ConfigMaps могут быть использованы для конфигурирования приложений с помощью переменных среды, обеспечивая безопасное хранение и передачу чувствительных данных.

Компоненты взаимодействуют следующим образом: Kubernetes управляет развёртыванием и масштабированием контейнеризированных приложений. Service Discovery обеспечивает обнаружение сервисов внутри кластера. Ingress Controller управляет маршрутизацией входящего трафика. HPA автоматически масштабирует количество экземпляров приложений на основе наблюдаемых метрик. Secrets и ConfigMaps используются для безопасного хранения и передачи конфигурационных данных и чувствительных данных.

Это решение обеспечивает гибкое и масштабируемое развёртывание, запуск и управление приложениями в контейнерной среде. Kubernetes обеспечивает автоматизацию операций с контейнерами, горизонтальное и автоматическое масштабирование, а также явное разделение ресурсов. Механизмы Service Discovery, Ingress Controller и HPA обеспечивают управление сетевым трафиком, обнаружение сервисов и масштабирование приложений. Secrets и ConfigMaps позволяют безопасно хранить и передавать конфигурационные данные и чувствительные данные.

## Задача 2: Распределённый кеш * (необязательная)

Разработчикам вашей компании понадобился распределённый кеш для организации хранения временной информации по сессиям пользователей.
Вам необходимо построить Redis Cluster, состоящий из трёх шард с тремя репликами.

### Схема:

![11-04-01](https://user-images.githubusercontent.com/1122523/114282923-9b16f900-9a4f-11eb-80aa-61ed09725760.png)

---

### Как оформить ДЗ?

Выполненное домашнее задание пришлите ссылкой на .md-файл в вашем репозитории.

---
