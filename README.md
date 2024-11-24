# TOIB.5
#ТОИБ ПР5 Лялин Илья Евгеньевич ББМО-02-24

1. Создадим 2 виртуальные машины на базе ОС Debian 12 и обеспечим между ними сетевой обмен с помощью сетевого моста
   
![1](https://github.com/user-attachments/assets/3c41bd06-042a-4dc4-a0d7-b350b96dc6df) 
![2](https://github.com/user-attachments/assets/7b7ab619-55e7-4d9c-819b-52ade7e20643)
![3](https://github.com/user-attachments/assets/746f9ddf-9f51-4d62-ada6-1a95cff3f132)

3. Включим на 1-й (серверной) ВМ передачу логов по протоколу rsyslog на 2-ю ВМ (клиент)

2.1 Установим и настроим rsyslog на сервере и клиенте
![4](https://github.com/user-attachments/assets/e1aa6419-ce26-4b46-b2ab-61eeb7aa99ad)

2.2 Проверим работоспособность rsyslog на сервере и клиенте
![5](https://github.com/user-attachments/assets/b52ed807-2d92-4995-83c4-40885a1dfb98)

2.3 Включим UDP и TCP соединения
![6](https://github.com/user-attachments/assets/ca6f8ba3-3ab0-4deb-bab3-c801734feb7d)

2.4 Установим правила на сервере
![7](https://github.com/user-attachments/assets/dd3ca0d7-979d-4a8d-bee4-3ea829763a90)

2.5 Установим правила на клиенте
![8](https://github.com/user-attachments/assets/90d1e309-1235-4814-a205-007527de120c)

2.6 Проверим получения логов на сервере
![9](https://github.com/user-attachments/assets/79b00d4f-f7b9-438f-9d2c-5dd884574972)
![10](https://github.com/user-attachments/assets/68409845-7103-499a-bb7b-26c401099943)

3. Установим и настроим получение логов на сервер с использованием Loki

3.1 Установим и отредактируем docker compose файл на сервере

![11](https://github.com/user-attachments/assets/c4a07b6b-d165-4df0-b2a4-b6f1f7c7c131)
![12](https://github.com/user-attachments/assets/9fb83c38-f416-44c4-b373-b1c827c558bc)

3.2 Запустим Loki
![13](https://github.com/user-attachments/assets/48eab01d-290e-4354-bf1d-8d3b6454618f)

3.3 Отредактируем promtail-config на клиенте
![14](https://github.com/user-attachments/assets/4fca2571-37d3-495d-99fe-6ac05dae7f01)

3.4 Отредактируем docker compose файл для promtail
![15](https://github.com/user-attachments/assets/121789ff-601e-4af2-b0a0-1896d2a46fbc)

3.5 Запустим promtail на клиенте
![16](https://github.com/user-attachments/assets/26614af3-a02b-4192-9527-f25b4d4b2f5a)

3.6 Просмотрим логи клиента в Grafana
![17](https://github.com/user-attachments/assets/a4979d55-5cb3-4dfa-b7d6-9c60d159a1d8)
![18](https://github.com/user-attachments/assets/390cc88f-4801-468d-a4a9-537f25a268f9)

4. Установим и настроим получение логов на сервере с использованием Signoz

Установка Signoz по инструкции с сайта: https://signoz.io/docs/install/docker/#install-signoz-using-docker-compose

4.1 Запустим Signoz
![19](https://github.com/user-attachments/assets/785dabad-076e-4ba3-ba99-e427fec49c6c)
![20](https://github.com/user-attachments/assets/7713db8f-b79a-401f-b756-07b9517be68c)
![21](https://github.com/user-attachments/assets/8a8e5388-e511-46c1-b8c3-944a43918b15)

4.2 Отредактируем конфигурации на клиенте для отправки данных в Signoz

Установка приложения sample-nodejs-app согласно инструкции с сайта: https://github.com/SigNoz/sample-nodejs-app/
![22](https://github.com/user-attachments/assets/e14be99b-0826-47ea-9168-85730e785f70)

4.3 Запустим клиентское приложение sample-nodejs-app
![23](https://github.com/user-attachments/assets/c6e06859-5be8-47cf-a554-1c980dac5cf6)

4.4 Проверим получение логов в Signoz
![24](https://github.com/user-attachments/assets/27702be0-cd1b-46bb-9281-955de2d030c9)
![25](https://github.com/user-attachments/assets/b0daf070-e559-48a2-98a5-0fb5f13383bc)





