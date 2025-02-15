---
title: "Централизованна ли сеть Lightning?"
h1: "Централизованна ли сеть Lightning?"
cover: /img/csl-716.png
description: "По “криптосообществу” начинает гулять миф, согласно которому сеть Молния (Lightning Network) является централизованной. Предлагаю разобраться, так ли это."
url: centralizovanna-li-set-lightning
date: 2022-12-26
bookFlatSection: false
weight: 5
---

По “криптосообществу” начинает гулять миф, согласно которому сеть Молния (Lightning Network) является централизованной. Предлагаю разобраться, так ли это.

{{< hint btc >}}
В основе этого материала лежит [статья](https://darthcoin.substack.com/p/omg-ln-nodes-are-running-on-amazon?r=mu07o&utm_medium=ios&utm_campaign=post) DarthCoin. Русскоязычная версия подготовлена [Тони⚡️](https://snort.social/p/npub10awzknjg5r5lajnr53438ndcyjylgqsrnrtq5grs495v42qc6awsj45ys7).

[Поддержать проект](/contribute).
{{< /hint >}}

Ок, плебсы, по “криптосообществу” начинает гулять миф, согласно которому сеть Молния (Lightning Network) является централизованной. Эта информация заставляет некоторых биткоинеров ужаснуться, а щиткоинерам придает мнимой уверенности в том, что любимые ими проекты не так уж и плохи. Но дело в том, что эта информация ложная.

Если честно, я даже рад тому факту, что теперь поле боя сместилось. Нападкам подвергается уже не основная сеть Биткоин, а второй слой, нацеленный на повышение масштабируемости и приватности. Все меньше новичков сомневается в децентрализации Биткоина и переживает о вероятности успешной атаки на сеть; все больше щиткоинеров отказывается от попыток атаковать Биткоин и уличить его в ненадежности или подверженности каким-либо атакам. Медленно, но уверенно, как и заведено в Биткоине, мы выигрываем одну битву за другой и движемся по выбранному нами пути к гипербиткоинизации.

Ну что ж, раз подавляющее большинство уже убеждено в нерушимости основного слоя Биткоина, пора начинать строить фундамент для защиты сети Молния от нападок хейтеров и невежд, в частности, для защиты святой всех святых любой свободной и нецензурируемой сети или протокола: децентрализации.

К моему удивлению, опасения сообщества были вызваны графиком, предоставленным биткоин-онли сервисом, созданным биткоинерами для биткоинеров, [mempool.space](https://mempool.space/ru/). Складывается впечатление, что биткоинеры здесь выстрелили себе в ногу, и отчасти это правда. Просто взгляните на этот график:

{{% image "/img/csl-716.png" %}}
[_https://mempool.space/ru/graphs/lightning/nodes-per-isp_](https://mempool.space/ru/graphs/lightning/nodes-per-isp)
{{% /image %}}

Любой не знакомый с принципами работы сети интернет ужаснется при виде такого “уровня централизации”. Увидев такой график и правда можно решить, что более половины ликвидности сети располагается на серверах Google и Amazon, и такое распределение никак нельзя назвать децентрализованным. Но не все так просто…

Во первых, ребятам из Mempool.space стоит приложить к этому графику пояснение или, как минимум, перефразировать сам его заголовок (название графика на русском является дословным переводом английского заголовка). Но я предлагаю разобраться с основными факторами, влияющими на показатели данного графика, чтобы в итоге осознать, что на самом деле ничего не грозит децентрализации сети.

Вот несколько основных аспектов, на которые следует обратить внимание:

- Облачные узлы, размещенные в дата-центрах
- Узлы VPS, выделенные серверы, размещенные в дата-центрах
- VPS, которые используются в качестве VPN-шлюзов
- VPN сервисы, пользователь которых получает IP из другой географической локации
- Сеть Tor – отдельная, приватная сеть
- Узлы clearnet – просто узлы с реальными обычными IP-адресами

**Глоссарий:**

**VPS** = виртуальный выделенный сервер  
**VPN** = виртуальная частная сеть  
**Tor** = система прокси-серверов, позволяющая устанавливать анонимное сетевое соединение, защищенное от прослушивания  
**Clearnet** = обычный IP-адрес/домен в Интернете  
**ISP** = интернет-провайдер, тот, кто предоставляет вам интернет дома/на работе

## Облачные узлы

Да, существует большое количество узлов сети Молния (LN), которые запущены в дата-центрах. Предприятия, разработчики, тестировщики и т.д. могут запускать некоторые LN-узлы таким образом с целью достижения большей надежности и в качестве резервных копий. В конце концов, их главная цель – защитить свои системы, а запуск узла на Raspberry Pi не является самым надежным решением для среднего или крупного бизнеса. Но целью этого материала не является выявление лучшего оборудования для запуска собственной ноды. Все узлы по своему хороши!

Давайте не будем забывать, что поставщик облачных узлов Voltage сейчас переживает значительный приток пользователей. Многие не прочь запустить узел за 5 минут, не имея при этом собственного оборудования. Поэтому многие выбирают [Voltage](https://voltage.cloud/), позволяющий запустить собственную ноду в несколько кликов и, более того, сделать это за несколько минут (да, в этом случае не нужно ждать загрузки блокчейна в течение нескольких суток). Да, сервис Voltage стоит от $12 в месяц; да, это не идеальное решение… но это вполне оправданный подход, если вы знаете, что делаете. Итак, все эти облачные узлы Voltage располагаются в дата-центрах (Amazon, Google и т.д.).

Все эти облачные узлы будут использовать и объявлять IP того дата-центра, который им выделен для каждого узла. Этот IP может принадлежать и транслироваться Amazon, Google и т.д. О том, как публичные IP распределяются между провайдерами, можно узнать из [этого короткого видео](https://www.youtube.com/watch?v=fja1OWBq7fY).

Очевидно, что на представленном выше графике появится определенное количество “узлов, запущенных Amazon’ом”.

Представляют ли эти "облачные узлы" угрозу децентрализации сети Молния?

Возможно, но не такую уж и значительную. Пользователь узла всегда будет контролировать свои ключи. Если ваш узел вдруг будет отключен по решению дата-центра, вы, обладая сид-фразой и актуальной резервной копией каналов, в любой момент можете запустить другой узел дома или в любом другом месте. То есть вы без труда сможете восстановить и запустить свой узел в считанные минуты.

Хорошим примером является [облачный узел, управляемый Sphinx](https://twitter.com/sphinx_chat/status/1571974701098074112) через хранящиеся дома ключи. Поэтому даже если “облачное” оборудование будет скомпрометировано, управлять им без ключей будет невозможно.

{{% image "/img/csl-717.png" %}}
_В сети Молния 17,000 узлов, но наш немного отличается. Core Lightning запущен в облаке, приватные ключи защищены с помощью_ [_VLS_](https://vls.tech/) _устройством, находящимся дома. Выделенное оборудование значительно упрощает процесс. Мы уже на шаг ближе к мультисигу для Lightning._
{{% /image %}}

Эти облачные узлы никак не могут подвергнуть обычный LN-трафик опасности.

## VPS-узлы

Эти узлы более или менее аналогичны облачным. Разница заключается в том, что пользователь сам управляет всей операционной системой, программным обеспечением узла, приложениями, доступом и т. д. Дата-центр управляет только аппаратным обеспечением.

Ситуация практически ни чем не отличается от предыдущего случая: пользователь может в любое время развернуть свой VPS-узел у любого другого провайдера или на собственном оборудовании – ключи также хранятся у запустившего узел.

Отображаемые IP-адреса также, как правило, не значат, что узел подконтролен, например, Amazon или Google. Они могут быть выданы различными крупными интернет-компаниями. По сути, это просто ссылка.

## VPS, используемые в качестве VPN-шлюзов

Мы подошли к самой интересной части!

Итак, пользователь арендовал оборудование в дата-центре, но **не** запускает узел на этом оборудовании! Он просто использует оборудование для запуска Linux как основы для VPN прокси, и подключает к нему свой домашний LN-узел, используя VPN туннель.

Таким образом, весь трафик узла LN будет перенаправлен через публичный IP, назначенный арендатором удаленному VPS, и купленный у различных крупных интернет-провайдеров.

Так что этот узел, даже если он использует определенный IP, не означает, что он физически там расположен, или даже, что запустивший узел пользователь является резидентом соответствующей страны. Это тем более не значит, что узел подконтролен Amazon или Google. Это просто ссылка.

Обычно эти VPS LN-узлы также работают на Tor, в гибридном режиме, в обеих сетях. Это лишь добавляет путаницы таблице.

Примером подобных VPS-сервисов может послужить [TunnelSats.com](https://tunnelsats.com/).

Является ли такой подход угрозой для LN? Ни в коем случае! Пользователь может в любой момент сменить VPS-провайдера или просто работать через Tor.

## VPN-сервисы

Пользователь арендует специальный сервис, который предоставляет ему выделенную сеть для всего домашнего трафика. Пользователь использует туннель и один или несколько IP-адресов.

Пользователь настраивает свой лайтнинг-узел для работы через эту сеть, но используя свое домашнее зашифрованное и приватное интернет-соединение.

Таким образом его узел может отображаться в диаграммах как использующий IP от Amazon, но Amazon не имеет никакого отношения к этому узлу. Опять же, это просто ссылка.

Является ли это угрозой для LN? Ни в коем случае! Пользователь может в любое время сменить VPN-провайдера или просто работать через Tor или даже использовать собственный домашним IP.

## Сеть Tor

Пользователь работает, сохраняя полную приватность своего узла, используя **только** сеть Tor. Не будем вдаваться в подробности работы этой сети, ведь у Джеймсона Лоппа есть [отличная статья](https://blog.lopp.net/tor-only-bitcoin-lightning-guide/), объясняющая, как работают эти Tor-узлы.

Представляют ли они угрозу для сети узлов LN? Нет!

Да, сеть Tor может быть медленной и неуклюжей в некоторых уголках нашей планеты, но в основном она работает отлично.

## Узлы Clearnet

Это самые обычные узлы, запущенные дома или в любом другом удобном пользователю месте. Их IP, как правило, отражает их интернет-провайдера.

Но я не буду на 100% полагаться на точность этих данных в диаграммах. Эти IP могут время от времени меняться или, если это публичные IP, они составляют лишь малую часть общего множества.

Представляют ли они угрозу для сети узлов LN? Ни в коем случае! Эти пользователи могут в любой момент взять свои узлы и подключить их к другой сети или даже к мобильному интернету, и их узел снова будет в сети.

## Вывод:

Сети Молния не угрожает централизация; сеть не может быть уничтожена!

Эти графики лишь подпитывают биткоин-хейтеров и пугают тех, кто не интересовался устройством сети интернет.

Как объяснил Джестофер из [Amboss](https://amboss.space/) на стриме Simply Bitcoin,

> _"LN может очень легко адаптироваться, и широкое распределение узлов и каналов не сильно пострадает, если один из дата-центров закроет доступ к некоторым облачным узлам. Пользователи смогут сразу перераспределить весь трафик через множество других пиров":_

{{< youtube b7fvoBsMUGw />}}

Не переживайте за децентрализацию сети Молния. Запускайте собственные узлы, открывайте каналы и поддерживайте работу самой быстрой, практически бесплатной, свободной и нецензурируемой сети в мире!
