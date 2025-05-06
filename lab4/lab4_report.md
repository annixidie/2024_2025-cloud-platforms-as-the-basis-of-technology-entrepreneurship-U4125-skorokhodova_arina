# Онлайн-секундомер  

В рамках лабораторной работы рассматривается простой веб-сервис «Онлайн-секундомер» с тремя стадиями жизненного цикла:  
	1.	Начальная разработка  
	2.	Тестирование партнерами  
	3.	Продовое (production) решение  

Для каждой стадии:  
	•	Представлена архитектурная схема  
	•	Рассчитана примерная стоимость  
	•	Обоснован выбор сервисов Google Cloud Platform  

## 1. Начальная разработка

__Описание архитектуры:__  
	•	Frontend и backend развёрнуты на Cloud Run  
	•	Статические файлы хранятся в Cloud Storage  
	•	Пользовательские настройки таймера — в Firestore  

<img width="890" alt="image" src="https://github.com/user-attachments/assets/957a22bb-3c48-46df-9258-f69d6c96d8f9" />


__Примерная стоимость (в мес):__   
<img width="279" alt="image" src="https://github.com/user-attachments/assets/dc7f817b-a4f0-4960-b04c-78bacff7ac8c" />


__Обоснование:__  
	•	Cloud Run быстро масштабируется, нет затрат при простое  
	•	Firestore не требует настройки и работает как key-value  
	•	Cloud Storage дешев для хранения статики и логов  

## 2. Тестирование партнерами 

__Описание архитектуры:__  
	•	Запросы проходят через Cloud Load Balancing  
	•	Приложение развёрнуто на Cloud Run  
	•	Статические ресурсы отдаются из Cloud Storage  
	•	Пользовательские данные — в Firestore  
	•	Метрики и логи собираются через Cloud Monitoring  

<img width="795" alt="image" src="https://github.com/user-attachments/assets/5b41a887-dfbd-44da-acab-d16c8e5c8e13" />


__Примерная стоимость (в мес):__  
<img width="285" alt="image" src="https://github.com/user-attachments/assets/1d5ab278-d04d-4288-9248-55195d56cff2" />

__Обоснование:__  
	•	Load Balancer нужен для теста нагрузки и пиков  
	•	Cloud Monitoring отслеживает ошибки и стабильность  
	•	Инфраструктура легко масштабируется  

## 3. Продовое решение

__Описание архитектуры:__  
	•	Запросы идут через Cloud Load Balancing  
	•	Приложение развёрнуто в Google Kubernetes Engine (GKE)  
	•	База данных — Cloud SQL (PostgreSQL)  
	•	Статика в Cloud Storage, кэшируется через Cloud CDN  
	•	Используются Cloud Logging и Cloud Monitoring  

<img width="1225" alt="image" src="https://github.com/user-attachments/assets/03d75507-3ec0-4594-a531-10423c62ad40" />

__Примерная стоимость (в мес):__  
<img width="286" alt="image" src="https://github.com/user-attachments/assets/01d52d03-9dac-43af-886a-ceb751e307a4" />


__Обоснование:__  
	•	GKE обеспечивает отказоустойчивость и масштабируемость  
	•	Cloud SQL надёжнее Firestore при больших объемах и сложных запросах  
	•	Cloud CDN снижает задержки и ускоряет загрузку  
	•	Мониторинг и логирование — обязательны для продакшена  
