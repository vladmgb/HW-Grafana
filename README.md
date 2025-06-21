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

Настроил алерты в каждой панели.
Пример:

![image](https://github.com/user-attachments/assets/c2293239-ab50-41c1-8d4d-f1e7a6157f31)

Настроил notification channel

![image](https://github.com/user-attachments/assets/0b436b47-39ab-47d0-916a-6bdef407eceb)

Пример алертов:

![image](https://github.com/user-attachments/assets/f35871da-5165-4820-b127-9d936373d0e1)

Итоговый дашборд:

![image](https://github.com/user-attachments/assets/4e4c3d34-d652-49bc-8674-af20266ef624)


## Задание 4



