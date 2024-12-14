# PRZ-4
PRZ-4

1. Поднимаем вирутальную машину из заранее заготовленного образа. После запуска виртуальной машины заходим в браузер и видим приветственное окно
![image](https://github.com/user-attachments/assets/aca29113-f43c-4fb4-8f28-4b397ef5d305)
![image](https://github.com/user-attachments/assets/c1d57980-ea9e-41e9-890b-053a5f3bddb8)

3. Используем полученные данные и входим в учетную запись. После входа нас просит выбрать датасет с которым мы будем работать
![image](https://github.com/user-attachments/assets/db69506b-7292-495f-a5d3-b245f7b3d4ed)


4. В системе уже храняться готовые датасеты с которыми мы будем работвть (lab1, lab2, lab3). Загружаем первый датасет и по аналогии делаем с другими практиками по очередно
![image](https://github.com/user-attachments/assets/753ab1d9-ce74-47e2-966f-07925e9ff69a)


5. После загрузки выбираем его и нам открываеться рабочая панель с нашими данными
![image](https://github.com/user-attachments/assets/68fb1ca2-1a87-4475-8eba-aa719406c99f)

6. Начнем анализировать наши данные
5.1) Первая запись: Значение beacon score очень высокое, пользовательскйи агент определлися как Windows 7, за последний день наблюдается большое колличество подключений, отсуствует строка хостинг
![image](https://github.com/user-attachments/assets/4f7858f8-d72c-4c8e-acd6-a9c3c388c6aa)

5.2) Вторая запись: Значение beacon низкое, есть легетимный сертификат, анализ в гугле показал что данная запись принадлежит Windows и считаеться легитимной
![image](https://github.com/user-attachments/assets/680444a6-4c8f-4729-8482-dc21ee4bd7cf)

Третья запись: Значение beacon низкое, принадлежит Wts (Windows tile services)
![image](https://github.com/user-attachments/assets/6b32b4d7-7ccf-4deb-8a8e-7be76d1be3b4)

Четвертая запись: Значение beacon низкое, имеет схожесть со второй записью
![image](https://github.com/user-attachments/assets/b96718be-89c8-4463-8b73-4fe49548b00f)

Пятая запись: Значение beacon низкое, имеет схожесть с предыдущими записями
![image](https://github.com/user-attachments/assets/65c94021-b12f-4a01-b400-a513b6983431)

Шестая запись: Значение beacon низкое, имеет схожест с четвертой записью
![image](https://github.com/user-attachments/assets/85ee0951-82df-481d-aa35-5055e0130642)

Седьмая запись: относится к Windows и имеет низкий показатель beaconscore
![image](https://github.com/user-attachments/assets/677be386-4807-4740-a4ad-f6a1ce7037f0)

После анализа записей сталдо ясно что первая выглядит довольно подозрительно и требует детального анализа, оставшиеся записи относятся к службам виндовс
Видим 2 записи ккаждая из которых имеет продолжительность почти сутки. Проанализируем их через Virustotal
Открыв превую запись видим сразу предупреждение об этом ip адрессе
![image](https://github.com/user-attachments/assets/c74ba2e2-661e-43a9-8be1-ba0ed34d0273)
![image](https://github.com/user-attachments/assets/00026d65-24ae-492d-bb3c-9a8591544994)

Открыв вторую запись видим что данный ip адресс легетимный
Следующим этапом посмотрим логи связанные с данной записью и ip адрессом
![image](https://github.com/user-attachments/assets/42c56d60-da5a-4b65-b31d-7a153b088684)
![image](https://github.com/user-attachments/assets/86801a91-363f-41c1-a18a-18caa3c91d60)

Слудующий этап загружаем второй набор данный. После загрузки система сразу нас предупреждает что возможно C2 через DNS
![image](https://github.com/user-attachments/assets/4cb2f5a5-a509-41d8-989a-56241321c0bb)
После загрузки выбираем его и нам открываеться рабочая панель с нашими данными
![image](https://github.com/user-attachments/assets/6b6a667e-643a-4765-9060-549f697a0277)

Открываем вкладуку DNS для анализа
![image](https://github.com/user-attachments/assets/535a3ab9-f03c-4e5d-b55b-270eb69799d0)
![image](https://github.com/user-attachments/assets/e8465367-3be4-4cce-8bb9-a3cf780ba075)
![image](https://github.com/user-attachments/assets/583439ae-978a-4d55-9bd3-a902940cab9f)
Проведя весь анализи мы получили следующую иформацию: a) Возможно C2 через DNS b) Имя хоста состоит из шестнадцатеричных символов с) Отсуствие отдельных IP адресов


Загружаем третий набор данный. Сразу видим что рейтинг равняется 100
![image](https://github.com/user-attachments/assets/eaeb8792-2ebd-40f3-b855-ae67b5f80c8d)
После загрузки выбираем его и нам открываеться рабочая панель с нашими данными
![image](https://github.com/user-attachments/assets/aefea309-f67e-4c66-b72a-0f891b66e749)
![image](https://github.com/user-attachments/assets/6e07a5c0-a8ee-4c94-a7e7-6d720255fde6)

Переходим в раздел beacons web для анализа
![image](https://github.com/user-attachments/assets/bfc78b5b-5611-4f69-895b-caf4e65dad20)
![image](https://github.com/user-attachments/assets/f3cd1006-41f7-47ae-9dc2-aa550eb2262d)
![image](https://github.com/user-attachments/assets/f1a64799-2301-48e3-8b14-a2be9e532c66)
![image](https://github.com/user-attachments/assets/9a7aca8d-071f-4b05-acd1-2d70bb577db5)
![image](https://github.com/user-attachments/assets/bb200cf7-e27a-4370-8089-718a2a73af4b)
![image](https://github.com/user-attachments/assets/54e0521d-b158-4e08-bc92-d02ffe6a017f)
![image](https://github.com/user-attachments/assets/0633a824-c53c-4dc5-9a65-7f8f765c8232)
![image](https://github.com/user-attachments/assets/192c4ef9-c738-489c-b991-6a0c82ceea58)
![image](https://github.com/user-attachments/assets/2695977f-125e-48e5-a513-205187098d59)

Видим запись с большим значение beacon. Домен хоть и похож на оригинальный скайп новсе-таки он отличается.
Так же как и первой части проверим черех virustotal и видим что данный домент помечен как ненадёжный
Переходим во вкладку длительные подулючения и видим такую же ситуацию как и в первом наборе данных

![image](https://github.com/user-attachments/assets/40720b48-faee-444d-9701-83e5461befa5)
![image](https://github.com/user-attachments/assets/7600c5f3-a128-451e-9e15-7a83328bd6e5)
![image](https://github.com/user-attachments/assets/65bee20e-f1ea-454e-bd74-57ff26a836ee)
![image](https://github.com/user-attachments/assets/c8b2885d-41a9-444c-9aa1-ca7a7ae38522)
![image](https://github.com/user-attachments/assets/2e3fb6c5-5587-4e98-b7ca-208fc1f62f85)
![image](https://github.com/user-attachments/assets/34d6c969-ab44-4859-a7b9-71f2d21c8eca)













