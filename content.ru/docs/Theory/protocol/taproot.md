---
title: "Что такое Taproot"
h1: "Что такое Taproot и какую пользу он принесет Биткоину?"
cover: /img/tr-811.jpeg
description: "Taproot — это предлагаемое обновление Биткоина, в котором появится несколько новых функций."
url: taproot
date: 2021-09-26
bookFlatSection: false
weight: 60
---

Taproot — это предлагаемое обновление Биткоина, в котором появится несколько новых функций.

{{< hint btc>}}
[Поддержать проект](/contribute/)
{{</hint >}}

{{% image "/img/tr-812.png" /%}}

- Taproot — это предлагаемое обновление Биткоина, в котором появится несколько новых функций.
- Taproot интегрирует схему цифровой подписи Шнорр в Биткоин, модернизируя криптографию, лежащую в основе Биткоина.
- Taproot опирается на обновление SegWit, чтобы улучшить приватность Биткоина и снизить комиссию за транзакции.
- Taproot облегчает будущие обновления Биткоина, реформируя язык используемых им скриптов.  
    

# Введение

Taproot — это обновление Биткоина, которое принесет ряд новых функций и преимуществ для пользователей сети.  

Обновление Taproot фактически состоит из трех предложений по улучшению Биткоина (BIP), которые определяют три различные модернизации протокола: Schnorr Signatures, Taproot и Tapscript. Однако эти три обновления известны как обновление Taproot, а BIP 340, 341 и 342 часто называют BIP Taproot. Вместе эти обновления представляют новые, более эффективные, гибкие и приватные способы передачи биткоина.  

# Подписи Schnorr

BIP 340 интегрирует схему цифровой подписи Шнорра в Биткоин. Подписи Шнорра принесут пользователям Биткоина ряд преимуществ, включая повышенную приватность, более низкие комиссии и более гибкое взаимодействия со [схемами мультисиг](/multisig-1).  

