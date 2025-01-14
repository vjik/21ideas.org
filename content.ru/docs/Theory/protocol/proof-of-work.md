---
title: "Proof of Work: доказательство проделанной работы"
h1: "Proof of Work: доказательство проделанной работы"
cover: /img/pow-608.png
description: "Алгоритм Proof of Work — это то, что связывает мир цифровых денег с физическим миром, не требуя при этом доверия третьей стороне."
url: proof-of-work
date: 2020-12-07
bookFlatSection: false
bookToc: true
weight: 58
---

{{< hint btc>}}
_Перевод_  [_статьи_](https://joinmarket.me/blog/blog/pow-a-pictorial-essay/) [_Адама Гибсона_](https://x0f.org/@waxwing) _от 07 декабря 2020 г. подготовлен биткоинером_ [_Tony ฿_](https://twitter.com/TonyCrusoe)

[Поддержать проект](/contribute/)
{{</hint >}}

В современном национальном государстве суды ("правосудие") функционируют, посредством насильственных угроз. Точный способ разрешения спора варьируется (присяжные, один судья и т.д.), но "необратимость" представленного решения основывается на том, что государство отстаивает окончательный вердикт, а ваше несогласие не имеет значения, потому что на их стороне наемники с оружием. Важно, что у них не просто есть люди с оружием (они, возможно, есть и у вас), у них есть подавляющее большинство людей с количеством огромных пушек, пропорциональным вашему нежеланию подчиниться их решению.

Если вы думаете, что "это глупый и слишком упрощенный способ мышления о современных системах правосудия", ничего страшного; многое из того, что следует далее, как раз и заключается в тонкости этого упрощенного взгляда на современность.

# Угроза опаснее, чем ее исполнение

Этот афоризм уходит своими корнями в шахматный мир (насколько я знаю); он каким-то образом одновременно и очевиден, и утончен. Простите, что отвлекаюсь, но он напоминает мне о возможном создателе этого выражения, противоречивой фигуре в истории шахмат — Ароне Нимцовиче. В одной его (апокрифической?) истории он указывает на своего соперника-гроссмейстера и громко заявляет: "Почему я должен проиграть этому идиоту?!". Но вернемся к делу: Нимцович написал один из самых известных ранних трактатов; он был посвящен шахматной стратегии под названием "Моя система".

{{% image "/img/pow-609.png" /%}}

В этой книге он популяризировал (среди многих других менее спорных вещей) идею **чрезмерной защиты** — так, например, пешка расположена на клетке е5, и он считал хорошей стратегией защиту ее конем на f3, ладьей на е1 и слоном на g3 и т. д. и т. п. Многие игроки — лучшие гроссмейстеры — сегодня находят эту идею немного забавной. Меня интересует то, что когда они высмеивают эту идею, то, по сути, отказываются принимать во внимание содержащийся в ней элемент истины, а именно: если N > 1 фигур защищают ключевую клетку, это значит, что любой из них может двигаться, не жертвуя защитой этого поля. Другими словами, сохраняется возможность перемещения любой фигуры (в отличие от сценариев с единственным защитником, который, следовательно, не может покинуть пост).

{{% image "/img/pow-610.png" /%}}

Идея фразы "угроза опаснее ее исполнения", которая поначалу звучит парадоксально, обладает определенными сходствами. Противнику сложнее противостоять потенциальной возможности, чем реальности, главным образом потому, что противнику, возможно, придется бороться со многими потенциальными сценариями, а не с тем единственным,  который в итоге будет актуализирован.

Это может проявляться и психологически — нагонять _страх_ на противника зачастую является очень эффективной стратегией по сравнению с непосредственным нападением. Но важно понимать, что это не просто игры разума. Это вопрос экономики и вопрос абстракции. Как и в развитии количественных дисциплин (от ранней математики до современного компьютерного программирования, да и львиной доли современной науки), развитие абстракций позволяет экономить, максимально эффективно используя ресурсы, и даже открывать совершенно новые, ранее недоступные измерения.

# Виртуализация насилия

Эта линия мышления естественным образом ведет нас к тому, что насилие как конкретная актуализация воли имеет тенденцию к абстрагированию. Это видно не только в человеческом обществе, но и в природе. Хорошо известно как право спаривания у социальных животных (различных видов млекопитающих) "определяется" посредством боя, и, что немаловажно, битва редко ведется насмерть. Еще более поразительно то, что "битва" сводится к конкуренции посредством атрибутов, которые _могут позволить добиться большего успеха в бою_. Очевидным примером являются рога оленя:

{{% image "/img/pow-611.png" /%}}

Они — масса сырого физического материала, требующего большого количества питательных веществ с неоднозначной полезностью (очень неэффективно!). Это лишь квази-абстракция по сравнению с рогами, предназначенными для убийства — они могут служить инструментом убийства других оленей, но, видимо, это очень редкое явление. Они эволюционировали таким образом, чтобы другие олени могли с легкостью их визуально оценить, а их сложная геометрия позволяет проводить сражения ("сцепились рогами"), которые являются скорее оценкой способности убивать, чем попыткой сделать это. Конечно, есть много других примеров, которые являются более очевидными абстракциями. Примеры, представленные далее могут быть предназначены не для нанесения насилия, а являться атрибутами, демонстрирующими высокий уровень общей физической подготовки, что само по себе является абстракцией от "способности собирать большое количество ресурсов". Павлин — самый известный и яркий пример, хотя точные механизмы, относящиеся к данному примеру, могут и не быть научно доказанным фактом.

{{% image "/img/pow-612.png" /%}}

Я предоставлю биологам возможность порассуждать на эту тему; уверен, что они смогут расширить этот список бóльшим количеством не самых очевидных примеров...

Довольно интересное обобщение одного из взглядов на эти явления — [концепция гандикапа](https://ru.wikipedia.org/wiki/%D0%9A%D0%BE%D0%BD%D1%86%D0%B5%D0%BF%D1%86%D0%B8%D1%8F_%D0%B3%D0%B0%D0%BD%D0%B4%D0%B8%D0%BA%D0%B0%D0%BF%D0%B0) (о которой я почему-то не слышал до того, как написал бóльшую часть этого эссе, и как вы вскоре поймете, мне очень жаль, что я не знал о существовании этой гипотезы ранее!).

Кроме того, два примера, с которыми мы ознакомились выше, указывают на две стороны данного явления: показать доминирование через демонстрацию способности побеждать битву, даже не участвуя в ней; показать превосходную пригодность, демонстрируя способность собирать ресурсы, не собирая их на самом деле. Эти явления явно _не критично_ отличаются друг от друга.

# Современное человеческое общество схоже

Даже в современном обществе мы также можем наблюдать оба типа “абстракции”. Наиболее очевидна виртуализация жесткой конкуренции в спорте:

{{% image "/img/pow-613.jpeg" /%}}

(Пожалуй не случайно в большей степени спортсмены находятся практически на вершине брачной иерархии, по крайней мере, для некоторых женщин!). Но чтобы не быть слишком абстрактными, не будем забывать, что в целом демонстрация _способности_ к насилию — это тоже важная особенность человеческого общества, даже на уровне государств-наций:

{{% image "/img/pow-614.jpeg" /%}}

И как только мы начинаем думать о человеческом поведении таким образом, мы начинаем замечать это повсюду. Возьмем к примеру обручальное кольцо и зададимся вопросом, откуда взялась эта традиция:

{{% image "/img/pow-615.jpeg" /%}}

Тут мы уже не сильно отличаемся от павлинов... даже если это не самое корректное сравнение, оно имеет место быть. Давайте проведем более тщательную аналогию между павлином, изображенном на фото выше и обручальным кольцом. Итак, оба:

- выглядят эффектно;
- внешне весьма обворожительны;
- (визуально) очень выделяются среди “обычных вещей” в окружающем мире;
- быстро и легко, без пояснений, всеми узнаваемы;
- своим внешним видом сигнализируют о том, что обладатель того либо другого является значимой частью (культурного или генетического) вида.

Менее очевидным, на мой взгляд, является то, что постоянство этих атрибутов не стоит во главе угла. Иногда они крайне деликатны и хрупки (вспомните, к примеру, цветы; вспомните спорт, связанный с определенным риском травм, которые могут привести к неспособности повторить былые достижения),  это _практически_ и есть суть — для получателя сигнала большее значение имеет то, что сигнал было сложно произвести.

Гораздо меньшее значение имеет "субстрат", т.е. то, из чего "состоит" сигнал.

Это лишь один из шагов к пониманию "принципа гандикапа": важно то, что ты _не сделал_, делая это  

{{% image "/img/pow-608.png" /%}}

Представьте себя маленькой птичкой в джунглях — чтобы найти партнеров по спариванию в этой **чрезвычайно** шумной обстановке, вы ищете небольшой сигнал — пятнышко яркого цвета в столь пестрой обстановке. Вы хотите, чтобы сигнал был однозначным — синий на фоне зеленого, желтого, коричневого, красного окружения — и сложным для воспроизведения. Вы не хотите сравнивать его с чем-либо другим с целью убедиться в его подлинности (это тот же цвет, что и там, в противоположной части джунглей? хм!). В подобной ситуации вас не волнует семантика, вас не волнует, что "означает" сигнал, за исключением того, что он в некотором смысле предварительно согласован (возможно, генетически? см. последний буллет👆). Для постороннего этот сигнал может показаться странным или нелепым, но это не имеет значения.

# Суд, банк и абстракция денег

{{% image "/img/pow-616.png" /%}}

Это прослеживается и в архитектуре; конечно же, есть очень веская причина, по которой исторически банки строились из чрезвычайно прочных материалов и по сей день ассоциируются с дороговизной постройки. Изначально они были хранилищами, в которых концентрировались немалые объемы физического богатства, и должны были быть хорошо защищены от прямого нападения.

{{% image "/img/pow-617.png" /%}}

Сегодня это — очередная абстракция уже упомянутого типа; если организация вложила столько денег в строительство столь внушительного здания или сверкающего небоскреба, вряд ли они украдут мои жалкие сбережения! Здания судов также представляют собой абстракцию власти государства, как и правительственные учреждения (это особенно очевидно в таких авторитарных государствах, как Китай, где правительственные здания в маленьких городах выглядят почти абсурдно (Лусянь является типичным примером):

{{% image "/img/pow-618.png" /%}}

Парадигма "виртуализации", принятия конкретной физической силы и замены ее "угрозами, которые опаснее чем их исполнение", покорила царство денег в том числе. Во избежание различных споров о происхождении денег, я коснусь лишь новейшей истории: мы перешли от инструментов на предъявителя и сертификатов на инструменты на предъявителя, к сертификатам, представляющим собой чистый "фиат" в буквальном смысле; фиат, означающий, по сути, волю правящей власти. Так что [высказывание](https://www.youtube.com/watch?v=MJWi8VUHUzk) Пола Кругмана "фиат подкреплен людьми с оружием" ..

{{% image "/img/pow-619.png" /%}}

...безусловно, по сути, верно, даже если вы решите поспорить о тех или иных деталях. Аналогичным образом и суды "подкреплены людьми с оружием".

Но я думаю, что важно сделать шаг назад и задуматься о том, какую роль деньги играют в обществе — их целью всегда является именно абстракция. Они решают проблему "[двойного совпадения желаний](https://ru.qaz.wiki/wiki/Coincidence_of_wants)", создавая совершенно новый класс товара, в котором никто изначально не нуждался. Это контринтуитивно с точки зрения большинства математических случаев — чтобы решить проблему, включающую 2 или 3 элемента, нужно добавить еще один, поверхностно усложнив все, но внезапно все "встает на свои места" благодаря новой, более симметричной структуре. Например, если полиномиальное уравнение запутанно и даже нерешаемо (см. [Галуа](https://ru.wikipedia.org/wiki/%D0%93%D0%B0%D0%BB%D1%83%D0%B0,_%D0%AD%D0%B2%D0%B0%D1%80%D0%B8%D1%81%D1%82)) в случае с вещественными числами, усложнив его при помощи нового выдуманного решения x^2=-1, вы вдруг обнаружите, что все само собой сходится (см. [основная теорема алгебры](https://ru.wikipedia.org/wiki/%D0%9E%D1%81%D0%BD%D0%BE%D0%B2%D0%BD%D0%B0%D1%8F_%D1%82%D0%B5%D0%BE%D1%80%D0%B5%D0%BC%D0%B0_%D0%B0%D0%BB%D0%B3%D0%B5%D0%B1%D1%80%D1%8B)). Деньги делают нечто подобное, потому что мы заменяем проблему ценообразования O(N^2) проблемой ценообразования O(N) — т.е. вы не должны оценивать все относительно всего, вы можете оценивать все относительно денег. Естественно, это еще не все, ведь не всякий товар справится с ролью денег, поэтому деньги сами по себе не являются чистой абстракцией; их целью является абстракция. Их роль как абстракции заключается в том, чтобы уменьшить когнитивную нагрузку, связанную с необходимостью формировать отношения между товарами и услугами, от нерабочей системы к чему-то разумному. Приведу ... не абстрактный ... пример: за несколько дней до появления чего-то подобного деньгам, чтобы обменять хлеб на обувь, я (пекарь) должен был познакомиться с Фредом сапожником и установить с ним долгосрочные полу-доверительные отношения. Так что, даже если деньги окружены социальными явлениями, они сами по себе не являются социальными — именно из-за ограничений, продиктованных формированием социальных групп нам и нужны деньги. Напоминание биткоинерам: "все то доверие, необходимое для того, чтобы это сработало" — та самая фраза, которую вы должны были усвоить.

Несмотря на всю его значимость, описанное в параграфе выше и является тем, что по какой-то причине многие биткоинеры и другие сторонники криптовалют, кажется, довольно редко усваивают. Например фразы наподобие: "это, по сути, социальный феномен", "это деньги, подконтрольные народу", произносимые снова и снова, категорически ошибочны. Более того, они противоположны действительности. Деньги **по своей природе не являются социальными**, повторяю: даже несмотря на то, что они существуют в социальном контексте, их цель — противодействовать этим ограничениям.

# Опредмечивание и информация

Глагол "опредметить" довольно необычен, но мне кажется, что он очень уместен и недостаточно часто употребляется в этом контексте. Чтобы избавить вас от суеты поиска:

Переходный глагол, означающий рассматривать или относиться (к абстракции) так, будто она имеет конкретную или материальную форму. Превратить в предмет; сделать реальным или материальным; рассматривать как вещь.

Я думаю, что данный термин часто используется чуть ли не с целью унижения (отношение к чему-то как к реальному в то время, как этого на самом деле не существует), но я предпочитаю альтернативный, положительный вариант, приведенный выше. Возможно, мое применение данного термина и причудливо, но я придерживаюсь его, потому что не вижу лучших способов передать смысл.

Мне вспоминается беседа с другом детства, который был увлечен компьютерами даже в начале 80-х, когда их даже отыскать было сложно; он спросил меня "существует ли что-либо, что компьютеры не смогли бы скопировать, используя бинарную графику?" — он имел в виду музыку, изображения и т.д. Споры о том, что собой представляют "виртуальные" единицы по сравнению с реальными, разумеется, продолжаются и по сей день.

Термин "виртуальная валюта", так полюбившийся некоторым законодательным органам и другими софистами, актуален, но я не смогу всецело пояснить суть до тех пор, пока мы не дойдем до конца этого эссе. В качестве отправной точки важно признать, что расчеты не являются бесполезными.

Любые вычисления требуют реальной работы, какой бы незначительной она ни была (я понятия не имею, сколько джоулей нужно вашему мозгу, чтобы превратить 3+8 в 11, но точно не ноль). Хотя это и заставляет вычисления выглядеть непригодными к созданию сигналов, необходимо лишь немного пораскинуть мозгами, чтобы увидеть огромное преимущество такого рода работы по созданию сигналов: они предельно однозначны.

Более того, в области криптографии в частности, а не вычислений в общем, долгая история исследований предоставила методики для создания вычислений с этой огромной односторонней асимметрией: они могут быть экспоненциально более быстрыми при "создании" относительно того, как много времени они занимают, чтобы "обратить" (я немного отклонюсь от темы, но в некотором роде, это одна из историй двадцатого века о том, как развитие быстрых вычислений открыло окна в области математики, поспособствовавшие их развитию. Канонический пример — факторизация целых чисел: пожалуй, в течение сотни лет уже было известно, что факторизация полупростых чисел N в простые числа p_1, p_2 становится (иногда) попросту сложной для больших значений N. Но до тех пор, пока мы не разработали компьютеры, это никого не волновало. В этот момент (см. [Clifford Cocks](https://en.wikipedia.org/wiki/Clifford_Cocks) и таких личностей, как [Diffie](https://ru.wikipedia.org/wiki/%D0%94%D0%B8%D1%84%D1%84%D0%B8,_%D0%A3%D0%B8%D1%82%D1%84%D0%B8%D0%BB%D0%B4) и др., в 70-х годах, а также обязательно обрати внимание на наш [четырехсерийный документальный фильм о становлении движения шифропанков](https://youtube.com/playlist?list=PLfCndTr__6HfnWzqQxso2Jh8AtlhCy3wf)) стало ясно, что мы можем создать ["потайной вход", одностороннюю функцию](https://ru.wikipedia.org/wiki/%D0%9E%D0%B4%D0%BD%D0%BE%D1%81%D1%82%D0%BE%D1%80%D0%BE%D0%BD%D0%BD%D1%8F%D1%8F_%D1%84%D1%83%D0%BD%D0%BA%D1%86%D0%B8%D1%8F_%D1%81_%D0%BF%D0%BE%D1%82%D0%B0%D0%B9%D0%BD%D1%8B%D0%BC_%D0%B2%D1%85%D0%BE%D0%B4%D0%BE%D0%BC#RSA), т.е. функцию, которую можно быстро отменить, если знаешь секрет, и фактически невозможно отменить иным образом. Это имитирует асимметрию силы или влияния).

История криптографических хеш-функций немного отличается от заключенного в скобки выше, но в попытке избежать повтора курса “крипто для чайников” (вам [сюда](https://toc.cryptobook.us/)), давайте просто скажем, что они разделяют основную суть: быть очень простыми в одном направлении и "трудно обратимыми" только в том смысле, что вы не можете легко найти другой вход, соответствующий тому самому выходу.

Но это не значит, что вычисление хеш-функции удовлетворяет потребности природного "сигнализирующего" механизма, который мы обсуждали ранее. Потому в данном случае верификация — это просто пересчет, а значит, это дешево; и точка. Для того, чтобы новая "функция” **H***, взяла на себя роль сигнализирующего механизма, на смену существующей хеш-функции **H**, она должна быть:

- непредсказуема на выходе, учитывая ее входные данные;
- не только непредсказуемой по своему выходу, но и фактически (детерминировано) случайной;
- требовательной к тому, чтобы на выходе была особая форма с низкой энтропией.

(странная фраза 'детерминировано случайный' происходит от того, что это является полноценной функцией: даже если выход 'выглядит случайным', вы все равно получите один и тот же выход для одного и того же входа; всегда).

Если подумать, то наша H*, в основе которой лежит криптографическая хеш-функция H, удовлетворит первые два пункта выше только благодаря свойствам H. Но, добавив, последнее требование, мы получим, в общем, что-то очень похожее на первые четыре пункта выше в разделе о "современном человеческом обществе"; именно из-за этого дополнительного требования "низкой энтропии". (Для не физиков: представьте "низкую энтропию" как "высокую степень структуры или симметрии", имеющую хоть какое-то отношение к красоте или эстетике).

Таким образом, в итоге, требование низкой энтропии на выходе из хеш-функции приводит к _дорогостоящему сигналу, который очень однозначен и легко проверяется_ — даже если _содержание_ этого сигнала само по себе совершенно бессмысленно.

Именно эту функцию и выполняет алгоритм Биткоина Proof of Work:  

{{% image "/img/pow-620.png" /%}}

Большинство читателей, вероятно, уже знают, но для полноты картины сообщу: странно, что в этих длинных шестнадцатеричных строках есть "много ведущих нулей", что на самом деле просто указывает на то, что значение этого целого числа намного меньше максимального возможного значения, и вероятность подбора подобного числа крайне низка. Суть в том, что этот вывод H* требует триллионов (на самом деле гораздо больше, но не суть) вычислений лежащих в основе хеш-функции (SHA256) H, с подавляюще высокой вероятностью.

Раз уж мы заговорили на эту тему, давайте обратимся к постоянно вызывающему отвращение "решению сверхъестественных/сложных математических задач", которым поясняют механизм работы протокола в не самых познавательных статьях о Биткоине. Глубокая причина, по которой это неверно, не в том, что вычисляется точная конструкция хеш-функции, а в том, что вычисления по своей природе случайны; вся внутренняя структура является артефактом, именно поэтому мы предпочитаем сравнение с лотереей, а не с "математической проблемой". К сожалению, это, как правило, не достигает адресатов и любопытные умы, несомненно, оказываются в замешательстве: “Каким образом этот “Биткоин” до сих пор здесь ...

Создание этих хешей представляет собой своего рода **опредмечивание информации**. Нули в приведенном выше дайджесте хешей — это всего лишь шаблон. Но в этом шаблоне скрыта реальная энергетическая сырьевая стоимость, которую можно количественно оценить (хотя, не забудьте о предостережении, представленном ниже).

В каком-то смысле вопрос моего друга детства был о различии между цифровым (бинарным?) и реальным мирами. Механизм, подобный PoW, связывает эти два мира. И я считаю, что он напоминает мост между жесткой физической реальностью, в которой обитает, например, павлин, и абстрактным/виртуальным царством сигналов, вовлеченном в его брачные ритуалы. В конкурентной среде, в которой есть что терять, разделение "реального" и "фальшивого" означает идентификацию объективных сигналов. А единственными объективными сигналами являются те, которые **очевидно дорогостоящи**.

Доказательство наличия рабочих хешей очевидно дорого (технически это только статистически верно, но в подавляющем большинстве случаев применяется закон больших чисел). Они не просто аналогичны ранее упомянутым примерам из природы и человеческого общества (наподобие выдающихся зданий или обручальных колец), но и намного лучше, потому что стоимость проверки их валидности намного ниже стоимости их производства (учтите стоимость оценки бриллианта в кольце, поразмыслите о крайней субъективности оценки военной мощи нации и о возможных масштабах сопутствующих затрат).

Оговорка: реальная энергетическая стоимость хешей Proof of Work в реальном мире является переменной, которую на самом деле непросто измерить. Это лишь оттягивает PoW несколько назад, как бы приравнивая его к некоторым другим упомянутым примерам; если взглянуть в целом, то он значительно превосходит другие сигналы, по крайней мере, если представить, что PoW функционирует в глобальном масштабе, как это происходит сегодня в случае с Биткоином (так что стоимость подвержена значительным рыночным силам).

# Что заменяет Proof of Work?

Раз мы разобрались с возможными биологическими и техническими диверсиями, давайте вернемся к идее судов, справедливости и насилия.

Хотя система, подобная Биткоину, не может заменить большинство общественных структур, она пытается изменить саму функцию создания денег (это спорно, но большинство согласно с этой точкой зрения) и их перевода (бесспорно; в противном случае она бессмысленна). Для того чтобы добиться успеха в последнем, Биткоину необходимо разрешить конфликты, которые неизбежны в конкурентной среде. Для этого необходим арбитр, настолько нейтральный, насколько это возможно (при этом многие часто забывают, что эта модель не приводит волшебным образом к "идеальной справедливости", если ее правильно не контекстуализировать: майнеры могут формировать блоки как им заблагорассудится, поэтому не забывайте, что вы находитесь на Диком Западе, и ваш платеж может быть заменен другим), а функция PoW обеспечивает справедливость, основанную на объективном, легко проверяемом, очень дорогостоящем сигнале.

Давайте еще раз вернемся к нашему списку свойств "хороших сигналов":

- дорогостоящие в производстве;
- привлекают внимание;
- (визуально) значительно отличаются от обычных "предметов" в окружающей среде;
- очень быстро и легко распознаются _любым_ наблюдающим, _без необходимости в дополнительном оборудовании_;
- сообщают о том, что создатель является частью группы (генетической или культурной).

На стоимости (пункт 1) был сделан значительный акцент, но помните о четвертом пункте: независимая, объективная и легкая проверка сигналов имеет первостепенное значение. В человеческой правовой системе все основывается на контексте — обратите внимание, например, на [прецедентное право](https://dic.academic.ru/dic.nsf/ruwiki/1105918) — явление считается верным, если оно отсылает к другому явлению. Это практично и логично, потому что внутренняя природа таких систем правосудия субъективна — договоры пишутся на человеческом языке, а этика, по крайней мере, по существу (если не полностью) является конвенцией — даже когда законы согласованы законодателями, вопрос толкования остается открытым... Так что в целом все, относящееся к праву, тоже субъективно.

{{% image "/img/pow-621.png" /%}}

Это не значит, что попытки сделать правовые системы более объективными бесполезны. Это вовсе не так — взгляните, к примеру, на концепцию [судебной независимости](https://ru.qaz.wiki/wiki/Judicial_independence), которая является чрезвычайно важным элементом цивилизации. Но, опять же, не забывайте обо "всем том доверии, необходимом для того, чтобы это сработало".

> _(Внимание: личное мнение)_ Философия, стоящая в основе Биткоина, не обязательно является анархизмом в какой-либо конкретной форме, даже если многие анархисты поддерживают Биткоин. Философия заключается в том, чтобы просто сделать деньги независимыми от контроля человека, ведь денежная система **может** обрести независимость от человеческого контроля при наличии сильной криптографии и механизма сигнализирования Proof of Work.

Если вы согласны с тем, что это, по крайней мере, возможно, стоит задуматься о более глубоком смысле, заложенном в алгоритм Proof of Work и почему, и в какой степени он является значимой составляющей при создании подобной формы денег.

Итак, если у вас имеется такой независимый от контекста механизм "опредмечивания информации", то у вас есть способ выстроить фиксированную уникальную "временнýю шкалу истины" — последовательность транзакций, перемещающих деньги из пункта А в пункт Б, которую каждый, по сути, может с легкостью проверить, и которая, очевидно, дорогостояща для создания. Затраченная ценность представляет собой уровень защищенности средств каждого участника сети — поддержание динамично растущего реестра требует значительных энергозатрат, а не просто изменения мнения других участников или иных субъективных рамок (как в случае с правовыми системами, или системами голосования, или чем-либо, в основе чего лежат социальные соглашения).

Значит ли это, что Proof of Work заменит банкоматы и банковских кассиров, как некоторые утверждают? Надеюсь, это вызовет соответствующую реакцию. Сравнение стоимости PoW с подобными затратами невероятно ошибочно, не столько потому, что это абсолютно не связано, сколько потому, что это довольно тривиальная стоимость по сравнению с тем, что на самом деле имеет значение!

Сравнивайте стоимость банковских операции со стоимостью огромного небоскреба, построенного в Гонконге или на Манхэттене. Вы обретаете доверие за счет "веса” и "реальности", за счет вещей, которые нелегко скопировать, отменить или иным образом обратить. Вот почему, как уже упоминалось ранее, называть Биткоин "виртуальной валютой" попросту глупо.  

"Какая валюта выглядит более виртуальной — та, чей запас можно удвоить в одночасье одним росчерком пера, или та, которая требует миллионы долларов электроэнергии для создания 25 новых единиц?"  

Надеюсь, суть ясна; современная фиатная валюта является абсолютно виртуальной, независимо от того, напечатана она на бумаге или нет.

Продолжая эту мысль, могут ли вооруженные силы заменить PoW в качестве сигнала?

{{% image "/img/pow-622.png" /%}}

Я думаю, что это нетривиальный вопрос, и он, вероятно, связан с разграничением, которое я сделал ранее, в сфере биологии: иногда сигналы о пригодности к спариванию демонстрируют потенциал насилия, иногда потенциал сбора ресурсов. Назначение армии, как и любого другого оружия национального государства — это не обеспечение валюты, а в первую очередь конкуренция с другими государствами за ресурсы, такие вещи, как подавление восстаний/революций/политического инакомыслия (в некоторых авторитарных государствах), применение силы с целью налогообложения, разрешение масштабных споров и т.п. Поэтому я не думаю, что ценность Биткоина следует сравнивать со стоимостью американских военных, например, но вы все же можете попытаться провести параллель (хотя это чистой воды спекуляция). Помимо этого не стоит забывать о правовой системе; опять же, Биткоин на заменит правовые функции, но можно заметить достаточно общих функций, чтобы принять это во внимание. Это не такой уж и простой вопрос :)

# Оправданы ли все эти “излишние” расходы?

Дискуссия о том, является ли PoW расточительным, тесно связана с вопросом о том, какова его цель, о чём и шла речь в предыдущих разделах.

Пожалуйста, поймите, что многие и правда задают этот вопрос искренне, но по своей природе ожидают определенного ответа: они совсем не понимают для чего предназначен PoW (см. "сложные математические задачи", приведенные выше), и поэтому для них практически очевидно, что этот алгоритм слишком расточителен; они просто хотят в этом убедится. Если вы хотите получить толковый ответ, просто скажите следующее:

> "Расточительны ли рога оленя? Расточителен ли хвост павлина? Если ты ответишь на эти вопросы, я отвечу на твои"

В любом случае, если вы согласны с предыдущим разделом ("Что заменяет Proof of Work?"), то мы можем обсудить это подробнее. Самыми большими потребителями энергии обычно являются военные (что неудивительно); бюрократия в целом также выступает в качестве эффективного потребителя энергии. Сравнение энергопотребления Биткоина со всеми составляющими инфраструктуры, которые он может заменить вовсе нелегко (в третий раз вспомним фразу "все то доверие, необходимое для того, чтобы это заработало": за доверие приходится платить энергией).

Добавляет ли ценности тот факт, что использование энергии биткоина более "взаимозаменяемо"? Я использую этот термин довольно свободно — я имею в виду, что биткоин может преобразовывать любую форму энергии вне зависимости от местоположения, что не характерно для большинства видов использования энергии в обществе, и энергия, за исключением нефти, печально известна своей плохой транспортабельностью. Я думаю, что это так, но я бы не стал преувеличивать. Точно так же верно и то, что Биткоин “отбирает” часть электроэнергии, созданной, к примеру, с помощью гидроэлектростанций. При этом, он стимулирует инновации в технологии преобразования энергии (см. недавние [инициативы](https://decrypt.co/41618/there-will-be-bitcoin-oil-gas-cash-cow-our-feet) по использованию сжигаемого природного газа).

Но эти аргументы скорее дополняют, чем выступают в качестве основы — они не будут и не должны убеждать скептика. Ключевой момент заключается в том, чтобы понять (а) что PoW на самом деле выполняет полезную функцию; если вы не видите этого и думаете, что это бессмысленно и глупо, то, конечно, даже 1 МВт, потраченный на использование данного алгоритма, будет катастрофой, и (б) что нет никакой пользы в оценке ситуации с точки зрения сокращения потребления энергии — в долгосрочной перспективе для человеческого рода это не будет иметь значения (осознать возможные масштабы развития криптовалют и финансов в частности и человечества в целом поможет данная серия эссе: [[1](/ba/1)] [[2](/ba/2)] [[3](/ba/3)]).

# Сигналы в джунглях против сигналов в лаборатории

Помните нашу маленькую птичку в поисках партнера в джунглях? Ее проблема была не в том, чтобы отличить сигнал с определенным значением, а в том, чтобы найти сигнал вообще, и чтобы он был "настоящим" в том смысле, в котором мы только что разобрались, и не было бы необходимости полагаться на дополнительные данные. Но здесь я хочу подчеркнуть слово "джунгли". По сути, в обществе большинство стремится получить любую возможную выгоду, любым способом. Это особенно верно в городской среде, а теперь и в интернете, где мы уже существенно превзошли [число Данбара](https://ru.wikipedia.org/wiki/%D0%A7%D0%B8%D1%81%D0%BB%D0%BE_%D0%94%D0%B0%D0%BD%D0%B1%D0%B0%D1%80%D0%B0):  

{{% image "/img/pow-623.png" %}}
[https://hard-life.kz/uploads/posts/2019-07/1563114259_11.jpg](https://hard-life.kz/uploads/posts/2019-07/1563114259_11.jpg)
{{% /image %}}

...а это значит, что разумным компромиссом для многих станет отказ от этических принципов с целью попытки обмана первого встречного незнакомца. В принципе, особенно когда речь идет о деньгах, стоит предполагать, что мы находимся в среде, которая:

- Очень враждебна
- Полна нерелевантной информации

Это относится к P2P сетям, к социальным сетям, к программным стекам, и, конечно же, к блокчейну, претендующему на звание средсва сбережения!

Люди обычно пытаются решить эти проблемы, возвращаясь к моделям, основанным на доверии. Они используют системы, которым доверяют, потому что знают их создателей (те, кто помнит ICO-бум 2017-го, не забудут уморительный шум вокруг лиц на веб-сайтах,

{{% image "/img/pow-624.png" /%}}

... включая добавление знаменитостей, ничего не знающих о криптовалютах в качестве участников проекта) или по какой-то причине надеются, что система каким-то образом поведет себя предсказуемо. Это все звучит прекрасно, но, по сути, в контексте Биткоина это сродни поднятию белого флага. Мы пытаемся построить систему, которая действительно может выжить в контексте двух вышеперечисленных пунктов, а не ту, что отступит из джунглей и продолжит свое существование в лабораторных условиях.

История богата на попытки создания системы, решающей проблему достижения консенсуса "в лаборатории", но участники данных экспериментов не думали столь радикально. Взгляните, например, на [задачу византийских генералов](https://ru.wikipedia.org/wiki/%D0%97%D0%B0%D0%B4%D0%B0%D1%87%D0%B0_%D0%B2%D0%B8%D0%B7%D0%B0%D0%BD%D1%82%D0%B8%D0%B9%D1%81%D0%BA%D0%B8%D1%85_%D0%B3%D0%B5%D0%BD%D0%B5%D1%80%D0%B0%D0%BB%D0%BE%D0%B2) — вопрос, изучением которого занимались задолго до появления криптовалют. Она рассматривает варианты развития событий в случае, если некоторые члены группы, пытаясь сохранить последовательность в каком-то состоянии, потерпят неудачу или откажутся следовать решению остальных участников. Любопытно то, что некоторые из самых ранних результатов в этой области заканчивались чем-то смутным по принципу "не более 1/3 нечестных лиц"; это, вероятно, происходит из-за того, что это порог, при котором на каждого нечестного участника приходится два честных. Помня о том, что мы рассматриваем распределенные системы, наличие двух хороших на одного плохого позволило бы достичь консенсуса.

Но обратите внимание: эти размышления основаны на "наборе действующих лиц", но идея PoW вне лабораторных условий заключается в том, чтобы функционировать вне подобных рамок: мы строим систему, в которой нет понятия “идентификация”. Мы не можем и не хотим позволить, чтобы Биткоин учитывал тот или иной набор сущностей, которые находятся в "кворуме" с целью принятия решений. На самом деле, в Биткоине нет механизма для группового принятия решений, потому что здесь нет никаких групп. Процитируем вайтпейпер Биткоина:

Сильной стороной сети является простота ее структуры. Все узлы работают самостоятельно, иногда обмениваясь информацией. Нет необходимости в идентификации, поскольку сообщения не идут по какому-то определенному маршруту, а основаны на принципе «наименьших затрат». Узлы могут покидать сеть и вновь подключаться, принимая самую длинную цепочку блоков как подтверждение пропущенной истории транзакций.

Последнее высказывание указывает на то, что отсутствие необходимости в постоянном присутствии, является прямым результатом "опредмечивания информации". Вы не можете добиться подобного через кворум, потому что это возвращает вас к субъективному принятию решений. Правила Биткоина — просто "воля народа", и именно поэтому изменить их должно быть и очень просто, и чрезвычайно сложно. Тем не менее, история Биткоина не является "волей народа", она пишется дорогостоящим, и намеренно бессмысленным трудом.

# Proof of Stake

Попытки заново изобрести Биткоин с использованием алгоритма [доказательства доли владения](https://ru.wikipedia.org/wiki/%D0%94%D0%BE%D0%BA%D0%B0%D0%B7%D0%B0%D1%82%D0%B5%D0%BB%D1%8C%D1%81%D1%82%D0%B2%D0%BE_%D0%B4%D0%BE%D0%BB%D0%B8_%D0%B2%D0%BB%D0%B0%D0%B4%D0%B5%D0%BD%D0%B8%D1%8F) (Proof-of-Stake / PoS) вместо PoW в конечном итоге попадают в категорию "лаборатория" выше. Предположив существующие наборы участников (которые, конечно, могут меняться, но все же..), можно создать все более сложные системы кворума; но они опираются на контекст, т.е. в отсутствие механизма "опредмечивания" они по своей природе субъективны. Подобные модели будут работать в определенных контекстах, но не в реальном мире, не в джунглях; они могут работать, если предполагается некоторая активность (отчасти наподобие [сети лайтнинг](/lightning), которая может получить кучу дополнительных полезных свойств, но требует большей активности (и полагается на лежащий в основе блокчейн). Обратите внимание, что более современные попытки проектирования PoS, по крайней мере, пытались рассмотреть тип рассуждений рассмотренный в данном эссе. В частности, они обращались к концепции гандикапа — помните наше "что вы не сделали, делая это"? В случае с наивным PoS ответа на этот вопрос попросту нет, что рождает собой ироническое высказывание "ничто на кону", что означает, что участник может выбрать существование в нескольких реальностях одновременно, без (или с невероятно низким уровнем) затрат. В менее наивных попытках, освещенных в [данном](https://eth.wiki/concepts/proof-of-stake-faqs) документе, в разделе “What is “nothing at stake” _("Что такое "ничего на кону...")_, наглядно и подробно рассматривается ряд релевантных вопросов ( я настоятельно рекомендую ознакомится с документом), вплоть до:

Логика заключается в том, что мы можем повторить экономику PoW при использовании алгоритма PoS. В случае с PoW, недоброжелатель может получить штраф за создание блока, не следующего правилам консенсуса, но этот штраф имеет место в реальном мире: майнеры вынуждены тратить электричество и приобретать или арендовать специализированное оборудование. В PoS штрафы имеют место лишь внутри соответствующей сети.

В целом я не согласен с озвученной точкой зрения: нельзя воспроизводить экономику "опредмечивания информации" путем симуляции; потому что ценность остается внутри симуляции.

Вы, конечно, можете установить некую базовую истину за пределами симуляции; и использовать ее в качестве исходной точки.

Если вы требуете, более критичных выводов, я могу порекомендовать [работу](https://download.wpsoftware.net/bitcoin/alts.pdf) Поельстры о PoS, см. раздел 6.4, а также более экономически ориентированный анализ от Sztorc [здесь](https://www.truthcoin.info/blog/pow-cheapest/).

В лучшем случае, современные попытки создать подобные системы — это просто совершенствование ранее существовавших механизмов поиска консенсуса. В худшем случае они будут деградировать в одном из двух направлений: либо в сторону запутанных PoW, либо (скорее) в сторону все более фиксированного набора собственников/”стейкеров” (см.: [эффект Матфея](https://ru.wikipedia.org/wiki/%D0%AD%D1%84%D1%84%D0%B5%D0%BA%D1%82_%D0%9C%D0%B0%D1%82%D1%84%D0%B5%D1%8F)), которые получают возможность решать споры в свою пользу. Также примечательно и, возможно, показательно, что они предполагают наличие механизма изначального распределения прав собственности на монеты, в чем нет необходимости при использовании PoW.
