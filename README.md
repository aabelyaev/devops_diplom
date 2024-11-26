# Дипломная работа Беляев А.А 

## Создание облачной инфраструктуры

<image src="IMG/1.png">
<image src="IMG/2.png">
<image src="IMG/3.png">
<image src="IMG/4.png">
Удалю все созданые ресурсы
<image src="IMG/5.png">
<image src="IMG/6.png">
<image src="IMG/7.png">
<image src="IMG/8.png">

## Создание Kubernetes кластера

При разворачивании облачной инфраструктуры автоматически заполняется файл hosts с ip адресами нод
<image src="IMG/9.png">

Установка Kubernetes кластера методом Kubespray завершена
<image src="IMG/10.png">
Конфигурационный файл создан. Теперь можно проверить доступность подов и нод кластера:
<image src="IMG/11.png">
<image src="IMG/12.png">
Развёртывание кластера успешно завершено

## Создание тестового приложения

https://github.com/aabelyaev/diplom-site
<image src="IMG/13.png">

Образ создался
<image src="IMG/14.png">

Опубликую созданный образ реестре Docker Hub
<image src="IMG/15.png">


## Подготовка системы мониторинга и деплой приложения

Kubernetes кластер доступен с рабочей машины.
<image src="IMG/16.png">
<image src="IMG/17.png">
Авторизация успешна, данные о состоянии кластера отображаются
<image src="IMG/18.png">
Проверю работу балансировщика нагрузки. Тестовое приложение будет открываться по порту 80, а Grafana будет открываться по порту 3000
<image src="IMG/19.png">
<image src="IMG/20.png">


Вот тут пожалуй единстенная проблема, у меня ни в какую не захотел подтягиваться мой image с dockerhub, хотя он там есть (см img 23), наткнулся в инете на образ lotsmansm/diplom-test-site:0.1 диплоймент завелся сходу и более менее с ним далее что-то да получилось с настройкой  CI/CD
<image src="IMG/23.png">


## Установка и настройка CI/CD
<image src="IMG/21.png">
<image src="IMG/22.png">
