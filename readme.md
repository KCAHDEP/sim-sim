sim-sim
=======

Простое в развертывании и использовании приложение-анонимайзер (webproxy) для платформы Google Appengine. Для работы достаточно бесплатного аккаунта. 

Попробуйте пример с отключенной авторизацией: [https://sim-sim.appspot.com](https://sim-sim.appspot.com) (может быть временно недоступно из-за исчерпания квот. В этом случае попробуйте зайти после 11:00 МСК).


Развертывание на Google Appengine
---------------------------------

Откройте [https://console.cloud.google.com/projectcreate](https://console.cloud.google.com/projectcreate) . Возможно, перед этим вам будет предложено войти в аккаунт Google.

На странице *New Project* введите название проекта и выберите свободный Project ID. Обратите внимание, в дальнейшем ваше приложение-прокси будет доступно по адресу https://{Ваш_Project_ID}.appspot.com

Нажмите кнопку *Create*. Будет запущен процесс создания нового приложения. Дождитесь появления сообщения о успешном завершении в панели *Notifications* (справа, наверху).

![Notifications](http://images.vfl.ru/ii/1523011443/c77c1b79/21273759.png)

Рядом вы найдете кнопку *Activate Google Cloud Shell*. Нажмите ее.

![Activate Goole Cloud Shell](http://images.vfl.ru/ii/1523011521/427768bf/21273769.png)

В нижней части окна откроется черное окно консоли. Вставьте в нее следующую команду и нажмите ввод.

    git clone https://github.com/stopcenz/sim-sim

Начнется копирование готового проекта в рабочую область. При успешном завершении в конце будет напечатана строка *Unpacking objects: 100% (34/34), done*.

Чтобы начать развертывание приложения на сервере выполните команду

    gcloud app deploy sim-sim/app.yaml --version 1

Будет выведен список доступных площадок. Если вы не знаете что выбрать, можете просто нажать "1" и клавишу ввода. Утилита установит соединение с указанной площадной. Нажмите ввод еще раз чтобы начать развертывание.

После завершения ваше приложение сразу станет доступно по адресу https://{Ваш_Project_ID}.appspot.com


Лицензия
--------

Лицензия [CC0](http://creativecommons.org/publicdomain/zero/1.0/).

Автор передает эту компьютерую программу в общественное достояние путём отказа от всех своих прав по всему миру, включая все связанные и смежные права, которые он имеет по отношению к данной программе, в той степени, в которой 
это допускается законом.

Вы можете копировать, изменять, распространять этот код, даже в коммерческих целях, не спрашивая разрешения.

Автор не даёт никаких гарантий относительно программы и не несет ответственности за все виды использования, в максимально возможной степени, допустимой применяемым правом.

![CC0](https://licensebuttons.net/p/zero/1.0/80x15.png)
