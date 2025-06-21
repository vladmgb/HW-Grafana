# Домашнее задание к занятию 14 «Средство визуализации Grafana»

## Обязательные задания

## Задание 1 

Используя docker-compose, развернул grafana, prometheus и node-exporter

![image](https://github.com/user-attachments/assets/878f5bd0-65d2-4c6d-ac31-ee6eb75e4050)

Залогинился в grafana, добавил datasource 

![image](https://github.com/user-attachments/assets/0eca5560-5fef-47d1-b053-c7c378a31e6c)

## Задание 2

Создал Dashboard c панелями:

- утилизация CPU для nodeexporter (в процентах, 100-idle)

  Запрос `100 - (avg(rate(node_cpu_seconds_total{job="nodeexporter",mode="idle"}[1m])) * 100)`
  
- CPULA 1/5/15

  Запросы
   ```
   avg(node_load1{job="nodeexporter"})
   avg(node_load5{job="nodeexporter"})
   avg(node_load15{job="nodeexporter"})

   ```
- количество свободной оперативной памяти

  Запрос `node_memory_MemFree_bytes`
  
- количество места на файловой системе

  Запрос `node_filesystem_avail_bytes`

Скрин всего дашборда:

![image](https://github.com/user-attachments/assets/aa55a3ab-f44d-4f69-b74d-3150ed9af6d4)


## Задание 3


## Задание 4



