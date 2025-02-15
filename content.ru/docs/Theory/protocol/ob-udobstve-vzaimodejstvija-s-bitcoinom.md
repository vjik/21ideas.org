---
title: "Об удобстве взаимодействия с Биткоином"
h1: "Об удобстве взаимодействия с Биткоином"
cover: /img/216.png
tags: ["протокол", "теория", "практика"]
description: "В Биткоин-пространстве продолжается дискуссия на тему пользовательского опыта (UX). Биткоин до сих пор выглядит странно, неуклюже и порой сложно. Таким же был и, возможно, до сих пор остается интернет"
url: ob-udobstve-vzaimodejstvija-s-bitcoinom
date: 2020-09-20
bookFlatSection: false
bookToc: false
weight: 53
---

В Биткоин-пространстве продолжается дискуссия на тему пользовательского опыта (_UX_). Биткоин до сих пор выглядит странно, неуклюже и порой сложно. Основной причиной этого является то, что Биткоин и его составляющие (сеть, протокол, криптография, язык программирования) действительно странные, неуклюжие и сложные. Таким же был и, возможно, до сих пор остается интернет.

{{< hint btc >}}
Перевод [статьи](https://www.swanbitcoin.com/on-bitcoins-ux/) GiGi подготовлен [Тони⚡️](https://snort.social/p/npub10awzknjg5r5lajnr53438ndcyjylgqsrnrtq5grs495v42qc6awsj45ys7). [Поддержать проект](/contribute/).
{{< /hint >}}

{{% image "/img/216.png" %}}
_До LNP/BP и TCP/IP имел место IPX/SPX_
{{% /image %}}

Причина, по которой интернет больше не кажется таким неуклюжим, двояка: (1) люди привыкли ко многим новым понятиям, которые принес с собой интернет, и (2) бесчисленные абстрагирующие слои облегчают взаимодействие с базовым протоколом. Сопутствующие технологии, такие как plug-and-play, помогли сделать работу пользователя еще комфортнее. Дни установки номера IRQ вашей сетевой карты вручную уже в прошлом!

{{% image "/img/217.png" %}}
_"Что такое IRQ?"_
{{% /image %}}

Как и интернет, Биткоин — это развивающаяся экосистема. Имейте в виду, что многое уже изменилось к лучшему. Например, первый кошелек, который поддерживал QR-коды, был выпущен в 2012 году. В том же году были предложены XPUB ([BIP32](https://github.com/bitcoin/bips/blob/master/bip-0032.mediawiki)). Сид-фразы ([BIP39](https://github.com/bitcoin/bips/blob/master/bip-0039.mediawiki)) были предложены в 2013 году. [BIP44](https://github.com/bitcoin/bips/blob/master/bip-0044.mediawiki) (HD-кошельки, они же "аккаунты") появился в 2014 году. SegWit ([BIP141](https://github.com/bitcoin/bips/blob/master/bip-0141.mediawiki)) был предложен в 2015 году и — после продолжительной гражданской войны — активирован в 2017 году. Сегодня большинство воспринимает QR-коды и сид-фразы как должное, не осознавая, что они не всегда были частью Биткоина. Я уверен, что некоторые воспринимают сеть _lightning_ (появившуюся благодаря SegWit) также в порядке вещей.

Я считаю, что все эти “закулисные” технические улучшения безумно важны для UX. Без них взаимодействие с сетью Биткоин показалось бы адом. Сид-фразы? Простое восстановление кошелька? Сеть lightning? Забудь! Тем не менее, все эти улучшения безумно технологичны и требуют технического обсуждения. Не за горами новые улучшения (Шнорр, Тапрут и [многие другие](https://bitcoinmagazine.com/articles/2020-and-beyond-bitcoins-potential-protocol-upgrades)), так что готовьтесь к тому, что обсуждения в Биткоин-пространстве останутся техническими еще довольно долго. Ассоциируйте Биткоин с "Linux", а не с "iPhone".

{{% image "/img/218.png" %}}
_"Git был иным в 1998 году"_
{{% /image %}}

Кстати об айфонах: Наблюдается напряженность в отношениях между изобретателями и фанатами айфонов и компании, ожидающими, что все будет работать идеально и будет супер-интуитивно, причем ПРЯМО СЕЙЧАС.

Ну, прямо сейчас идеально работать ничего не будет. Точно так же, как во времена зарождения интернета нужно было знать, что такое IP-адрес и как работает коммутация пакетов, так и сегодня нужно знать, что такое XPUB. DHCP, по сути, решил проблему IP-адресов, так же, как Google расправился с проблемой "ввода точных URL". Всё это придет и в Биткоин. Просто это не произойдет в мгновение ока.

Базовый протокол, вероятно, будет постепенно “отвердевать”, так же, как и TCP/IP окреп со временем. Как только базовый уровень будет достаточно оптимизирован, большинство инноваций начнут происходить на более высоких уровнях.

{{% image "/img/219.png" %}}
_"Круто. Теперь, когда мы разобрались с пользовательским интерфейсом, давайте обновимся до IPv6."_
{{% /image %}}

Я считаю, что те, кому разработка знакома не понаслышке, просто устали от слов "это так сложно, все должно быть проще". Да, мы согласны, все должно быть проще, и мы упорно работаем над тем, чтобы это было именно так.

Некоторые из них создают простые в использовании продукты (Strike, Casa, Coinkite, Samourai и т.д.), другие работают над улучшением протоколов, чтобы в будущем все было проще и лучше (спасибо Core-разработчикам!), третьи работают над более широкой экосистемой (Raspiblitz, BTCPay Server, Umbrel и т.д.), а четвертые — над просвещением и распространением информации(Nakamoto Institute, Bitcoin-only, "21 идея"), чтобы больше людей могли принять участие в проекте и помочь сделать Биткоин лучше.

Со временем люди привыкнут к понятиям, от которых нельзя абстрагироваться. Я убежден, что все станет проще, наподобие того, как и подключиться к сети интернет сейчас легче, чем это было в 1995 году.

{{% image "/img/220.png" %}}
_"Делай хорошие вещи"_
{{% /image %}}

Биткоин — это новая парадигма, как и интернет в свое время. Точно так же, как нельзя было избавиться от адресов электронной почты ("Что это за странный знак @?") и URL ("Что такое http/https/ftp/ssh?"), на сегодняшний день нет возможности обойти биткоин-адреса, приватные ключи, и, как вы уже догадались, XPUB.

Некоторые концепты очень важны, отказ от них с целью получения лучшего UX, может привести к фатальным результатам. Откажитесь от коммутации пакетов ([сетевой нейтралитет](https://www.battleforthenet.com/)) в сети интернет, и вы уничтожите то, что изначально сделало интернет великим. Пожертвуйте самостоятельным хранением монет (или созданием учетной записи посредством математики, или нейтралитетом, или множеством других вещей) в Биткоине, и вы уничтожите то, что делает его великим в первую очередь. Само собой разумеется, что самостоятельное хранение всегда будет хуже с точки зрения UX, по сравнению с тем, чтобы позволить кому-то другому хранить ваши монеты. Точно так же, создание собственного домена и хостинг собственного сайта всегда принесет больше хлопот, чем создание страницы в Facebook. Это всегда вопрос компромиссов.

Сосредоточение внимания исключительно на максимизации UX может привести к неоптимальным результатам в долгосрочной перспективе. Просто сравните Facebook, TikTok и огороженный сад iOS с не требующими разрешения открытыми протоколами и экосистемой FLOSS. Лично я всегда предпочту свободу удобству.

Впереди светлое будущее. Просто у нас много работы.

_Gigi_
