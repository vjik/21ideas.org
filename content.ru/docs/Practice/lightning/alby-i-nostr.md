---
title: "Alby и Nostr"
h1: "Браузерное расширение Alby: оптимизируйте свое взаимодействие с интернетом"
cover: /img/alb-363.png
description: "Cегодня я бы хотел поделиться с вами гидом по двум очень интересным и полезным приложениям. Это универсальное браузерное расширение Alby и клиент для взаимодействия с протоколом Nostr под названием Nostrgram."
url: alby-i-nostr
date: 2023-02-17
bookFlatSection: false
bookToc: true
weight: 3
---

{{< hint btc >}}
Гид подготовлен [Тони⚡️](https://snort.social/p/npub10awzknjg5r5lajnr53438ndcyjylgqsrnrtq5grs495v42qc6awsj45ys7). 

[Поддержать проект](/contribute).
{{< /hint >}}

## Интро

Cегодня я бы хотел поделиться с вами гидом по двум очень интересным и полезным приложениям. Это универсальное браузерное расширение [Alby](https://getalby.com/) и клиент для взаимодействия с протоколом Nostr под названием [Nostrgram](https://nostrgram.co/). Почему именно эти два и почему в одном гиде? Потому что они отлично друг друга дополняют и призваны работать в связке. Начнем с Alby.

{{< hint btc >}}
Отличным дополнением к этому материалу станет подготовленный нами исчерпывающий ресурс по протоколу Nostr: [https://nostr.21ideas.org/](https://nostr.21ideas.org/)
{{< /hint >}}

## Зачем мне Alby?

Благодаря Alby мы теперь можем взаимодействовать с Биткоином наиболее простым и удобным способом. Это стало возможно благодаря сети Молния – решению второго уровня, расположившемуся поверх основной сети Биткоин. Многие уже осознали тот факт, что Биткоин является новой, революционной формой интернет-денег, но все еще считают его либо неудобным, либо слишком дорогим в использовании. Именно эти проблемы решает протокол второго уровня (⚡️Лайтнинг) и построенные поверх него приложения (🐝Alby).

{{% image "/img/alb-364.png" /%}}

Alby предлагает множество функций – от простой отправки и получения сат до лайтнинг-адресов, установки отдельных бюджетов на траты на каждом сайте и хранения учетных записей Nostr, – и я попробую вкратце описать и показать каждую из них.

## Установка приложения

Как я уже сказал, основным продуктом Alby является одноименное браузерное расширение. Благодаря этому сама установка аналогична установке любого другого расширения для браузеров Crome или Firefox.

{{% image "/img/alb-365.png" /%}}

Необычным и при этом очень полезным для некоторых дополнением к этому является поддержка Alby браузера [Tor](https://blog.getalby.com/access-your-private-lightning-node/). Эта связка позволяет значительно повысить уровень приватности пользователя. Расширение для Tor устанавливается так же, как и в случае с Firefox.

Как и в случае любых других кошельков, лучшим подходом к скачиванию является переход на официальный сайт проекта [https://blog.getalby.com/](https://blog.getalby.com/). Далее устанавливаем расширение привычным  способом.

{{% image "/img/alb-366.png" /%}}

После добавления расширения в браузер нас встретит окошко создания профиля.

{{% image "/img/alb-367.png" /%}}

### Регистрация для новичков

Самым простым и дружелюбным к новичкам способом будет создание нового аккаунта через сам сервис Alby. Для этого нажимаем подсвеченную оранжевым кнопку **Sign Up**.

{{% image "/img/alb-368.png" /%}}

Далее все аналогично любой другой регистрации, за исключением дополнительного поля **Lightning Address**. Подробнее об ЛН-адресах я писал в этом посте, но в двух словах это один из наиболее простых и удобных способов отправлять и получать лайтнинг-платежи. Так что выбираем ник, вводим его и нажимаем **Continue**.

Ваш аккаунт создан! Теперь вы можете обмениваться сатами прямо из браузера, а также вставлять свой лайтнинг-адрес в описание своих аккаунтов в социальных сетях, чтобы ваши подписчики могли с легкостью отправлять вам саты. Единственное, что нужно сделать – это добавить эмоджи ⚡️ перед ЛН-адресом, чтобы его не спутали с обыкновенной электронной почтой. Мой лайтнинг-адрес, например, выглядит так: ⚡️21ideas@getalby.com. Не постесняйтесь отправить немного сат, если этот гид или любой другой мой труд оказался вам полезен.

Лайтнинг-адреса также поддерживаются множеством кошельков, например, Wallet of Satoshi.

{{% image "/img/alb-369.png" /%}}

Я не буду подробно пояснять все мельчайшие детали установки и использования приложения, такие как пункты меню, отправка и получение сат и т. п. Если вам нужны такие подробности, они доступны в гиде моего друга-энтузиаста Blind Dev, доступном [по этой ссылке](https://teletype.in/@blind_dev/Obzor-Lightning-koshelka-09-21).

### Регистрация для биткоин-гангстеров

{{% image "/img/alb-370.png" /%}}

Более опытным биткоинерам и пользователям сети Молния будут интересны другие варианты подключения аккаунта Alby, предоставляющие лучшую гибкость использования и возможность самостоятельно хранить свои ЛН-сатошики. Здесь вы можете подключить сервис к уже используемому вами кошельку или собственному лайтнинг-узлу.

В этих случаях привязка устройства также не обременит пользователя. При добавлении кошелька приложение просто попросит вас либо сгенерировать QR-код своим кошельком и отсканировать его вебкамерой расширения Alby, либо вставить данные, генерируемые при экспорте нового кошелька.

{{% image "/img/alb-371.png" /%}}

Держателям полных узлов также нужно будет лишь скопировать необходимую информацию в соответствующее поле в Alby. Не думаю, что этот процесс требует детального разбора, более того, Alby предоставляет видеогиды подключения собственных узлов.

<center><video src="/img/alb-382.mp4" controls style="width: 100%"></video></center>

{{< hint btc >}}
Обратите внимание, что Alby поддерживает создание нескольких аккаунтов – вы вольны создать любое их количество.
{{< /hint >}}

## Возможности Alby

### ЛН-адреса

Вы можете вставлять ЛН-адрес во все свои социальные сети – 🪦Twitter , ⚡️Nostr, 👽Reddit, 🎥YouTube, 📺BitcoinTV, 👾GitHub, на собственный 🌐веб сайт... По сути, возможности безграничны: на любой страничке, где вы вставите свой лайтнинг-адрес в формате ⚡️21ideas@getalby.com, расширение посещающего страничку пользователя подсветится синим цветом, оповещая его, что хозяину странички можно отправить несколько сат.

{{% image "/img/alb-372.png" /%}}

### Бюджеты

Удобной функцией Alby является возможность устанавливать бюджет для каждого отдельного сайта или приложения.

<center><video src="/img/alb-383.mp4" controls style="width: 100%"></video></center>

Во вкладке **Websites** раздела ⚙️**Settings** вы можете видеть все сайты, с которыми вы когда-либо взаимодействовали через расширение Alby. Здесь же вы можете нажать на интересующий вас сайт, кликнуть по значку ⚙️ и установить месячный бюджет, который вы готовы потратить на этом сайте. Тут же можно разрешить приложению логиниться на сайтах, поддерживающих функцию “Логин через лайтнинг” (подробнее о ней в [этом посте](https://t.me/bitcoin21ideas/2483)). Эти возможности сберегают немало времени – приложение запоминает ваше решение и не переспрашивает вас каждый раз при логине или отправке средств. Это может показаться незначительным, ведь _“что такое две секунды, которые требуются, чтобы подтвердить действие”_, но пример браузера Brave, блокирующего рекламу и выигрывающего за счет этого пару миллисекунд при открытии страниц, указывает, что каждая секунда играет роль:

{{% image "/img/alb-373.png" %}}
_Эти результаты достигнуты за несколько лет, но пример от этого не перестает быть показательным_
{{% /image %}}

Особенно важной эта функция становится с взрывным ростом нового протокола Nostr (подробнее о нем – на страничке [nostr.21ideas.org](https://nostr.21ideas.org/)), который позволил разработчикам внедрить так называемые ⚡️Запы (⚡️Zaps) – “лайки 2.0", посредством которых вы можете отправлять пару сат с каждым запом понравившегося поста в соцсети. Невероятно, да? Как раз об этом я и расскажу подробнее 🤙. Мы также обсуждали эту и другие возможности Ностр на недавнем [стриме](https://t.me/bitcoin21ideas/2645).

<center><video src="/img/alb-384.mp4" controls style="width: 100%"></video></center>

## Alby + Nostr

Nostr – не самый простой концепт для понимания, но в двух словах, это революционный протокол, который обеспечивает возможность передавать информацию устойчивым к цензуре способом (я все же настоятельно советую изучить страничку [nostr.21ideas.org](https://nostr.21ideas.org/)). Его нельзя запретить или остановить, а отправленные в децентрализованную сеть данные нельзя ни удалить, ни заглушить.

{{% image "/img/alb-374.png" /%}}

Логично, что в первую очередь этот протокол взяли в обиход разработчики, создающие приложения для социального взаимодействия, но на протоколе также строят [игры](https://jesterui.github.io/) и [другие](https://sendstr.com/) [приложения](https://nosbin.com/).

## Особенности учетных записей Nostr

Чтобы создать “учетную запись” Nostr, вам нужно сгенерировать пару ключей – приватный и публичный. Приватный ключ является аналогом пароля в традиционных соцсетях, а публичный представляет собой что-то вроде логина и имени пользователя, по которому любой другой участник сети может вас найти. Разумеется, важно ответственно отнестись к хранению этих ключей, ведь каждый, кто получит к ним доступ, сможет просматривать всю опубликованную вами информацию, включая личные сообщения, и постить от вашего имени.

На базе протокола Nostr уже построено огромное количество клиентов (приложений), и чтобы зайти в них, необходимо использовать один из вышеупомянутых ключей. Подробнее об этой особенности можно узнать из моего поста в Nostr – вы сможете с ним ознакомиться, когда разберетесь в основах создания аккаунта благодаря этому гиду.

{{% image "/img/alb-375.png" %}}
ID заметки: `@note1rupes6t0439felc29ycuq75nfqc0v3yny0gvpvgmqta6ppsh8v5q4sertm`
{{% /image %}}

Суть заключается в том, что просто вставлять свой публичный ключ в разные клиенты небезопасно. Здесь на помощь и приходит расширение Alby, которое способно управлять вашей связкой ключей. Alby поможет вам сгенерировать или сохранить ранее сгенерированный вами приватный ключ Nostr. С Alby ваши ключи никогда не покидают вашего устройства – расширение хранит ваш приватный ключ и подписывает все необходимые действия (постинг, лайки, запы…). Управление ключами Nostr производится из настроек приложения в разделе “Учетные записи” (**Accounts**).

<center><video src="/img/alb-385.mp4" controls style="width: 100%"></video></center>

Если вы хотите завести (или уже завели) несколько аккаунтов в Nostr, вы можете создать аналогичное количество аккаунтов в Alby и таким образом хранить ключи от каждой учетной записи.

Несмотря на то, что расширение Alby не давало повода усомниться в своей надежности, я настоятельно рекомендую сохранить свой приватный ключ в дополнительном месте. Это может быть менеджер паролей или даже листок бумаги, который вы знаете, что не выбросите. Главное – осознавать значимость бэкапа и хранить его соответствующе.

{{% image "/img/alb-376.png" /%}}

## Использование Nostr

Существует огромное количество клиентов Nostr как для мобильных устройств, так и для браузеров. В этом гиде я познакомлю вас с основами взаимодействия с этим протоколом на примере своего любимого веб-приложения [Nostrgram](https://nostrgram.co/). На то есть несколько причин:

- Будучи веб-приложением Nostrgram потребует от вас минимум усилий для запуска – просто перейдите по [ссылке](https://nostrgram.co/) для запуска веб-странички;
- В случае использования мобильного приложения вам придется предоставлять ему приватный ключ или генерировать его там, а позже разбираться с переносом его в Alby, поэтому я бы все же начал знакомство с Nostr с веб-версии (вы вольны выбрать любое другое веб- или мобильное приложение; альтернативы можно найти на [nostr.21ideas.org](https://nostr.21ideas.org/));
- Nostrgram предлагает огромное количество самых разных функций (подробнее о них чуть позже), но главное – встроенный переводчик на русский, украинский и целый ряд популярных языков. Nostr, как и базирующиеся на нем приложения, очень молод и далеко не все разработчики успели внедрить все желаемые функции;
- Разработчик Nostrgram, Джон Леджер (публичный ключ: `npub1t9a59hjk48svr8hz6rx727ta6kx53n5d6fw8x26vsua0zytpl87sa6h4uw`), очень активен в соцсети и буквально каждый день сообщает о разного рода нововведениях и улучшениях.

Мне очень понравился его подход к развитию клиента и я связался с ним, предложив перевести пользовательский интерфейс Nostrgram на русский. Рад сообщить, что довольно скоро первый Nostr-клиент получит полную поддержку русского языка. Эта новость может звучать довольно посредственно, но дело в том, что это будет первый веб-клиент, предлагающий опцию выбора языка. Я также нахожусь в процессе перевода на русский приложения для iOS [Damus](https://damus.io/).

## Регистрируемся в Nostrgram

Переходим по ссылке [nostrgram.co](http://nostrgram.co/) в браузере, на котором установлено расширение Alby и нажимаем на 🔑ключик в левом верхнем углу экрана. По словам разработчика Nostrgram лучше всего работает с браузерами на основе Chromium, такими как Google Chrome и Opera, но Brave в силу своих нетривиальных настроек “ломает” некоторые функции веб-клиента, например, столь важный многим встроенный перевод постов.

Для взаимодействия с Nostrgram я использую Firefox и не заметил никаких ошибок, а Джон подтвердил, что взаимодействие клиента с Firefox не вызывало у него никаких нареканий. В будущем проблемы с Brave также будут устранены.

Итак, при первом запуске Nostrgram попросит вас ввести ключ авторизации...

{{% image "/img/alb-377.png" /%}}

{{< hint btc >}}
Следующий абзац представляет собой технические подробности процесса авторизации клиентов Nostr через расширение Alby. Для понимания этого процесса нужны базовые знания функционирования связок публичный-приватный ключ. Если вы не знакомы с этой темой, вы можете либо узнать подробности [здесь](https://ru.wikipedia.org/wiki/%D0%9A%D1%80%D0%B8%D0%BF%D1%82%D0%BE%D1%81%D0%B8%D1%81%D1%82%D0%B5%D0%BC%D0%B0_%D1%81_%D0%BE%D1%82%D0%BA%D1%80%D1%8B%D1%82%D1%8B%D0%BC_%D0%BA%D0%BB%D1%8E%D1%87%D0%BE%D0%BC), либо окинуть абзац беглым взглядом и продолжить ознакомление с гидом.
{{< /hint >}}

Особенность использования Nostr-приложений в связке с Alby заключается в том, что ваши приватные ключи не передаются клиенту (приложению), то есть, грубо говоря, “не транслируются в интернет”. Таким образом, вам не приходится доверять клиенту: даже если его взломают и все хранящиеся на нем данные утекут, ваш приватный ключ останется в безопасности, а значит злоумышленники не смогут получить доступ к вашим персональным данным, таким как личная переписка. Вы авторизуетесь с помощью публичного ключа, который предоставляет вам доступ “наблюдателя”, а каждый раз, когда вы хотите опубликовать пост, открыть личное сообщение или выполнить другое активное действие, например отправить Зап⚡️, клиент обращается к Alby, прося расширение авторизовать действие (то есть, подписать сообщение вашим приватным ключом). Alby в свою очередь спрашивает вашего разрешения авторизовать это действие. Разумеется, это нельзя назвать эффективным подходом, поэтому Alby дает возможность автоматизировать этот процесс.

{{< hint btc >}}
Когда расширение в следующий раз попросит вашего одобрения действия, стоит поставить галочку в поле “Запомнить мой выбор и больше не спрашивать” (**Remember my choice and don’t ask again**).
{{< /hint >}}

{{% image "/img/alb-378.png" /%}}

Готово! Мы авторизовались в клиенте Nostrgram и теперь можем полноценно использовать протокол Nostr – публиковать посты, пересылать сатошики другим пользователям в один клик, обмениваться зашифрованными сообщениями… Таким же образом вы сможете залогиниться в любой другой клиент Nostr, а если вы захотите использовать веб-клиент на мобильном телефоне, это можно сделать на Android в браузере Kiwi и в браузере Orion на iOS. Но и это еще не все: вы также сможете использовать ваш приватный ключ для авторизации в других приложениях на основе Nostr, например, в вышеупомянутых шахматах [Jestr](https://jesterui.github.io/).

На этом этапе было бы логично осветить процесс настройки профиля Nostrgram, но эта информация уже есть в нашем [гиде](https://nostr.21ideas.org/), поэтому, если у вас возникнут какие-то вопросы, вы всегда можете к нему обратиться. Лишь подчеркну, что в настройках профиля клиентов Nostr есть поле **Lightning Address**, куда вы можете вставить [ЛН-адрес](https://t.me/bitcoin21ideas/2485), ранее предоставленный Alby, чтобы другие пользователи могли с легкость отправить вам немного сат, не покидая собственного клиента (не выходя из приложения). Как только вы заполните это поле возле вашего аватара появится значок ⚡️, нажав на который можно будет перечислить вам средства.

## Функции Nostrgram

Как я уже говорил, Nostrgram предоставляет, пожалуй, самый широкий ассортимент функций из всех известных мне клиентов Nostr. Давайте подробнее остановимся на некоторых из них.

**1. Перевод постов**

Привычная функция для пользователей традиционных соцсетей пока что доступна не во всех клиентах. Nostrgram предоставляет такую возможность. Все что нужно сделать – выбрать желаемый язык в настройках (значок ⚙️ в правом верхнем углу экрана) и сохранить настройки (нажимаем 🆗). Теперь при нажатии иконки перевода, отображаемой в правом верхнем углу каждого поста, вы будете видеть текст на выбранном вами языке. 🗣️ Эта функция работает в обе стороны: носители других языков теперь способны понимать ваши посты на незнакомом им языке и вы можете беседовать, преодолевая языковые барьеры.

**2. Возможность отправлять саты вместо лайков (Запы/Zaps)**

Лайки – пустое место. Их легко подделать, невозможно переиспользовать и легко потерять. Поэтому разработчики Nostr внедряют в свои приложения ⚡️Запы. Вместо того, чтобы ставить бесполезный лайк вы теперь можете поддержать полезный или повеселивший вас пост самыми твердыми деньгами, просто отправив пару сат его автору в один клик. Nostrgram стал одним из первых клиентов, внедривший поддержку ⚡️Запов. Покажу-ка я видео, уже выложенное выше, еще раз – уж очень оно мне нравится 🤗

<center><video src="/img/alb-384.mp4" controls style="width: 100%"></video></center>

Будьте осторожны: Запы завлекают, и опустошить свой лайтнинг-адрес не составит большого труда 😅. Именно для таких случаев пригодится возможность Alby устанавливать бюджет для каждого сайта. Мало того, что вы теперь получите оповещение по достижению указанной суммы, вы еще и сможете легко отслеживать суммы, уже потраченные в течение месяца на разных используемых вами сервисах.

{{% image "/img/alb-379.png" /%}}

**3. Гибкие настройки интерфейса**

Nostrgram позволяет настроить внешний вид клиента именно так, как вам нравится. Хотите отображение контента в один столбец, наподобие Twitter? Пожалуйста! Хотите несколько столбцов? Не проблема! Можно даже отображать только посты, содержащие медиа, как в Instagram или Pinterest. Переключатель находится в центре верхней части страницы.

{{% image "/img/alb-380.png" /%}}

В настройках клиента вы также можете выбрать разные акцентирующие цвета, выделяющие посты тех, на кого вы подписаны, ваших подписчиков и т. д.

**4. Разные источники информации**

Вы можете просматривать посты как исключительно от пользователей, на которых вы подписались (**Following**), так и тех, на кого подписаны ваши подписки (**Friends+**). Переключатель находится в верхнем левом углу экрана.

Вы также можете просматривать глобальную ленту, которая агрегирует посты со всего мира. Отличный способ завести 🌎новые 🌍международные 🌏знакомства (кто знает, возможно, в будущем и 🪐межпланетные). Но у глобальной ленты есть и свои минусы…

**Острожно, спам!**

В силу того, что Nostr является цензуроустойчивым протоколом, он моментально привлек внимание спамеров, скамеров и разного рода жуликов.

{{% image "/img/alb-381.png" /%}}

Коммуникации в Nostr производятся посредством обмена сообщениями между так называемыми релеями (подробности смотрите на [nostr.21ideas.org](http://nostr.21ideas.org/)). Поэтому то, какие посты вы будете видеть зависит от того, к каким релеям (ретрансляторам) вы подключились. Это довольно комплексная тема и подробнее о ней можно узнать, из нашего гида (см. выше), либо подписавшись на меня в Nostr, где я регулярно поясняю подобные базовые особенности протокола (и, конечно, делюсь мемасиками и разного рода полезным и развлекательным контентом).

Мой публичный ключ: `npub10awzknjg5r5lajnr53438ndcyjylgqsrnrtq5grs495v42qc6awsj45ys7`

**5. Борьба со спамом**

Nostrgram посвящает много времени и сил тому, чтобы решить эту проблему. Я не буду вдаваться в подробности, но скажу, что учитывая то, насколько эта задача сложна, клиенту это удается на ура. Если вы и увидите какие-то нерелевантные сообщения в глобальной ленте, то довольно редко.

**6. Сохранение истории сообщений**

Nostrgram также позволяет вам сохранять историю ваших взаимодействий с протоколом Nostr. Эта возможность также еще не представлена повсеместно. Учитывая структуру устройства Nostr это очень полезная опция. Сохранить историю можно, нажав на кнопку ⬇️ в вашем профиле.

**7. Возможность прикреплять медиафайлы**

Пользователям традиционных соцсетей сложно представить себе приложение, лишенное этой опции. Но с технической точки зрения внедрить подобное в распределенной системе, полагающейся на легковесные и простые (даже глупые) ретрансляторы не так уж и просто. Они попросту не способны хранить большие объемы медиа, которые так любят пользователи социальных сетей. Куда же мы без 🐸мемов, гифочек и вот этого всего. Nostrgram – единственный известный мне клиент, позволяющий добавлять изображения, видео и GIF, используя кнопки загрузки. Клиент автоматически берет ваш медиафайл, загружает его в облачное хранилище и размещает в посте ссылку, ведущую на файл. Другие клиенты заставляют вас делать это вручную, что, разумеется, усложняет взаимодействие с приложением и отнимает ваше время.

**8. Возможность приглушать отдельных пользователей**

Очень полезная функция, которая пригодится если вы, например, подписались на одного из ботов, например, на бота ChatGPT. любой подписавшийся на этого бота будет получать в свою ленту все его взаимодействия со всеми пользователями Nostr. Несложно представить во что превратится ваша лента в таком случае. Чтобы приглушить любого пользователя просто нажмите на значок 🔇в его профиле.

**9. Зашифрованные сообщения**

Эта функция не уникальна для Nostrgram, но является одной из важнейших возможностей Nostr. Как и в других клиентах протокола Nostr вы можете обмениваться зашифрованными сообщениями с другими пользователями. Но, как было сказано в моем посте, предоставленном выше, очень важно хранить свои приватные ключи в безопасности, ведь именно они расшифровывают эти сообщения.

**10. Русскоязычная версия интерфейса и другие функции в разработке**

Nostrgram предлагает еще множество тонких настроек, оценить которые можно в разделе (внимание!) ⚙️**настройки**, который, кстати, скоро будет доступен и на русском языке. Более того, Джон трудится над множеством других интересных нововведений. Узнать о планах и улучшениях Nostrgram можно, подписавшись на его Nostr-аккаунт (`npub1t9a59hjk48svr8hz6rx727ta6kx53n5d6fw8x26vsua0zytpl87sa6h4uw`).

Разумеется, вы можете выбрать любой другой клиент для взаимодействия с протоколом Nostr, и опыт использования будет во многом напоминать описанные мною принципы. Попробуйте разные клиенты и расскажите какой вам понравился больше всего в своем посте в Nostr.

## Аутро

В этом гиде мы затронули два важных приложения, которые нацелены на упрощение вашего взаимодействия с открытыми, безграничными, нейтральными, цензуроустойчивыми, никому не подконтрольными протоколами. Я, конечно, говорю о протоколах Биткоин и Ностр. Конечно, на рынке есть аналоги, но именно Alby и Nostrgram являются моими фаворитами в силу набора функций и отличной работы в связке – они как нельзя лучше дополняют друг друга.

---

{{< hint btc >}}
Напомню, что этот гид и все остальные материалы проекта 21 идея распространяются безвозмездно, а ваша помощь очень нужна некоммерческому образовательному проекту. Если материал оказался вам полезен, поддержите меня на сайте [21 идея](/contribute) или в Nostr 🤙
{{< /hint >}}

Также задавайте свои вопросы и делитесь впечатлениями от использования протоколов будущего! Задать свои вопросы касательно Биткоина, сети Молния и Nostr можно нам с Almoo:

- Tony – `npub10awzknjg5r5lajnr53438ndcyjylgqsrnrtq5grs495v42qc6awsj45ys7`
- Almoo – `npub1zvvv8fm7w2ngwdyszg3y6zgp6vwqlht8zrr8wcmjaxjecrvpjfwsd0zs7w`

В Nostr также есть система дополнительной верификации пользователей. Хотите получить чекмарк? Пишите мне в ЛС 📬
