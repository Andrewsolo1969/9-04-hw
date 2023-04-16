# Домашнее задание к занятию "9.4 «Система мониторинга Prometheus»" - Соловьёв Андрей SYS-18

При выполнении задания в  использована домашняя машина c Ubuntu 22.04

Prometheus, Node Exporter и Grfana установлены на  виртуальную машину 192.168.122.104 

На 192.168.122.198 установлен Node Exporter

---

## Задание 1

Установите Prometheus.

### Процесс выполнения

1. Выполняя ДЗ сверяйтесь с процессом отражённым в записи лекции.
2. Создайте пользователя Prometheus. 
3. Скачайте Prometheus и в соответствии с лекцией разместите файлы в целевые директории.
4. Создайте сервис как показано на уроке
5. Проверьте что prometheus запускается, останавливается, перезапускается и отображает статус с помощью systemctl.

Prometheus остановлен.

![Prometheus остановлен](https://github.com/Andrewsolo1969/9-04-hw/blob/main/img/Prometheus_stop.png)

Prometheus запущен.

![Prometheus запущен](https://github.com/Andrewsolo1969/9-04-hw/blob/main/img/Prometheus_start.png)

### Требования к результаты

- Прикрепите к файлу README.md скриншот systemctl status prometheus, где будет написано: prometheus.service — Prometheus Service Netology Lesson 9.4 — [Ваши ФИО]

Добавление данных учащегося можно произвести путём редактирования файл сервиса - Description

sudo nano /etc/systemd/system/prometheus.service

![ФИО](https://github.com/Andrewsolo1969/9-04-hw/blob/main/img/fio.png)

![ФИО2](https://github.com/Andrewsolo1969/9-04-hw/blob/main/img/fio2.png)


## Задание 2

Установите Node Exporter.

Процесс выполнения

1. Выполняя ДЗ сверяйтесь с процессом отражённым в записи лекции.
2. Скачайте node exporter приведённый в презентации и в соответствии с лекцией разместите файлы в целевые директории
3. Создайте сервис для как показано на уроке
4. Проверьте что node exporter запускается, останавливается, перезапускается и отображает статус с помощью systemctl

![NE_stop](https://github.com/Andrewsolo1969/9-04-hw/blob/main/img/NE_stop.png)

![NE_start](https://github.com/Andrewsolo1969/9-04-hw/blob/main/img/NE_start.png)

Требования к результату

- Прикрепите к файлу README.md скриншот systemctl status node-exporter, где будет написано: node-exporter.service — Node Exporter Netology Lesson 9.4 — [Ваши ФИО]

Добавление данных учащегося можно произвести путём редактирования файл сервиса - Description - также, как и для файла сервиса Prometheus

![NE_FIO](https://github.com/Andrewsolo1969/9-04-hw/blob/main/img/NE_FIO.png)


Node-exporter на хосте 192.168.122.198 


![NE_FIO_198](https://github.com/Andrewsolo1969/9-04-hw/blob/main/img/NE_FIO_198.png)


## Задание 3

Подключите Node Exporter к серверу Prometheus.

Процесс выполнения

1. Выполняя ДЗ сверяйтесь с процессом отражённым в записи лекции.
2. Отредактируйте prometheus.yaml, добавив в массив таргетов установленный в задании 2 node exporter
3. Перезапустите prometheus
4. Проверьте что он запустился

Требования к результату

 Прикрепите к файлу README.md скриншот конфигурации из интерфейса Prometheus вкладки Status > Configuration

 nano /etc/prometheus/prometheus.yml

![prometheus.yml](https://github.com/Andrewsolo1969/9-04-hw/blob/main/img/prometheus_yml.png)

 Прикрепите к файлу README.md скриншот из интерфейса Prometheus вкладки Status > Targets, чтобы было видно минимум два эндпоинта

 ![targets](https://github.com/Andrewsolo1969/9-04-hw/blob/main/img/targets.png)


 ## Задание 4*

Установите Grafana.

Требования к результату

 Прикрепите к файлу README.md скриншот левого нижнего угла интерфейса, чтобы при наведении на иконку пользователя были видны ваши ФИО

 [Grafana](https://github.com/Andrewsolo1969/9-04-hw/blob/main/img/Grafana.png)

## Задание 5*
Интегрируйте Grafana и Prometheus.

Требования к результату

 Прикрепите к файлу README.md скриншот дашборда (ID:11074) с поступающими туда данными из Node Exporter

 [NE_full](https://github.com/Andrewsolo1969/9-04-hw/blob/main/img/NE_full.png)

 
