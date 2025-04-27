University: [ITMO University](https://itmo.ru/ru/)  
Faculty: [Факультет технологического менеджмента и инноваций](https://itmo.ru/ru/viewfaculty/87/fakultet_tehnologicheskogo_menedzhmenta_i_innovaciy.htm)  
Course: [Cloud platforms as the basis of technology entrepreneurship](https://itmo-ict-faculty.github.io/cloud-platforms-as-the-basis-of-technology-entrepreneurship/education/labs/)  
Year: 2024/2025  
Group: U4125  
Author: Strelkova Alisa Sergeevna  
Lab: Lab1  
Date of create: 27.04.2025  
Date of finished: 

## Шаг 1 
В разделе IAM & Admin на вкладке Service Accounts создан новый сервисный аккаунт.  
<img width="452" alt="Picture 1" src="https://github.com/user-attachments/assets/f315f157-3ef6-4f71-a321-df9591fa0ef7" />
## Шаг 2
При создании задано название сервисного аккаунта **astrelkova-sa-lab1** в соответствии с маской, указанной в лабораторной работе. После этого выполнен переход к следующему этапу.  
<img width="452" alt="Picture 2" src="https://github.com/user-attachments/assets/6af78726-e613-4839-83c3-44c4fb8b36fd" />
## Шаг 3
Для созданного сервисного аккаунта была назначена роль **Storage Admin**, которая предоставляет полный доступ к управлению объектами в хранилище.  
<img width="452" alt="Picture 3" src="https://github.com/user-attachments/assets/9a930b3f-8624-483b-b412-e86e098bc811" />
## Шаг 4
Переходим в раздел **Compute Engine** в консоли Google Cloud.  
На вкладке **VM instances** нажимаем кнопку **Create instance** для создания новой виртуальной машины.
<img width="452" alt="Picture 4" src="https://github.com/user-attachments/assets/fa2b8ac7-f72f-4d83-bd9f-cae3fc3d40e3" />
### Шаг 5
Настроена виртуальная машина в разделе **Compute Engine**.
Выбран тип машины **e2-micro** с 1 виртуальным CPU и 1 GB оперативной памяти в регионе **us-central1 (Iowa)**.
Также был включён режим **Spot instance** для снижения стоимости использования.  
**При создании виртуальной машины надо выбрать именно свой сервисный аккаунт.**  
 **Итоговая стоимость виртуальной машины составляет $3.44 в месяц** согласно расчётам в консоли Google Cloud.
<img width="452" alt="Picture 5" src="https://github.com/user-attachments/assets/1c4e38f5-37d5-4d90-b37a-cf5d73ffe584" />  
<img width="452" alt="Picture 6" src="https://github.com/user-attachments/assets/4de5d456-8817-4ef7-b441-35a764a5b865" />  
<img width="452" alt="Picture 8" src="https://github.com/user-attachments/assets/a50cbeca-c118-4c4f-b523-5509ebd10007" />  
<img width="452" alt="Picture 7" src="https://github.com/user-attachments/assets/2ac33249-5992-4edb-aab8-fb9f8660b575" />  
## Шаг 6
После успешного создания виртуальной машины выполнено подключение к ней через веб-интерфейс консоли Google Cloud.
Для подключения использована функция **SSH**, встроенная в раздел **VM Instances**.
Если подключение прошло успешно то открывается терминал для работы с командной строкой на виртуальной машине.  
<img width="452" alt="Picture 9" src="https://github.com/user-attachments/assets/a232c276-41c5-465a-8bfd-5ebc52db8563" />
## Шаг 7
В окне подключения через SSH выполнены команды для создания новой папки и копирования в неё необходимых файлов из бакета `lab1-bucket-itmo`. Все выполнено без ошибок. 
После выполнения операций SSH-сессия была завершена.  
<img width="452" alt="Picture 10" src="https://github.com/user-attachments/assets/41b44873-090c-499c-8799-3145845aa15c" />
## Шаг 8
В разделе **IAM & Admin** на вкладке **Service Accounts** для созданного сервисного аккаунта добавлена роль **Compute Viewer**.
## Шаг 9
Повторно выполнено подключение к виртуальной машине через SSH.  
При попытке скопировать файлы из бакета возникла ошибка **AccessDeniedException 403** — нет прав на доступ к объектам в Storage,
потому что у сервисного аккаунта роль ограничена до **Compute Viewer**.   
<img width="452" alt="Picture 11" src="https://github.com/user-attachments/assets/5813787f-c52e-4546-beeb-e18de85691d7" />
## Шаг 10
Удалены все созданные ресурсы:
- Виртуальная машина через раздел Compute Engine.
- Сервисный аккаунт через раздел IAM & Admin → Service Accounts.
<img width="320" alt="Picture 12" src="https://github.com/user-attachments/assets/68badd74-f6e3-4b63-84fd-ca1a3e1e20b2" />



