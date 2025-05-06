Шаг 1. В разделе IAM & Admin на вкладке Service Accounts был создан новый сервисный аккаунт.

<img width="910" alt="image" src="https://github.com/user-attachments/assets/a7dc1a53-ee04-4470-b48d-df4d0e19c2e2" />

Шаг 2. При создании указано имя аккаунта в соответствии с шаблоном из лабораторной работы, после чего выполнен переход к следующему этапу.

![telegram-cloud-photo-size-2-5246800983474959702-y](https://github.com/user-attachments/assets/2acd3b19-91b8-47ac-99e3-d4d09f52749d)

Шаг 3. Для аккаунта назначена роль Storage Admin, после чего его создание завершено.

<img width="532" alt="image" src="https://github.com/user-attachments/assets/ebf67007-169c-4860-867e-eefc39e5ee9e" />

Шаг 4. В разделе Compute Engine на вкладке VM instances начато создание новой виртуальной машины.

<img width="809" alt="image" src="https://github.com/user-attachments/assets/3bbcf9ea-5f9b-4e2d-b5ab-74f14a41ce19" />

Шаг 5. Заданы параметры ВМ согласно инструкции. Проверена предполагаемая стоимость — $3.44.

![telegram-cloud-photo-size-2-5246800983474959710-y](https://github.com/user-attachments/assets/54e0ba59-c8a8-4f51-8cc1-c9d1087948d2)

<img width="634" alt="image" src="https://github.com/user-attachments/assets/9f4a0b9d-18b5-424f-b9d7-899f8d571be4" />

<img width="1047" alt="image" src="https://github.com/user-attachments/assets/7b987384-3114-438a-995b-f1728c57d2c4" />

Шаг 6. Выполнено подключение к созданной ВМ через SSH-интерфейс.

![telegram-cloud-photo-size-2-5246800983474959716-y](https://github.com/user-attachments/assets/0c3ed32c-9ed6-42ac-bf80-6eeaa5e81a96)


Шаг 7. В терминале созданы необходимые каталоги и скопированы файлы. После выполнения операций соединение завершено.

<img width="801" alt="image" src="https://github.com/user-attachments/assets/9511d07d-81bf-4606-bae5-e5c067fa0f17" />

Шаг 8. В сервисный аккаунт добавлена дополнительная роль Compute Viewer через раздел IAM & Admin.

<img width="797" alt="image" src="https://github.com/user-attachments/assets/98fb037b-cab1-44a3-bbab-1386b847cc34" />


Шаг 9. Повторное подключение к ВМ через SSH показало ошибку при передаче данных из-за нехватки прав.

![telegram-cloud-photo-size-2-5246800983474959789-y](https://github.com/user-attachments/assets/d5b0eb7d-6ec1-462d-9eaa-3e5bc84c6b8a)

Шаг 10. После завершения работы ВМ и сервисный аккаунт были удалены.
