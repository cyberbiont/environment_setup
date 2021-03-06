# Работа с VS Code Live Share - руководство для студентов

## Подготовка к работе:

1.  Установить VScode. Подробные инструкции по установке и настройка VSCode вы найдете [здесь](https://github.com/cyberbiont/environment_setup/blob/master/Environment%20setup.md#%D1%83%D1%81%D1%82%D0%B0%D0%BD%D0%BE%D0%B2%D0%BA%D0%B0-visual-studio-code).

2.  Зарегистрироваться на https://github.com/. В качестве логина укажите свое настоящее имя_фамилию, это сильно упростит преподавателю жизнь и даст возможность более эффективно помогать вам во время занятий. В дальнейшем. если захотите, вы сможете сменить логин после окончания курсов (на Github есть такая возможность).

3.  Установить расширение VSCode Live Share:

    3.1. Открываем менеджер расширений VSCode:

  <img src="http://dl3.joxi.net/drive/2020/03/23/0032/1408/2123136/36/f27c1a9e38.jpg" alt="extensions manager" width="400">

3.2. В ![панели поиска](http://joxi.ru/Rmz4O6etRwvx9A) вводим Live Share и устанавливаем найденный ![плагин](http://joxi.ru/Vm6PewvHjb3nXA).

3.3. В панели поиска вводим "Live Share Extension Pack" и устанавливаем этот плагин:

  <img src="http://dl4.joxi.net/drive/2020/03/23/0032/1408/2123136/36/5aa304bcbb.jpg" alt="live share extension pack" width="400">

3.4. Таким же образом устанавливаем расширение "Live Server".

3.5. После этого перезагружаем VSCode.

Если у вас что-то не получается - внимательно прочитайте [расширенный гайд](https://docs.google.com/document/d/1S3Gfzum6c0f35hWZLXeH6UZpPmTYBCfdbhXx1JIHqq0/edit)

## Подключение к сессии

Преподаватель, начав сессию, публикует ссылку-инвайт в общем канале Slack. Если используется многоразовая ссылка, она будет прикреплена к каналу вашей группы в Slack (Details - Pinned Items в окошке справа).
Студент присоединяется к сессии, пройдя по этой ссылке и на открывшейся странице браузера во всплывающем окне будет предложение открыть ссылку с помощью VS Code, его нужно принять. Это запускает у вас на компьютере новый экземпляр VS Code с сессией.

Далее, если вы еще этого не сделали, авторизируйтесь через Github (нажмите на кнопку `Sign In` во всплывающем окне справа внизу и выберите вариант авторизации через Github). Достаточно авторизироваться один раз, в дальнейшем просто не выходите из аккаунта (в статус-баре должен отображаться ваш логин, это значит, что все хорошо и вы авторизированы).
Если логин не отображается, то при присоединении к сессии VS Code вновь покажет вам всплывающее окно с предложением авторизироваться, выберите `Sign in`.
Быть авторизированным важно, иначе преподаватель не сможет вызвать вас "к доске" (выдать вам права на редактирование) поэтому обращайте на это внимание.

Вы можете свободно гулять между файлами проекта, открывать на своем компьютере те, что вам нужны, и прокручивать их до нужного места в коде - теперь вам не нужно просить “прокрутить код на проекторе”.

Для того, чтобы “вызвать студента к доске”, преподаватель даст ему права редактирования проекта, и студент будет писать в проекте преподавателя, как в своем.

> Если преподаватель выдал вам права на запись, но у вас не получается писать в файле (при попытке редактирования вы продолжаете видеть сообщение 'Cannot edit in read-only editor') - переключитесь на другой документ в проекте, а потом вернитесь в текущий. Возможность писать код появится. Убедиться, что у вас есть права на запись, можно, проверив свой значок в статус-баре. Если вы в read-only, рядом с вашим логином будет написано (Read-Only).

[Более подробно о способах подключения к сессии](https://github.com/cyberbiont/environment_setup/blob/master/live_share_guide.md#%D0%BF%D1%80%D0%B8%D1%81%D0%BE%D0%B5%D0%B4%D0%B8%D0%BD%D0%B5%D0%BD%D0%B8%D0%B5-%D0%BA-%D1%81%D0%B5%D1%81%D1%81%D0%B8%D0%B8)

## Сервер

Во время работы над проектом у вас будет доступ к общему серверу, с помощью которого можно будет просматривать результаты изменений, которые вы вносите, на странице, открытой в вашем браузере.
Чтобы открыть ее, вы можете:

- принять предложение открыть страницу, которое появляется у вас во всплывающем окне при присоединении к сессии;
- если это окно по какой-то причине не появилось, на вкладке Live Share в сайбаре есть пункт Shared Servers, где будет список всех доступных серверов. Клик по имени сервера запускает страницу у вас в браузере.

Обратите внимание, для того, чтобы изменения отобразились на сервере, вам нужно сохранить их (команда Ctrl + S на Windows, Cmd + S на Mac).

### Возможные проблемы и их решения

Если что-то не работает - первым делом перезагрузите VSCode и присоединитесь к сессии заново.
Решения проблем, которые могут возникнуть при установке или авторизации, поищите [здесь](https://github.com/cyberbiont/environment_setup/blob/master/live_share_troubleshooting.md)

## Обратите внимание!

### Если нужно загрузить файл в общий проект

Перетаскивание бинарного файла (например, картинки) в окно VS Code из Windows Explorer не работает (передача таких файлов не поддерживается Live Share и файлы приходят "битыми"). Вам нужно отправить файл через чат, чтобы преподаватель сам переместил его в нужную папку.

### Undo

Во время совместной работы в сессии Live Share, если одновременно с вами код редактирует кто-то еще, **старайтесь не использовать функцию Undo** (Ctrl-Z) . В данный момент эта функция отменяет последнее действие _у всех_ участников сессии. В дальнейшем это [будет исправлено](https://github.com/MicrosoftDocs/live-share/issues/1439), но пока старайтесь не пользоваться Undo без особой необходимости.

<!-- 🕮 <cyberbiont> eab76d57-ee02-4008-873e-2b70a57370df.md -->

## Открытие своего проекта параллельно с Live Share

Обычно на занятии параллельно с Live-share сессией вам нужно будет работать над собственным проектом.
Если для своего проекта вы используете VS Code, его удобно открыть в отдельном окне (новое окно VS Code можно открыть через File - New Window).

<!-- 🕮 <cyberbiont> 4b3e4237-d3f7-4508-b2e8-cb4b5d3b62f7.md -->

Если ваш проект уже открыт, а вам нужно присоединиться к Live Share сессии, то лучше это сделать, открыв инвайт-ссылку в браузере, тогда она запустится в новом окне автоматически.
Если вы сделаете это через команду "Join Collaboration session", сессия заменит ваш открытый проект в текущем окне.

### Peacock

Чтобы легко отличать окна одно от другого, есть расширение Peacock, которое изменяет цвет рамки окна, если вы находитесь в сессии Live Share.

Нажмите F1 и в появившемся меню команд введите `Peacock:Change Live Share` Выберите команды `Peacock: Change Live Share Color(Host)` и `Peacock: Change Live Share Color(Guest)`, и задайте цвет, который будет использоваться, если вы находитесь в активной сессии (Host - вы начали сессию, Guest - присоединились к сессии).

Выбираем команду "Peacock: Change Live Share Color(Host)"

<img src="http://i.piccy.info/i9/6ee6900531b00032d1965276f8810ca4/1585163673/41514/1369367/Clipboard_20200325_01.png" alt="peacock" width="400">

Затем

<img src="http://i.piccy.info/i9/783de8c135259ea16dcafe25ee074bc0/1585163790/59444/1369367/Clipboard_20200325_02.jpg" alt="peacock colors" width="400">

Список цветов можно редактировать в настройках плагина.

## Если код, который вы написали, не работает

Сравните ваш код с кодом, который написал преподаватель/студент, с помощью инструмента Compare.

Для этого, оба файла должны быть открыты у вас в одном окне VS Code.
Если ваш проект открыт в отдельном окне, откройте интересующий вас файл в окне Live Share и перетащите вкладку с ним в окно с вашим проектом.

Затем, чтобы сравнить файлы, на вкладке Explorer в сайдбаре нажмите на интересующие вас файлы правой кнопкой мыши и выберите сначала `Select for Compare`, а затем `Compare With Saved` для второго файла (если вы перетащили вкладку из другого окна, ищите ее вверху в "open editors").

Как это работает: вы нажимаете правую кнопку мыши на вашей файле, и выбираете пункт `Select to Compare`.

<img src="http://dl3.joxi.net/drive/2020/03/23/0032/1408/2123136/36/c9e7f0df93.jpg" alt="select to compare" width="400">

После чего нажимаете на файл, написанный на компьютере преподавателя, правой кнопкой мыши и выбираете пункт `Compare with Selected.`

<img src="http://dl4.joxi.net/drive/2020/03/23/0032/1408/2123136/36/e8eddb543c.jpg" alt="compare with selected" width="400">

Также вы можете посмотреть [видео-инструкцию](https://www.youtube.com/watch?v=atMu5lZ5RzU)

Если вы писали код, сильно отличающийся от того, что писал преподаватель/другой студент, то по окончании решения задачи скидывайте свой код в личные сообщения преподавателю в чат GoToWebinar, например с помощью сервиса https://codeshare.io/

<!-- 🕮 <cyberbiont> 6df82a4b-8a46-4e72-9b55-ffa61adea70e.md -->

## Консультация с преподавателем

Преподаватель может попросить вас выполнить следующие шаги, чтобы иметь возможность проконсультировать Вас по вашему коду через LiveShare:

1. Вам нужно будет запустить локальный сервер.

  <!-- 🕮 <cyberbiont> 36f60747-539a-4939-a73d-0c44d0d44862.md -->

Если у вас установлено расширение LiveServer, в статус-баре (внизу справа) у вас должна быть кнопка GoLive.
Нажмите ее и у вас автоматически откроется вкладка в браузере с превью вашего проекта (по дефолту на порту 5500).

2. Вы должны будете создать свою сессию.
   Чтобы это сделать, нажмите на кнопку LiveShare в статус-баре, ссылка автоматически будет скопирована в буфер обмена, отправьте ее преподавателю. (Более подробно см. [Запуск сессии](#Запуск-сессии)).

> В некоторых случаях сервер может не расшариться автоматически, тогда вам придется сделать это вручную. Вы можете проверить, доступен ли ваш сервер, в разделе Shared Servers. Если нет (список пуст), используйте команду ShareServer, чтобы расшарить его вручную.

![Share Server](http://i.piccy.info/i9/f1f69998b11c76f69c1ef387c4df97f0/1585164955/33587/1369367/Clipboard_20200325_04.jpg)

> В открывшемся окне вам нужно ввести номер порта, на котором работает сервер, после этого он появится в списке в разделе Session Details на вкладке Live Share в сайдбаре.
> Более подробно, см. [здесь](#Расшаривание-сервера)

3. Иногда преподавателю также может понадобиться доступ к вашему терминалу. См. [Расшаривание терминала](#Расшаривание-терминала)