Этот BIP также определяет, как публичные ключи и подписи Шнорра должны кодироваться для использования в Биткоине. Публичные ключи, используемые в подписях Шнорра, имеют длину 32 байта по сравнению с публичными ключами ECDSA длиной в 33 байта. Кроме того, длина подписей Шнорра равна 65 байтам по сравнению с подписями ECDSA, длина которых составляет 71-72 байта, включая [флаг sighash](https://river.com/learn/terms/s/sighash-flag/). Эта небольшая экономия места позволяет пользователям Биткоина, использующим Taproot, сэкономить на комиссии.  

# Taproot

В то время как BIP 340 определяет спецификацию для генерации и кодирования подписей Шнорра и публичных ключей, BIP 341 определяет, как протокол Биткоина будет интегрировать подписи Шнорра. В частности, Биткоин-скрипт должен быть обновлен, чтобы также оценивать подписи Шнорра. Taproot также интегрирует Merkelized Alternative Script Trees (MAST), которые позволяют пользователям блокировать выходы в нескольких скриптах одновременно.  

## Pay-to-Taproot (P2TR)

Taproot также представляет новый тип скрипта — способ траты биткоина. Pay-to-Taproot (P2TR) позволяет пользователям производить оплату либо на публичный ключ Шнорра, либо использовать корень Меркла ряда других скриптов. Используя этот новый тип скрипта, пользователь может создать [UTXO](https://t.me/bitcoin21ideas/151), который может быть разблокирован и потрачен либо владельцем приватного ключа, либо любым, кто может удовлетворить требования любого скрипта в дереве Меркла.  

## Агрегация ключей

Функция агрегации ключей Шнорра обеспечивает довольно гибкую функциональность. Когда биткоин отправляется на выход P2TR, он привязывается к одному приватному ключу, называемому Q. Однако этот приватный ключ Q на самом деле является агрегацией публичного ключа P и приватного ключа, сформированного из корня Меркл многих других типов скриптов. Любой из альтернативных скриптов в дереве Меркла может быть использован для траты выхода.  

{{% image "/img/tr-813.png" /%}}

Такая конструкция позволяет пользователям выбирать между сложными, произвольными скриптами, а также простыми функциями оплаты на публичный ключ (pay-to-public-key) в момент траты, а не в момент получения. Это также делает все выходы Taproot похожими друг на друга. Поскольку в блокчейне с введением обновления мультисиг транзакции, транзакции с одной подписью и другие сложные смарт-контракты будут выглядеть одинаково, многие эвристики анализа блокчейна станут непригодными, что повысит приватность всех пользователей Taproot.  

## Tapscript

Чтобы реализовать транзакции P2TR, BIP 342 добавляет и обновляет несколько операционных кодов. Эти новые скрипты используются для верификации Taproot-трат и подписей Шнорр, и известны под общим названием Tapscript.  

Tapscript был разработан для обеспечения максимальной гибкости P2TR-расходов в будущем, чтобы позволить модернизацию, которая еще далека от реализации.  

# Преимущества Taproot

Обновление Taproot предлагает множество преимуществ как пользователям Биткоина, которые принимают Taproot, так и тем, кто его не принимает. Введение подписей Шнорра дает значительные преимущества для приватности и безопасности, но Taproot и Tapscript также обладают рядом преимуществ.  

## Экономия пространства

Большинство выходов Taproot (P2TR) занимают меньше места в блокчейне, чем обычные выходы P2PKH, но немного больше, чем выходы P2WPKH. В основном это связано с тем, что P2TR-выходы привязывают биткоин непосредственно к публичному ключу, а не к хешу публичного ключа. Это делает отправку на выходы Taproot немного более дорогой, поскольку публичные ключи занимают больше места, чем их хеши. Однако тратить Taproot-выходы значительно дешевле, потому что открытый ключ включен в scriptPubKey, и поэтому его не нужно включать в [Script Witness](https://river.com/learn/terms/s/script-witness/).  

Taproot также определил схему кодирования для публичных ключей и подписей Шнорра, сделав их короче, чем их аналоги ECDSA, что обеспечивает дополнительную экономию средств.  

## Улучшения приватности

Последствия Taproot для приватности — это, пожалуй, самая важная составляющая обновления. Благодаря внедрению подписей Шнорра и агрегации ключей, контракты с несколькими подписями (мультисиг) больше внешне не отличается от контрактов с одной подписью, обеспечивая приватность для всех пользователей Taproot.  

Taproot также вводит значительные преимущества в плане приватности благодаря интеграции MAST. Как говорилось выше, Taproot позволяет заблокировать биткоин в многочисленных скриптах одновременно. Однако при расходовании биткоинов с выхода Taproot, пользователю не нужно раскрывать все возможные скрипты, которые могли бы разблокировать (потратить) биткоин; только основной скрипт, который он фактически использовал. В большинстве случаев пользователи Taproot, скорее всего, будут использовать опцию pay-to-public-key, что позволит им сохранить в тайне все запланированные ими запасные варианты.  

## Модернизация системы безопасности

На техническом, теоретическом уровне подписи Шнорра считаются более безопасными, чем подписи ECDSA. Как и все схемы криптографии на эллиптических кривых, ECDSA и Шнорр основываются на предположении, что проблема дискретного логарифма является трудной. Однако, чтобы гарантировать свою безопасность, ECDSA опирается на дополнительные предположения. Тем не менее, за время существования Биткоина не было ни одного примера систематической компрометации ECDSA.  

Подписи Шнорра также устраняют любую уязвимость подписи, которая могла присутствовать в подписях ECDSA. Хотя проблема искажения транзакций была решена обновлением SegWit, искажение подписей в ECDSA сохранилось.  

# Активация Taproot

На данный момент Taproot все еще является предлагаемым обновлением и еще не активирован в сети Биткоин. В случае предложения обновления сети Биткоин, оно сначала обсуждается сообществом разработчиков. Как только предложение формализуется, ему присваивается номер BIP. После того как код написан, рассмотрен, протестирован и объединен, операторы Биткоин-нод должны решить, как и когда активировать обновление.  

Обновления Schnorr, Taproot и Tapscript получили номера BIP 340, 341 и 342 в январе 2020 года и с тех пор находятся в стадии обсуждения и разработки. В конце 2020 года реализация кода всех трех обновлений была завершена, протестирована, рассмотрена и включена в Bitcoin Core.  

В настоящее время весь необходимый код для реализации Taproot уже есть на каждой обновленной до последней версии ноде Биткоина. Теперь сообщество должно решить, нужно ли активировать Taproot и как начать применять новые правила консенсуса. Существует несколько методов активации обновлений Биткоина, поэтому сообщество сначала должно было выбрать путь, а затем осуществить обновление.  

# Пути активации Биткоина

BIP 8 и BIP 9 определяют два популярных метода активации обновлений. Оба процесса начинаются с опроса Биткоин-майнеров на предмет поддержки. Если подавляющее большинство майнеров выражают свою поддержку через сообщения в блоках, которые они добывают, обновление активируется. Разница между BIP 8 и BIP 9 возникает, если поддержка майнеров недостаточна. В этом случае BIP 9 определяет, что обновление не должно происходить, в то время как BIP 8 определяет, что обновление должно быть активировано после периода задержки.  

Варианты этих двух предложений были выдвинуты в контексте активации Taproot. Однако сообщество Биткоин в подавляющем большинстве поддержало Taproot, а критики было очень мало. Таким образом, сам путь активации, скорее всего, окажется незначительным.  

На данный момент активация Taproot проходит по пути Speedy Trial в попытке добиться более быстрого принятия. За прогрессом активации можно следить на сайте [taproot.watch](https://taproot.watch/miners). Подавляющее большинство (84.96%) майнинг-пулов просигнализировало о поддержке обновления, но чтобы обновление вступило в силу 90% блоков, намайненных в период одной эпохи (между корректировками сложности, то есть за 2016 блоков), должны включать сигнал в поддержку Taproot. На сегодняшний день этот показатель составляет 31.89%.