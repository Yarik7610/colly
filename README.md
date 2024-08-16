# О проекте

**Колли** - веб-сайт для коллекционеров со всего мира. Создавайте, смотрите, оценивайте, комментируйте. 

# Картинки

![Снимок экрана 2024-08-16 181704](https://github.com/user-attachments/assets/9a630c8d-b749-4219-b6c1-1d01a828972b)
![Снимок экрана 2024-08-16 183418](https://github.com/user-attachments/assets/109ac84e-10e2-4231-822c-3ccbcdeac635)
![Снимок экрана 2024-08-16 183344](https://github.com/user-attachments/assets/a9d35062-cec4-452d-a109-9c5ff711ca18)
![Снимок экрана 2024-08-16 183307](https://github.com/user-attachments/assets/13955866-ad23-4028-990e-dc19208aab87)
![Снимок экрана 2024-08-16 183246](https://github.com/user-attachments/assets/368aa745-aaf4-4634-9453-c5999e7a4dd0)
![Снимок экрана 2024-08-16 182304](https://github.com/user-attachments/assets/6bccbb0e-582f-4ab5-b7e6-c44210e7c2d2)
![Снимок экрана 2024-08-16 181933](https://github.com/user-attachments/assets/aae38df4-0176-456d-b9c9-eaeb7d1ce0b8)
![Снимок экрана 2024-08-16 181738](https://github.com/user-attachments/assets/8a08f413-2c70-4bbd-91f6-70387bad6ec8)


# Функционал
1. Регистрация, авторизация с подтверждением почты с помощью специальной ссылки.
2. Смена имени, описания, почты, пароля, аватара, возможность удаления аккаунта в настройках.
3. Просмотр коллекций с пагинацией, фильтрами, сортировкой, тегами и поиском + всё вшивается в URL.
4. Просмотр авторов с пагинацией, фильтрами, сортировкой, и поиском + всё вшивается в URL.
5. Создание коллекции, её обновление, удаление. В создателе и редакторе коллекции есть DragNDrop input для картинок (можно как добавлять перетаскиванием картинок, а можно через нажатие по зоне). Также есть возможность удаления ненужных картинок на стадии перед отправкой формы. 
6. Просмотр страницы автора с его данными, рейтингом и списком коллекций.
7. Просмотр коллекции с её содержимым. Есть возможность оценить коллекцию, а также есть комментарии с пагинацией + страница комментариев вшивается в URL. Рейтинг и комментарии можно удалять, а также изменять. Комментарии можно создавать много раз.

# Стек основных технологий
1. Next.js c TypeScript
2. Tailwind CSS
3. React Hook Form
4. Zod
5. Shadcn
6. Auth.js 
7. Prisma ORM
8. PostgreSQL
9. Resend

# Что нового сделал для себя
1. Поработал с Next.js на практике (Мой первый проект на нём).
2. Закрепил на практике работу с Tailwind CSS (В связке с модульностью React тема).
3. Впервые поработал с Shadcn (По сути неплохо, но иногда слишком громоздко).
4. Впервые поработал с Zod (Тема, но при отправке файлов надо превращать их в FormData, а потом обратно в нужный объект и валидировать его).
5. Впервые поработал с Prisma ORM (В принципе неплохо, но были некоторые ограничения с Auth.js для Microsoft Edge).
6. Впервые поработал с Auth.js (Не зашло, минусы перевешивают достоинства).
7. Впервые вшил данные в URL (Тема).
8. PostgreSQL (Особо ничего не скажу, т.к работал через ORM).
9. Resend (Неплохо, но нет возможности отправки сообщении для верификации почт на разные адреса бесплатно, надо покупать свой домен и подтверждать его, чего я не делал, но в обучающих целях сойдёт).
10. Впервые сделал DragNDrop input для картинок, а также удаление временно выбранных файлов при создании / редактировании коллекции (Тема).
 
# Впечатления
- Next.js и современный React: В принципе, возможность отсылать данные с сервера (говорю про серверные компоненты и server actions преимущественно, т.к. в приложении я роуты не использовал), а не фетчить их через useEffect крутая, но ещё думаю есть немало ограничений, с которыми ты должен идти на компромисс в приложении, однако, об этом можно говорить скорее как о новом подходе в разработке приложения, нежели чем это какая-то ошибка со стороны разрабов. Например, нельзя в клиентских компонентах использовать серверные, но можно их передать как Children и тогда такой вариант пройдет. Однако, если мне нужны будут пропсы от клиента серверу, передать я их не смогу. Тот же redirect на серверной стороне разрешает либо скролл вверх, либо отключение скролла, других опций нет, их если делать, то через useEffect, либо мириться с этим, что я и сделал.
Но всё это не супер критично. Самое непривычное, это то, что это - фуллстак фреймворк, которые держит всё воедино. Раньше я делал бек и фронт раздельно, и как я говорил выше, разрабы React и Next просто воплощают новый подход, возможно, к которому стоит привыкнуть. Скажу, что структура проекта мне не совсем нравится, а бек по сути - это преимущественно папка с server actions, где нет привычных ответов от сервера и json-ов (ну по сути оно есть, просто теперь у нас эти данные получаются по другому немного). Короче. Фреймворк, несмотря на некоторые недочёты, хороший, однако хотелось бы делать раздельно бек и клиент для чистоты и поддержки проекта.
 - Auth.js: Недавно перекочевала в новую версию, отчего как я понимаю, много недочётов и непоняток. Честно говоря, легче было бы сделать свою авторизацию через useClient, axios и interceptors и routes. Начнём с того, что структура проекта для сетапа либры загрязняется (в их доке написано что это соглашения, что можно менять под себя, возможно и так). Следующий минус исходит из стратегии Credentials адаптера - jwt. Первое, что напрягло, что есть у них jwt с токеном и session с токеном. Но поля этих токенов у них захардкодили, отчего ты должен менять структуру своих моделей, чтобы данные подхватились. Об этом они предупреждает в доке, да, я изменил модель, но поле picture не подтягивалось. Сами callback могут быть асинхронными, в либре новой примеров вроде даже таких не было (только в старой), и то, почему-то при асихнронном callback с jwt у меня часто выдавало ошибку с подключением к БД (возможно, была ошибка моя), в конечном счёте я лишь вшил в сессию id пользователя, а уже все данные нужные мне всегда фетчил, где надо. Следующие минусы были связаны с тем, что непонятно, что вообще надо возвращать в middleware в случае ошибки, что также нужно иногда после обработки ошибки прокидывать её наружу, чтобы ошибка приходила, что также надо при использовании метода singIn явно указывать редирект путь, т.к без этого произойдет редирект, но URL не сменится. Так же не совсем была удобная работа с обработкой ошибок для метода authorize, я так и не понял, как делать кастомные ошибки с сообщением кастомным. Ну и также минус в том, что если удалить пользователя из бд напрямую, то останется кука в браузере, из-за чего человек будет авторизован, хотя аккаунта уже не будет существовать. В общем, плохо.
 - Итог: Несмотря на все возникшие трудности с Auth.js и подходом Next.js, приложение получилось, и получилось оно довольно крутым, пока мой лучший проект.  

# Ограничения проекта

1. В случае удаления пользователя из БД вручную, удаляйте также и куки в браузере.
2. Сообщения для верификации почты приходят только на вашу почту, которую вы указали при регистрации в Resend. 
3. В случае удаления файлов-аватаров и файлов-картинок коллекций вручную, удаляйте также и запись из БД в таблицах `users` и `images`. 

# Запуск

1. Склонируйте репозиторий.
2. Установите все зависимости командой `npm install`.
3. Создайте в PostgreSQL свою БД.
4. Создайте в корне проекта файл `.env` и поместите в него ваши значения следующих переменных: `DATABASE_URL` (путь до БД, созданной выше), `AUTH_SECRET` (Команда npx auth в терминале сгенерирует автоматически данную переменную), `EMAIL_SENDER` (Вам нужно зарегистрироваться на сайте Resend, и ваша почта и будет этим значением, на неё будут приходить письма), `RESEND_API_KEY`(Вам нужно зарегистрироваться на сайте Resend, и там взять данное значение), `NEXT_PUBLIC_APP_URL="http://localhost:3000"`.
5. Пропишите команду `npx prisma db seed` для сида бд тегами.
6. Запустите приложение командой `npm run dev`.
