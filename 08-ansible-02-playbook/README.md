# Домашнее задание к занятию 2 «Работа с Playbook» - Бодарев В.В.

---

Исправим ошибки и запустим ansible-lint site.yml.

![image alt](https://github.com/vasionxxx/ans/blob/main/2.jpg)

---

Запустим playbook флагом --check.

![image alt](https://github.com/vasionxxx/ans/blob/main/21.jpg)

---

Запустим playbook флагом --diff.

![image alt](https://github.com/vasionxxx/ans/blob/main/22.jpg)

---

Повторно запустим playbook флагом --diff.

![image alt](https://github.com/vasionxxx/ans/blob/main/23.jpg)

---
Описание Ansible Playbook
Этот Ansible Playbook предназначен для автоматизированной установки и настройки двух компонентов:
1.ClickHouse – аналитическая СУБД для хранения и обработки данных.
2.Vector – агент сбора логов и метрик.
Playbook выполняет установку, настройку и запуск этих сервисов на соответствующих хостах.

Что делает Playbook?
1️.Установка ClickHouse
•	Загружает пакеты ClickHouse с официального репозитория.
•	Устанавливает необходимые пакеты: ClickHouse
•	Запускает службу ClickHouse.
•	Создаёт базу данных logs (если она ещё не создана).
2️.Установка и настройка Vector
•	Загружает архив с Vector.
•	Проверяет наличие загруженного файла.
•	Создаёт директорию для установки.
•	Распаковывает Vector в указанную директорию.
•	Деплоит конфигурационный файл vector.toml.
•	Создаёт и настраивает сервис vector.service.
•	Запускает и перезапускает Vector при изменении конфигурации.

Переменные

Переменная	Описание	

clickhouse_version	Версия ClickHouse, которую нужно установить	
clickhouse_packages	Список пакетов ClickHouse для установки	
vector_version	Версия Vector, которую нужно установить	
vector_install_dir	Директория установки Vector


Используемые теги

Тег  	Описание
clickhouse	Устанавливает и настраивает ClickHouse.
vector	Устанавливает и настраивает Vector.
config	Применяет конфигурацию для Vector.
database	Создаёт базу данных в ClickHouse.

---
