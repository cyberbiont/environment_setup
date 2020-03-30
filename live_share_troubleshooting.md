
# Возможные проблемы с Live Share и их Решение

## Установка Live Share

### MacOS: появляется предупреждение "... running outside application directory"

[Решение](https://github.com/MicrosoftDocs/live-share/issues/2408#issuecomment-505640943)
Проще говоря, переместить _Visual Studio Code.app_ сначала на рабочий стол, а уже оттуда - в директорию ~/Applications.

### Ошибка "An update or installation of VS Live Share failed due to a corrupted download"

Симптомы: при установке Live Share во всплывающем окне появляется ошибка "An update or installation of VS Live Share failed due to a corrupted download". Кнопка Live Share не появляется, хотя Live Share отображается в списке установленных расширений.

Иногда проблема появляется на MacOS и в некоторых случаях на Windows.

Больше информации о проблеме: [здесь](https://github.com/MicrosoftDocs/live-share/issues/3124) и [здесь](https://github.com/MicrosoftDocs/live-share/issues/180)

Шаги по решению проблемы:
1. Деинсталлируйте Live Share.
2. Закройте VS Code.
3. Перейдите в папку `C:\Users\<USERNAME>\.vscode\extensions`(Windows) или `~/.vscode/extensions`(MacOS) и удалите папку с именем ms-vsliveshare.vsliveshare-<номер.версии> (если их несколько, удалите все). Если не получается это сделать, проверьте в диспетчере задач, активен ли процесс `vsls-agent.exe`, если да, завершите процесс и снова попробуйте удалить папку.
4. Установите Live Share заново.

Если вдруг не помогло, что еще можно попробовать:
- удалить расширение Live Share Audio (если установлено).
- установить более раннюю версию Live Share. Нажмите на шестеренку в правом нижнем углу плашки расширения в списке расширений и выберите `Install Another Version`. Появится список доступных версий, выберите версию 1.0.1456 и перезагрузите VSCode.
- удалить данные расширений. Зайдите в директорию `~/Library/Application Support/Code/user/globalStorage` (MacOS) или `C:\Users\<USERNAME>\AppData\Roaming\Code\globalStorage`(Windows) и удалите папку `ms-vsliveshare.vsliveshare`. Чтобы на MacOS попасть в этут папку из папки пользователя, нужно включить отображение папки Library в настройках вида папки). Перезагрузить VSCode и установить Live Share заново.
- Почистить кэш. В той же директории Code очистить содержимое папок, имя которых содержит в себе "cache" или "cached". Перезагрузить VSCode и установить Live Share заново.

<!-- 🕮 <cyberbiont> c2202dc8-f900-42b4-8309-bac915805a9a.md -->

### Ошибка SlimCore not found / Electron not found

Результат бага в Live Share Audio, по поводу которого открыто масса issue на [Github](https://github.com/MicrosoftDocs/live-share/issues?q=globalStorage%5C%5Cms-vsliveshare.vsliveshare-audio+is%3Aopen)

Удалите Live Share Audio.

<!-- 🕮 <cyberbiont> 5c1620f7-9e35-4a5a-8e55-72edafbbe579.md -->

### Подключение в Online-режиме

Если не удалется решить проблемы никаким из способов, студент может подключиться к сессии в online-режиме, см.про него в разделе про способ подключения.

## Авторизация

### Не получается авторизироваться через браузер

Иногда возникают проблемы с авторизацией через браузер. Если вы пытаетесь авторизироваться через GitHub и на длительное время зависли на странице "You are being Authorizing...", обратить внимание на надпись внизу "Having trouble? If your browser doesn't redirect you back, click here". Нажмите на ссылку и следуйте инструкциям (нужно будет скопировать код и вставить его в VS Code).

## Возможные проблемы с firewall'ом

<!-- 🕮 <cyberbiont> c6cdc55c-2204-4580-a8f6-fb76cba0e136.md -->
При первом подключении к сессии Защитник Windows может запросить разрешения для Visual Studio Live Share Agent, нужно разрешить ему доступ в частных сетях (эта настройка уже стоит по дефолту в окне, ничего не нужно менять).
При наличии проблем с подключением можно поэкспериментировать с настройками браундмауэра для приложения vsls-agent.exe
