# Домашнее задание к занятию 14 «Средство визуализации Grafana»


## Обязательные задания

### Задание 1

1. Используя директорию [help](./help) внутри этого домашнего задания, запустите связку prometheus-grafana.
1. Зайдите в веб-интерфейс grafana, используя авторизационные данные, указанные в манифесте docker-compose.
1. Подключите поднятый вами prometheus, как источник данных.
1. Решение домашнего задания — скриншот веб-интерфейса grafana со списком подключенных Datasource.

![скриншот веб-интерфейса grafana](https://github.com/YuriKopshev/grafana_devops/blob/main/img/grafana1.png);

## Задание 2


Создайте Dashboard и в ней создайте Panels:

- утилизация CPU для nodeexporter (в процентах, 100-idle); 

 Ответ: 100 - (avg by (instance) (rate(node_cpu_seconds_total{mode="idle"}[5m])) * 100)

- CPULA 1/5/15;

 Ответ: node_load1, node_load5, node_load15


- количество свободной оперативной памяти;

 Ответ:  node_memory_MemAvailable_bytes 


- количество места на файловой системе.

 Ответ:  node_filesystem_avail_bytes{mountpoint="/"}


## Задание 3

1. Создайте для каждой Dashboard подходящее правило alert — можно обратиться к первой лекции в блоке «Мониторинг».
1. В качестве решения задания приведите скриншот вашей итоговой Dashboard.

![скриншот Дашборда с добавленными Panels и Alerts](https://github.com/YuriKopshev/grafana_devops/blob/main/img/grafana3.png);

## Задание 4

1. Сохраните ваш Dashboard.Для этого перейдите в настройки Dashboard, выберите в боковом меню «JSON MODEL». Далее скопируйте отображаемое json-содержимое в отдельный файл и сохраните его.
1. В качестве решения задания приведите листинг этого файла.

Ответ: Файл listing.json в корне проекта


---


