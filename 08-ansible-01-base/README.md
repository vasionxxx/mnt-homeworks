# Домашнее задание к занятию 1 «Введение в Ansible»  - Бодарев В.В.

---

1.Запустим playbook, зафиксируем значение some_fact.

![image alt](https://github.com/vasionxxx/ans/blob/main/1.jpg)

---

2.Найдем файл с переменными (group_vars) и поменяем его на all default fact.

![image alt](https://github.com/vasionxxx/ans/blob/main/2.jpg)

---

3.Воспользуемся окружением используя docker.

![image alt](https://github.com/vasionxxx/ans/blob/main/3.jpg)

---

4. Запустим playbook на окружении из prod.yml. Увидим значения some_fact для каждого из managed host.

![image alt](https://github.com/vasionxxx/ans/blob/main/4.jpg)

---

5. Добавим факты в group_vars каждой из групп хостов так, чтобы для some_fact получились значения: для deb — deb default fact, для el — el default fact.

![image alt](https://github.com/vasionxxx/ans/blob/main/5.jpg)

---

6.Повторим запуск playbook.

![image alt](https://github.com/vasionxxx/ans/blob/main/6.jpg)

---

7.При помощи ansible-vault зашифруем факты в group_vars/deb и group_vars/el с паролем netology.

![image alt](https://github.com/vasionxxx/ans/blob/main/7.jpg)

---

8.Запустим playbook, введем пароль установленный на прошлом этапе. 

![image alt](https://github.com/vasionxxx/ans/blob/main/8.jpg)

---

9.Добавим новую группу хостов.

![image alt](https://github.com/vasionxxx/ans/blob/main/9.jpg)

---

10.Запустим playbook. 

![image alt](https://github.com/vasionxxx/ans/blob/main/10.jpg)

---
