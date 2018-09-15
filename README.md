# Демонстрация возможностей Kubernetes

В этом репоизитории находятся материалы, использованные в моём докладе на DevFest 2018. Конфигурация предназначена
для Google Kubernetes Engine

## 00-services.yaml

Конфигурация Service и Ingress для доступа к веб-приложению извне. Применение новой конфигурации занимает некоторое
время.

## 01-pod.yaml

Простой пример Pod, который будет в бесконечном цикле писать в лог.

## 02-deployment-hello.yaml

Пример Deployment, который запустит три реплики веб приложения. Для получения IP адреса для доступа к нему можно
воспользоваться командой `kubectl get ing`

## 03-deployment-devfest.yaml

Пример Deployment, который демонстрирует обновление сущестующего deployment (02)

## 04-tank.yaml

Job с Yandex.Tank, который демонстрирует возможности autoscaling. Для конфигурации autoscaling, можно воспользоваться
командой `kubectl autoscale deploy webapp --min=1 --max=10 --cpu-percent=5`.

