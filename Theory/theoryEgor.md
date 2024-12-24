# Рубежка 1

Выполнил Макаров Егор К3240

## Вопрос 4.  Можно ли в 2020 году назвать датацентр частным облаком? Почему?  


Датацентр можно представить как большой склад с серверами, где хранятся данные и обрабатываются запросы. Это физическое место с конкретным оборудованием.  
Частное облако — это что то похожее, но оно не только хранит и обрабатывает данные, но и предоставляет услуги, как облачные сервисы. Например, это возможность гибко распределять ресурсы (мощности серверов, памяти) между пользователями, автоматизировать процессы и управлять всем через специальное программное обеспечение.  
В 2020 году можно было бы назвать датацентр частным облаком, если бы он работаел именно как облако — то есть, обладаел такими функциями:  
1. Виртуализация - серверы и ресурсы не жестко привязаны к оборудованию, а распределяются программно.  
2. Автоматизация - всё управляется не вручную, а через софт, который помогает быстро запускать новые сервисы.  
3. Закрытость - доступ имеют только сотрудники или определенные пользователи компании — это и делает его частным облаком.  
Но если датацентр просто стоит, как склад с серверами, и не имеет этих облачных функций, то это еще не частное облако.


# Рубежка 2

## Вопрос 6 У вас развернута большая инфраструктура: сотни виртуальных машин, десятки сервисов. Как будете мониторить её состояние? Что делать с логами, отказами, нагрузкой? Пример для любого провайдера

Для мониторинга такой инфраструктуры нужно использовать спец инструменты, которые помогут собирать метрики, анализировать логи и автоматически оповещать о проблемах.  

   Начнем с логов, т к они записывают все события в системе, то для их централизованного анализа используется лог-менеджмент, например  ELK Stack (Elasticsearch, Logstash, Kibana) или инструменты от провайдера, такие как Cloud Logging в Google Cloud.  
Что можно сделать, чтобы все работа четко: 
   - Собирать логи со всех машин и сервисов.  
   - Фильтровать логи по ошибкам, предупреждениям, запросам.  
   - Искать аномалии или ошибки в логах.  

Далее мониторинг метрик, он отслеживает состояние всех компонентов системы: загрузку процессора, использование памяти, сетевой трафик, доступность сервисов. Например, Google Cloud Operations Suite (Stackdriver)
 Что можно сделать:  
   - Настраивать метрики для мониторинга ключевых показателей (CPU, RAM).  
   - Визуализировать метрики в дашбордах для анализа.  
   - Настраивать оповещения - если метрика выходит за пределы нормы, вы получаете уведомление.  
И отказы, можно настроить их отслеживание дабы быстро находить и устранять проблемы. Используются те же инструменты, что и для мониторинга, но с акцентом на создание алерт-системы.  
Что делаем:
   - Настраиваем пороги для срабатывания уведомлений (например, если сервер не отвечает 5 минут).  
   - Автоматизируем действия при отказе: перезапуск сервиса или масштабирование.  


Пример: Система Google Cloud Operations Suite:  
- Мониторинг метрик: отслеживает состояние виртуальных машин, использование ресурсов и доступность сервисов.  
- Логирование: позволяет централизованно собирать и анализировать логи.  
- Оповещения: можно настроить автоматические уведомления при отклонениях от нормы (например, превышение CPU).  
- Автоматизация: поддерживает автоматическое масштабирование или перезапуск сервисов в случае сбоя.