University: [ITMO University](https://itmo.ru/ru/)  
Faculty: [FICT](https://fict.itmo.ru)  
Course: [Cloud platforms as the basis of technology entrepreneurship](https://itmo-ict-faculty.github.io/cloud-platforms-as-the-basis-of-technology-entrepreneurship/education/labs/)  
Year: 2024/2025  
Group: U4125  
Author: Strelkova Alisa Sergeevna  
Lab: Lab3 
Date of create: 27.04.2025  
Date of finished: 


## Шаг 1

Заходим в **Cloud Storage** на Google Cloud Console и создаем новый **Bucket**. 
Надо убрать галочку с "Enforce public access prevention", чтобы разрешить публичный доступ к объектам в бакете.
Это важно, если вы хотите, чтобы другие пользователи могли получить доступ к данным в бакете через ссылки.   

<img width="452" alt="шаг 1 баскет" src="https://github.com/user-attachments/assets/0e53052a-4761-4361-82ae-b212e4734805" />


## Шаг 2

Загрузили 3 изображения в бакет через кнопку **Upload**. 
После этого создали папку с именем **alice** и перенесли файлы в неё с помощью опции **Move** в меню файла.  

<img width="452" alt="шаг2" src="https://github.com/user-attachments/assets/0b22e0dc-ab95-4fab-8143-87d6a9bfd0d3" />

## Шаг 3

Заходим в **Bucket** в раздел **Permissions**, нажимаем на **Grant Access**. 
Добавляем **allUsers** с ролью **Storage Object Viewer**, чтобы файлы в бакете были доступны для чтения по ссылке.

<img width="452" alt="шаг3 " src="https://github.com/user-attachments/assets/ed51d169-66b1-448e-8880-80c15455c516" />


## Шаг 4

Убеждаемся что **Bucket** стал **Public**

<img width="452" alt="шаг4" src="https://github.com/user-attachments/assets/d32eb5ad-832d-4a49-b681-ee3f8a087a74" />


## Шаг 5 



