University: [ITMO University](https://itmo.ru/ru/)  
Faculty: [Факультет технологического менеджмента и инноваций](https://itmo.ru/ru/viewfaculty/87/fakultet_tehnologicheskogo_menedzhmenta_i_innovaciy.htm)  
Course: [Cloud platforms as the basis of technology entrepreneurship](https://itmo-ict-faculty.github.io/cloud-platforms-as-the-basis-of-technology-entrepreneurship/education/labs/)  
Year: 2024/2025  
Group: U4125  
Author: Strelkova Alisa Sergeevna  
Lab: Lab2  
Date of create: 27.04.2025  
Date of finished:   

## Шаг 1

Перешли в раздел **Cloud Run** на Google Cloud Platform.  
На странице отображаются все доступные сервисы.  
Нажали на кнопку **Deploy container** для начала развертывания сервиса.  
<img width="452" alt="Picture 1" src="https://github.com/user-attachments/assets/822b568c-d322-4292-a7cd-bedb4d66a4ea" />

## Шаг 2
Развернули существующий сервис **hello** с минимальными настройками:
Выбрали образ контейнера.
Установили порт **8080** для прослушивания входящих HTTP-запросов.  
<img width="452" alt="Picture 2 шаг" src="https://github.com/user-attachments/assets/2f0d7221-f2da-4468-a0fe-7a2845a481a8" />

Включили опцию **Allow unauthenticated invocations**, чтобы дать доступ всем пользователям без авторизации.

<img width="452" alt="Picture 2" src="https://github.com/user-attachments/assets/87f545c1-433e-4eef-9a47-1c40a5dccd7c" />  


## Шаг 3
Доп настройки:
Память контейнера установлена на **128 MiB**.
Количество процессоров (CPU) выбрано **< 1** (доля виртуального процессора).
Возможность использования GPU отключена. (не активирована поддержка графического процессора)  
<img width="452" alt="Picture 4" src="https://github.com/user-attachments/assets/a9bd3426-983c-4640-8aa8-8391fb909524" />

## Шаг 4  
После создания сервиса проверили его запуск в списке Cloud Run.   
<img width="452" alt="шаг 4" src="https://github.com/user-attachments/assets/512f0701-c577-48bf-a3ef-2c53c94f920d" />

## Шаг 5 

По ссылке проверим работоспособность сервиса, удостоверяемся, что все сработало. 

<img width="452" alt="шаг 5 " src="https://github.com/user-attachments/assets/07ac2be9-d7da-42af-be4b-0c6d062bd802" />

## Шаг 6

Раздел **Logs** и **Metrics** в Cloud Run.  
В **Logs** отображаются все запросы и ошибки, в **Metrics** можно увидеть данные о нагрузке на сервис, использование памяти, CPU и другие ключевые показатели.  
<img width="452" alt="шаг6" src="https://github.com/user-attachments/assets/bd6ea3ae-1c49-4c75-bb48-e165175a5621" />

## Шаг 7

Изменили настройки сервиса в Cloud Run:
Установили **порт 8090** 
Применили распределение трафика 50 на 50. 

<img width="452" alt="шаг7" src="https://github.com/user-attachments/assets/24d4d70d-b993-4093-8cb4-db58fdd19dff" />


## Шаг 8

После изменения порта на **8090** и установки трафика на 50% проверяем изменения в логах и метриках.
В логах видно, что контейнер теперь запускается на порт **8090** вместо **8080**.  
Произошло обновление сервиса (ReplaceService), после чего контейнер начал работу на новом порту.  
<img width="452" alt="шаг8" src="https://github.com/user-attachments/assets/e0a096d9-272a-4b67-98a5-2b7fab2f02b2" />  


В метриках:
- **Container Instance Count**: наблюдался всплеск до двух активных экземпляров во время переключения.
- **CPU/Memory Utilization**: минимальные нагрузки, CPU около 1%, память 10-20%.
- **Container Startup Latency**: задержка старта контейнера около 80 мс.
- **Max Concurrent Requests**: максимум 2 запроса одновременно.

<img width="452" alt="МЕТРИКИ" src="https://github.com/user-attachments/assets/2ce5a297-22e5-4f37-923d-9ab43020362b" />


  ## Шаг 9
  
Удаляем Cloud Run.








  
