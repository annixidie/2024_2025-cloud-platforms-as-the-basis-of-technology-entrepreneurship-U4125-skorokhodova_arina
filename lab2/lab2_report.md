1 шаг. Зайдем в Cloud Run на Google Cloud Platform и нажмем на Deploy.

<img width="688" alt="image" src="https://github.com/user-attachments/assets/a7a8fc99-360c-4913-af5a-8c95aa38ee3b" />

2 шаг. Используем существующий сервис hello и выставим минимальные настройки сервиса. Установим 8080 порт. Дадим доступ неавторизованным пользователям.

![telegram-cloud-photo-size-2-5206196087780668063-y](https://github.com/user-attachments/assets/68a1e3e2-ceb8-40b9-9a97-98ba2cbb72ab)


3 шаг. Проверим, что сервис запущен.

![IMG_8555](https://github.com/user-attachments/assets/d8121182-1fe6-4e9a-b913-657c88b832da)



4 шаг. По ссылке проверим работоспособность сервиса, удостоверяемся, что все сработало.

![telegram-cloud-photo-size-2-5246800983474959792-y](https://github.com/user-attachments/assets/4ac4a727-1564-49a0-b680-65cc503753d3)


5 шаг. Просмотрим текущие Logs и Metrics.

![telegram-cloud-photo-size-2-5246800983474959759-y](https://github.com/user-attachments/assets/62fd0d08-e0ba-4c7b-95d0-7c9656653856)


![telegram-cloud-photo-size-2-5246800983474959780-y](https://github.com/user-attachments/assets/76e7afba-da69-4b3c-8d11-e0a6ea53400c)


6 шаг. Выставим для данного Cloud Run 8090 порт и применим трафик на 50%.

![telegram-cloud-photo-size-2-5246800983474959799-y](https://github.com/user-attachments/assets/b2afb9b4-295e-4954-a719-c5811ad5f85e)

7 шаг. Рассмотрим изменения в метриках и при логах при изменении трафика и порта. 

По логам видно, что контейнер успешно запускается и теперь прослушивает порт 8090 вместо ранее используемого 8080.

После выполнения операции обновления сервиса (ReplaceService) контейнер сообщает о запуске с новым портом.

Количество экземпляров контейнера: во время переключения наблюдалось кратковременное увеличение до двух активных экземпляров.

Загрузка CPU и памяти: показатели остаются стабильными, с минимальной нагрузкой (CPU около 1%, использование памяти — в пределах 10–20%).

Задержка запуска контейнера: зафиксирована незначительная задержка при старте — около 80 мс.

Максимум одновременных запросов: во время переключения обрабатывалось до двух параллельных запросов.

![telegram-cloud-photo-size-2-5246800983474959800-y](https://github.com/user-attachments/assets/bb655f7e-06a4-496e-b5a1-6dab41487481)
![telegram-cloud-photo-size-2-5246800983474959801-y](https://github.com/user-attachments/assets/6535c9cd-599f-4bdf-8890-0c4323f97f17)
![telegram-cloud-photo-size-2-5246897680368659868-y](https://github.com/user-attachments/assets/a6bd3cbd-175b-4b57-97ba-1198bc498a6c)

8 шаг. Удалим Cloud Run.
