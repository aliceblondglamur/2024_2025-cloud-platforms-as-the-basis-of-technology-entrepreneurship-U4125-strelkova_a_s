University: [ITMO University](https://itmo.ru/ru/)  
Faculty: [Факультет технологического менеджмента и инноваций](https://itmo.ru/ru/viewfaculty/87/fakultet_tehnologicheskogo_menedzhmenta_i_innovaciy.htm)  
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

Убеждаемся что **Bucket** стал **Public**. 

<img width="452" alt="шаг4" src="https://github.com/user-attachments/assets/d32eb5ad-832d-4a49-b681-ee3f8a087a74" />


## Шаг 5 

Заходим в наш **Bucket** и выбираем нужный файл. Нажимаем на имя файла, чтобы открыть его.    

<img width="452" alt="шаг5" src="https://github.com/user-attachments/assets/2298520b-3e9c-4923-821f-a7e029ab61ab" />


## Шаг 6 
Далее копируем **public URL** и проверяем, что файл доступен по ссылке в браузере.  

<img width="452" alt="шаг6" src="https://github.com/user-attachments/assets/1ce44e50-5e92-40cc-b769-2694360a696a" />


## Шаг 7 

По ссылке открылась картинка.   

<img width="451" alt="шаг7" src="https://github.com/user-attachments/assets/a930d4d5-7e2d-429f-937d-88c6d6271acb" />

## Шаг 8 

Удаляем Bucket.  
<img width="452" alt="шаг9" src="https://github.com/user-attachments/assets/84339a12-99c5-4965-b3f2-175bf3f5e664" />




