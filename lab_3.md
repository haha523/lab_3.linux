## Лабораторная работа No3

- [ ] [Задача 1 - Множество](https://github.com/haha523/lab_3.linux/blob/d874b1960dfbc96844691ff2125a55f7da472f17/README.md)
1\. Скачайте и установите VirtualBox:

![image](https://github.com/haha523/lab_3.linux/blob/eb413558a19fa99f14d64e95878da6451d4f7ecb/png%20for%20lab%203/h%C3%ACnh%20c%E1%BB%A7a%20app.png)

2\. Создание виртуальной машины A с Ubuntu:

![image](https://github.com/haha523/lab_3.linux/blob/d8e4d9d7ab8b79fab9d48707a8310e55ac5df978/png%20for%20lab%203/m%C3%A1y%20A.png)

3\. Создание виртуальной машины B и C с Ubuntu:

![image](https://github.com/haha523/lab_3.linux/blob/d8e4d9d7ab8b79fab9d48707a8310e55ac5df978/png%20for%20lab%203/giao%20di%E1%BB%87n%20c%E1%BA%A3%203%20m%C3%A1y.png)

4\. Проверка доступа в интернет на:

Используем команду: 

```bash
ping -c 4 google.com 
```

⦁ Машина А:

![image](https://github.com/haha523/lab_3.linux/blob/d8e4d9d7ab8b79fab9d48707a8310e55ac5df978/png%20for%20lab%203/th%E1%BB%AD%20m%E1%BA%A1ng%20m%C3%A1y%20A.png)

⦁ Машина B:

![image](https://github.com/haha523/lab_3.linux/blob/d8e4d9d7ab8b79fab9d48707a8310e55ac5df978/png%20for%20lab%203/th%E1%BB%AD%20m%E1%BA%A1ng%20m%C3%A1y%20B.png)

⦁ Машина C:

![image](https://github.com/haha523/lab_3.linux/blob/d8e4d9d7ab8b79fab9d48707a8310e55ac5df978/png%20for%20lab%203/th%E1%BB%AD%20m%E1%BA%A1ng%20m%C3%A1y%20C.png)

5\. Поиска IP - адрес:

Используем команду: 
```bash
ifconfig
```

⦁ Машина А:

![image](https://github.com/haha523/lab_3.linux/blob/d8e4d9d7ab8b79fab9d48707a8310e55ac5df978/png%20for%20lab%203/ip%20m%C3%A1y%20A.png)


⦁ Машина B:

![image](https://github.com/haha523/lab_3.linux/blob/d8e4d9d7ab8b79fab9d48707a8310e55ac5df978/png%20for%20lab%203/ip%20m%C3%A1y%20B.png)

⦁ Машина C:

![image](https://github.com/haha523/lab_3.linux/blob/d8e4d9d7ab8b79fab9d48707a8310e55ac5df978/png%20for%20lab%203/ip%20m%C3%A1y%20C%20(a).png)

6\. Проверка сетевого доступа:

Используем команду: 
```bash
ping -c 4 [IP_of_машины_]
```

⦁ На машины А:

![image](https://github.com/haha523/lab_3.linux/blob/d8e4d9d7ab8b79fab9d48707a8310e55ac5df978/png%20for%20lab%203/k%E1%BA%BFt%20n%E1%BB%91i%20ip%20tr%C3%AAn%20m%C3%A1y%20A.png)

⦁ На машины B:

![image](https://github.com/haha523/lab_3.linux/blob/d8e4d9d7ab8b79fab9d48707a8310e55ac5df978/png%20for%20lab%203/k%E1%BA%BFt%20n%E1%BB%91i%20ip%20tr%C3%AAn%20m%C3%A1y%20B.png)

⦁ На машины C:

![image](https://github.com/haha523/lab_3.linux/blob/d8e4d9d7ab8b79fab9d48707a8310e55ac5df978/png%20for%20lab%203/k%E1%BA%BFt%20n%E1%BB%91i%20ip%20tr%C3%AAn%20m%C3%A1y%20C.png)

7\. Запрета доступа из B в C:

Выполнит команду на машины В:
```bash 
sudo iptables -A OUTPUT -d <<IP - адрес С>> -j DROP
```
![image](https://github.com/haha523/lab_3.linux/blob/d8e4d9d7ab8b79fab9d48707a8310e55ac5df978/png%20for%20lab%203/ch%E1%BA%B7n%20k%E1%BA%BFt%20n%E1%BB%91i%20tr%C3%AAn%20m%C3%A1y%20B.png)

Или Выполнит команду на машины C: 
```bash 
sudo iptables -A INPUT -s <<IP - адрес B>> -j DROP
```
![image](https://github.com/haha523/lab_3.linux/blob/d8e4d9d7ab8b79fab9d48707a8310e55ac5df978/png%20for%20lab%203/ch%E1%BA%B7n%20k%E1%BA%BFt%20n%E1%BB%91i%20tr%C3%AAn%20m%C3%A1y%20C.png)

8\. Результат:

⦁ Машина А:

![image](https://github.com/haha523/lab_3.linux/blob/d8e4d9d7ab8b79fab9d48707a8310e55ac5df978/png%20for%20lab%203/k%E1%BA%BFt%20qu%E1%BA%A3%20k%E1%BA%BFt%20n%E1%BB%91i%20tr%C3%AAn%20m%C3%A1y%20A.png)

⦁ Машина B:

![image](https://github.com/haha523/lab_3.linux/blob/d8e4d9d7ab8b79fab9d48707a8310e55ac5df978/png%20for%20lab%203/k%E1%BA%BFt%20qu%E1%BA%A3%20k%E1%BA%BFt%20n%E1%BB%91i%20tr%C3%AAn%20m%C3%A1y%20B.png)

⦁ Машина C:

![image](https://github.com/haha523/lab_3.linux/blob/d8e4d9d7ab8b79fab9d48707a8310e55ac5df978/png%20for%20lab%203/k%E1%BA%BFt%20qu%E1%BA%A3%20k%E1%BA%BFt%20n%E1%BB%91i%20tr%C3%AAn%20m%C3%A1y%20C.png)

Цель:

 
  ⦁  Проверка доступа в интернет на машины.

 
  ⦁  Проверка сетевого доступа из одной машины на другую машину.

 
  ⦁  Запрета доступа из одной машины на другую машину.




























