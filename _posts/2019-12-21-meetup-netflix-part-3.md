---
layout: post
title: Meetup. Об IT без галстуков. Встреча с инженером Netflix, беседа о ДНК компании и о секретах ее успеха. Часть 3
image: /img/previews/meetup_netflix_p3.jpg
tags: [netflix, culture, meetup, recruitment, freedom, responsibility, hr, salary, life in usa]
---

Сегодня третья часть оцифровки нашего митапа с Арсеном Костенко из Netflix. Напомню, что сама встреча
прошла 10 ноября, и собралось 120 человек.

Тем, кто не читал [первую часть]({{ site.baseurl }}{% link _posts/2019-11-27-meetup-netflix-part-1.md %}) или
[вторую часть]({{ site.baseurl }}{% link _posts/2019-12-11-meetup-netflix-part-2.md %}) рекомендую
начать с нее. В первой части шла речь о собеседованиях, найме, доходе, акциях, опционах, и затронули культуру компании,
которая умещается в двух словах: freedom & responsibility. Во второй части продолжаем о культуре,
вкладе менеджеров и разработчиков в общее дело, SLA, Agile, self-management, организации
команд и межкомандного взаимодействия, личных планах развития и DevOps.

В этой части речь пойдет о:

* снова и снова о культуре в Netflix;
* тестировании;
* передаче знаний;
* дежурствах и SLA;
* о том для кого что явялется успехом;
* продолжительности жизни в компании и возрасте сотрудников;
* об иммиграции и будующем отечества.

В конце этой статьи ссылки на наши контактные данные. Те, кто уверен в своих силах, могут запросить reference check
у Арсена.

> Оцифрованная версия **для чтения на русском языке**, но те, кто понимают **украинский**, могут **посмотреть видео**.
2 часа 17 минут, правда, но на прочтение текста ниже потребуется 10-15 минут.

> <iframe width="560" height="315" src="https://www.youtube.com/embed/1so_s4y6b54" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

Поехали! **ДМ** - это я, **АК** - это Арсен Костенко. **Зал** - это зал) Кстати, прежде чем начнем, большое спасибо
Ксюше Иващенко, она делала оцифровку этой части, спасибо, Ксю! Начнем сразу с вопроса зала!

**Зал**: Делегировал ли ты свои обязанности или свою кодовую базу кому-то в Netflix? Передавал ли свои наработки по CI/CD кому-то?

**АК**: Нет, пока нет. Возможно, в какой-то момент, если кто-то другой захочет ими пользоваться, я это сделаю. Но пока нет.

**ДМ**: Ещё 2 вопроса, и перейдём к другим поинтам.

**Зал**: Спасибо, очень интересно про культуру, и ты повторил несколько раз про самый главный принцип – freedom & responsibility. Это очень круто, они наверное делают крутую работу по культуре. Поделись, как ты думаешь, почему этот принцип так важен для Netflix? Что это даёт?

**АК**: Я думаю, что лучше всего на этот вопрос ответил бы Рид Хейстингс (смех зала), это СЕО компании, он с этими ценностями намного дольше живёт, он видел развитие компании намного лучше, и т.д. Для меня, как для программиста, видно такое интересное последствие – я начинаю балансировать между работой, которую делаю и тем, как много времени я буду тратить на поддержку этого всего. Я намного больше внимания обращаю на аспект DevOps. Насколько легко мне потом будет работать с сервисами. Я намного больше включаюсь в то, каким я хочу видеть этот сервис, потому что потом ко мне же и "прилетит". 

**Зал**: Ты говорил, что Netflix это компания, в которой ты специалист. Можешь ли ты привести примеры из своей практики, когда ты чувствовал, что имеешь это влияние? 

**АК**: Ну, наверное я ещё конкретно до этого не дорос, но примеры влияния Netflix на индустрию – например, в сфере энкодинга, есть два элемента, которые мне нравятся: AV1 – новый кодек, который в том числе сделан при участии Netflix, и VMAF – это субъективная метрика оценки качества изображения, которая была сделана полностью Netflix. 

**Зал**: А эта информация где-то есть?

**АК**: Да, это open source. 

**ДМ**: Кстати, есть свежий конкурент, из лаборатории Фраунгофера, сделал с видео такое – было SSIM, а они сделали 3SSIM, но для бедных. А у вас есть в open source эти вещи?

**АК**: Ну, у Netflix есть целое подразделение – Netflix OSS, вы там можете посмотреть всё, что Netflix заоупенсорсил. В том числе там есть VMAF, и AV1, в принципе, создан как open source кодек с самого начала. 

**ДМ**: Тут был интересный вопрос, встречался ли ты с инженерами Netflix, которые, что называется, работают из-под палки? Их как-то отфильтровывают или они ровно сидят, получают деньги и всё?

**АК**: Я даже не знаю, как на это ответить. 

**ДМ**: Встречал или нет?

**АК**: Нет.

**ДМ**: Это довольно интересно. А как ты думаешь, что вообще с ними происходит? (смех зала)

**АК**: Когда я встречу, я спрошу.

**ДМ**: Это будет интересно, расскажешь потом.

**АК**: Обязательно.

![Meetup Photo 6]({{ "/img/meetup_netflix/photo_6.jpg" | absolute_url }}){: .in-post-img-center .in-post-img-border}

**ДМ**: Так, давай ещё немного о технической стороне поговорим. Про code review тесты, профайлинг, debugging на продакшене или нет. Работа с проблемами и эскалация. Давай начнём с code review, мы с тобой уже проговаривали фишки про code review. Я уже знаю, что ты можешь пригласить другого человека сделать code review для тебя, но обязательной практики нет. 

**АК**: Мы опять же возвращаемся к этому основному моменту – freedom & responsibility. Если наша команда достаточно уверена в том, что она может функционировать так, она может функционировать так. Это правила, которые существуют для меня, которые поддерживаются моей командой, и я подозреваю, что могут быть команды, в которых другие правила. 

**ДМ**: То же самое, наверное, касается и тестов? Если ты и команда понимаете, что вам не нужны тесты, что вы с первого раза можете написать качественный продукт, то ты не будешь писать тесты?

**АК**: Мне уже 37, я уже не верю, что могу пилить качественный продукт. Поэтому я пишу много тестов, и единственное, что меня расстраивает в тестах это то, что они у меня выполняются дольше, чем весь остальной build, и это время возрастает. Поэтому я очень люблю нашу build команду – когда они скорость выполнения тестов снижают на 10 минут, это просто супер. 

**ДМ**: А у вас прям CI/CD происходит в процессе с тестированием?

**АК**: Есть классическая пирамида тестирования, которую мы, например, приняли, и мне она очень нравится. Это огромное количество unit тестов, которые оформляются локально, потом некоторые smoke тесты, потом какое-то количество интеграционных тестов, и всё. А, и потом мы ещё иногда делаем load тесты на всю систему. 

**ДМ**: А мутационные тесты?

**АК**: Ты имеешь в виду хаос? У нас есть команда, которая управляет хаосом, и они это проводят. Если я буду проводить сам свой хаос, он превратится в неконтролируемый хаос, а это не совсем то, к чему ты хочешь подготовиться. 

**ДМ**: А можешь немного рассказать об этом не контролируемом хаосе? Что это такое и как это использовать эффективно? 

**АК**: Во-первых, если вы загуглите chaos monkey или просто chaos, то вы увидите много интересных статей на блоге Нетфликс о том, как мы это делаем, и технические детали. В общем это сводится к тому, что в любом микросервисе, в их Amazon image, есть запаянный небольшой sidecar, который запускается, и может при желании этот сервис опустить или обрубить ему сеть, или ещё что-то типа того, и потом посмотреть, насколько легко эта система справляется с такого рода вещами. 

**ДМ**: А какие-то load тесты вы проводите или нет?

**АК**: Моя конкретная команда да, проводит. 

**ДМ**: Как это происходит?

**АК**: У нас есть выделенный стек, куда мы деплоим наши инстансы, у нас есть определённое время, когда мы запускаем нами же написанный load framework, который начинает валить с определёнными характеристиками, определенным уровнем нагрузки.

**ДМ**: Пытаетесь ли вы сделать такие тесты более похожими на реальных пользователей? Паттерны, которые пользователи системы могут демонстрировать? Даже если это система внутри самого Netflix.

**АК**: Да, но мы стараемся сделать более агрессивное тестирование, чтобы иметь гарантии определенного уровня. Мы не пытаемся воссоздать то, что уже есть, потому что оно у нас и так уже есть. Мы пытаемся умножить это на Х для того, чтобы знать, где наша грань, как далеко мы можем зайти без того, чтобы упасть.

**ДМ**: А деградацию вы как-то фиксируете?

**АК**: Целью всего load тестирования и есть фиксирование деградации. 

**ДМ**: А если есть какой-то минимальный SLA, а оно деградирует, но не переходит грань SLA?

**АК**: Мы счастливчики.

**ДМ**: То есть, SLA является критерием?

**АК**: Да, но это не SLA, который запущен сверху, или не SLA, который навязан нам пользователями. Это SLA, к которому мы стремимся для того, чтобы спать спокойно. Для того, чтобы знать, что сейчас пользователи валят вот с такой скоростью, с такой нагрузкой, а мы можем выдержать в -надцать раз больше. Очень маловероятно, что сегодня build свалится.

**ДМ**: У нас остаётся 15 минут на нетворкинг. Был вопрос про фулстеков и про языки программирования. Есть ли такая культура, как у Booking.com, где компания набирает программистов, которые могут программировать на разных языках, имеют нерелевантный стек, но потом их обучают 2-3 месяца и говорят, что если ты senior инженер, то ты можешь писать на чём угодно, и тебе без разницы, на чём писать? Тебе нужно решать оптимально задачи.

**АК**: Я к этому постоянно возвращаюсь – свобода и ответственность. Человек нанимается командой, со мной проводят собеседование не какие-то абстрактные люди из всей компании, со мной проводит собеседование моя команда. Они меня нанимают, и у них есть видение того, какой у них стек и что они будут делать. Я могу с этим не согласиться, но, если я не соглашаюсь, мы коммуницируем некоторым образом - мы же всё-таки ожидаем, что на это необходимо выделить столько то времени, и к этому моменту мы будет иметь уже готовую систему. Если я вдруг буду использовать какой-то другой стек, успею ли я сделать всё, что нужно, будет ли мой сервис вообще иметь метрики, успею ли я позаботиться о его scaling, успею ли я позаботиться ещё о многих вещах? Теоретически я мог бы сказать, что я использую другой язык программирования, и всё напишу с нуля по-новому, но всё, на что я трачу время, это дополнительная стоимость. Я не хочу париться о том, как собираются логи, как собираются метрики, как посылаются алерты в сервис, как происходит его scaling, и всё такое. Поэтому в основном я беру то, что предлагают мне другие команды. Например, есть команда, которая занимается поддержкой jvm на наших Amazon instances. И, если я беру их jvmку, и начинаю ей пользоваться, моя жизнь становится на порядок легче. И да, у человека есть свобода прийти и сказать: “Я буду использовать язык программирования Х”, если при этом всём человек может адекватно сам заменить работу всех других команд, и работать эффективно с другими своими сотрудниками. Я пошёл путём, когда я максимально отдаю всё, что могу отдать, и максимально пользуюсь готовыми коробочными решениями для себя, а сам фокусируюсь на бизнес части своего сервиса. 

**ДМ**: Это, кстати, очень отличается от модели, которая, к сожалению, существует в Украине, потому что много команд начинают распадаться на этапе детализации того, как использовать пробелы или табы, чтобы выравнивать код. То есть, это реальные проблемы.

**АК**: Я обожаю это (смех зала). Это три разные вещи – есть кнопочка, которую ты нажимаешь, есть что-то, что ты видишь на экране, и есть bit, который записывается на диск. Мы можем так наконфигурировать наши IDE, чтобы было три пробела, вставлялся табик и вставлялось визуально вот столько то расстояния, или наоборот, если мы начнём говорить о том, что я хочу, чтобы код выглядел одинаково у всех, современные IDE могут взять любой код и форматировать его так, как вам выгодно. 

**ДМ**: Ну, тут уже начинается дедовщина, что называется. Каждый говорит: “Я хочу, чтобы тут было 2 пробела, а я хочу, чтобы 4”.

**АК**: Конечно, но если речь идёт о виде кода, то ты можешь наконфигурировать IDE так, чтобы оно выглядело для тебя будто там два пробела. 

**ДМ**: Ну это такой, простой кейс (смех зала) А сложные – например, делать переносы или нет в каких-то массивах?

**АК**: Ты не поверишь, что эти чуваки из Eclipse и Jet Brains могут сейчас сделать, это просто феноменально. 

**ДМ**: Кто-то такое использует вообще? Именно визуальную часть?

**Зал**: Схемку в git, вся команда её “apply”, и у всех одинаково выглядит. 

**ДМ**: В контексте того, что обратно распаковать, и показать, что там 2 пробела, а мне показывает, как 4.

![Meetup Photo 7]({{ "/img/meetup_netflix/photo_7.jpg" | absolute_url }}){: .in-post-img-center .in-post-img-border}

**Зал**: Если ты смог трансформировать в одну сторону, значит сможешь и в другую, это не односторонний процесс. 

**Зал**: Вы рассказывали про свой код, что вы делаете свой CI/CD. А как с шерингом знаний, когда, кроме вас, из команды кто-то тоже должен это поддерживать, если вы оставите команду?

**АК**: То есть, вопрос в том, что делать с шерингом знаний, когда человек уходит из команды? 

**Зал**: Да.

**АК**: Это сложный вопрос, на него нет ответа. То есть, у меня нет на него уникального ответа, который мне самому бы нравился. Всё сводится к тому, что вы пытаетесь уловить эти знания, пока человек есть, и не откладывать это на последний момент. По крайней мере, я для себя выработал такую практику, она мне помогает больше, чем knowledge transfer в последний момент. Где-то 2 раза в моей жизни ко мне обращались постфактум с предыдущей компании типа “а ты не можешь нам сказать пароль” или что-то ещё. А в середине самой компании, если у вас сохранились нормальные отношения, ничего не мешает позвать человека на кофе и сказать “Слушай, помоги, подскажи, куда смотреть”. 

**Зал**: У меня есть вопрос относительно поддержки,. Насколько я понял, у вас всё строится так, что каждая команда делает свой сервис или несколько сервисов, и пытается интегрировать его в работу других сервисов. Но что случается, если эти сервисы сбоят? Как вы ловите какие-то алерты? Есть какие-то дежурные?

**АК**: Да, всё, что ты сказал, работает. Есть такой чудесный сервис PagerDuty, есть команда, которая строит сервисы алертов, они поддерживают этот PagerDuty. Присоединить к нему команду просто, и присоединить его к определённому алерту просто. Дальше команда сама решает, какие алерты ей нужны для того, чтобы она не блокировала работу других команд. То есть, мы можем повесить эта алерты на что угодно. Мы решили, что мы будем вешать их на те, те и те метрики, потому что они больше всего коррелируют с теми сбоями, которые сильно мешают другой команде. Поэтому, когда в этих метриках начинается какая-то деградация, нам всем приходит уведомление о том, что сейчас происходит что-то плохое. Очень часто это сообщение приходит на команду, а у команды есть расписание ротаций, когда кто-то один, диспетчер, принимает это первое сообщение, и они решают, что делать с этим дальше – посмотреть самим или отправить дальше.  

**Зал**: То есть, грубо говоря, каждая команда решает, кто и когда будет ответственен за проблему? 

**АК**: Каждая команда сама решает, кто будет первым уровнем ответа, а ответственность за проблемы определяется уже по тому, что это за проблема. Иногда это бывают проблемы в каких-то других сервисах, которыми мы не пользуемся. Просто мы её поймали, а они не успели поймать, и мы начинаем коммуницировать с ними. 

**Зал**: Достаточно ли вам 4 человек для oncall?

**АК**: Работы всегда больше, чем людей. Пока что наш oncall мне очень нравится.   

**ДМ**: Давайте я задам 2 последних вопроса. Что по твоему мнению вообще мотивирует людей в компании? Почему они приходят в Нетфликс?

**АК**: Это философский вопрос, который неуместен. Мы разные люди, нас мотивируют разные вещи. Каждый приходит в ту или иную компанию со своими собственными амбициями, вопросами и выигрышами от того, что он обменивает своё время на деньги именно этой компании. То, что мотивировало меня, это очень индивидуальный специфический микс, но, что мотивирует людей в целом…

**ДМ**: Может существует какой-то паттерн, который ты видишь среди всех инженеров?

**АК**: Паттерн, который я вижу среди инженеров, это то, что у большинства моих коллег горят глаза, они с вдохновением рассказывают о том, что они делают.

**ДМ**: Круто. Финальный вопрос – почему Нетфликс такой успешный? 

**АК**: Ну, опять-таки, что такое успех?

**ДМ**: Давай начнём с инвесторов.

**АК**: Я не знаю, я программист (смех зала)

![Meetup Photo 8]({{ "/img/meetup_netflix/photo_8.jpg" | absolute_url }}){: .in-post-img-center .in-post-img-border}

**ДМ**: Но ты же видишь финансовые показатели?

**АК**: Ты их тоже видишь. Открываешь аппку, и там написано NFLX, цена качества.

**ДМ**: Ты сейчас говоришь об акциях?

**АК**: Ну, это способ взаимодействия с инвесторами. 

**ДМ**: Я мог бы многое сказать о том, почему нет, но…

**АК**: Ок, что такое успех?

**Зал**: Shareholders value.

**АК**: Ну, она выражается в цене акций, или я ошибаюсь? Если я прав, то, говоря о Нетфликсе, не обязательно меня приглашать сюда. Можно смотреть на то, что говорят инвесторы про Netflix и иметь свою точку зрения. Или я ошибаюсь?

**Зал**: Тут, наверное, больше про инженерную часть успеха.

**ДМ**: Ок, инженерная часть успеха: для кого-то это возможность иметь на себе бренд Netflix, для кого-то это возможность иметь влияние, для кого-то это возможность учиться, для кого-то – зарабатывать много денег. 

**Зал**: И почему именно в Netflix это так выражается в финансовом эквиваленте?

**АК**: А это не факт. То есть, люди приходят в Netflix, люди уходят из Netflix, есть люди, которые присоединяются, а есть те, которые меняют Нетфликс на какую-то другую компанию. Я не могу сказать, что это the Destination. 

**Зал**: То есть, в Netflix это никак не выражается в денежном эквиваленте?

**АК**: Сложный вопрос. Есть ли что-то, что отличает Netflix? Netflix лучший в медиа, чем большинство компаний в Долине, и Netflix лучший в технологиях, чем большинство компаний в Лос-Анджелесе. Но то ли это, что вам важно? Каждый решает для себя. 

**Зал**: А чем он лучше технологически?

**АК**: Например, потому, что он полностью на cloud. Мало компаний в Лос-Анджелесе полностью диджитализированы. Что мне нравится – technology first, компания, которая была рождена с технологиями. Компания, которая была создана для того, чтобы развлекать, делать entertainment, но при этом всём с четким пониманием технологий. Яркий пример для меня – Sony, львиная доля assets которых хранится на tapes, на кассетах, потому что на кассетах можно плотнее записать информацию, но это означает, что и считываться она будет дольше. Потом для того, чтобы показать ваш фильм, вам нужно его считать с кассеты, а у этого процесса могут быть и последствия, например, плохое считывание. И вы строите целый бизнес, чтобы ваши фильмы правильно считывались с кассет. Для меня, как для технаря, это довольно странная комбинация, а Sony в этом видит выгоду.

**ДМ**: Может инвесторы Sony видят результат, потому что намного дешевле хранить данные на tapes. 

**АК**: Да, тут начинается другой разговор, но мне, как человеку, который смотрит на это с точки зрения технологий, легче работать, когда физический аспект сохранения данных от меня абстрагирован.

**Зал**: А ещё что-нибудь?

**АК**: Ну, то, что они пионерят кодеки – это мега круто. Внедрение кодеков в жизнь это вообще отдельный разговор, потому что кодек лучше внедряется, когда у вас есть физический декодер на устройстве, а это означает, что вам нужно будет подождать 5 лет, пока этот декодер появится у всех, кому вы собираетесь этот фильм показывать, поэтому процесс довольно долгий. Но сама идея того, что люди этим парятся, что для них это важно, меня это очень вдохновляет. Я могу долго говорить о разных вещах, которые люди сделали в Нетфликсе, это не настолько громко и популярно звучит, как что-то, что люди делают в Фейсбуке и Гугле, но это уже вопрос коммуникации, пиара этих всех наработок.

**ДМ**: Нетфликс завязан на сервисы Amazon, и на другие технологии других компаний, и тут есть два момента. Во-первых, если вы находите баг в каких-то решениях Amazon, как вы контактируете? И второй момент – если Amazon завтра зачарджит Х2 для Netflix?

**АК**: Тогда мы спросим, что дальше делать. И на этот вопрос мы, как неглупые люди, найдём ответ. Это вопрос, с которым появляется бизнес, и с которым он живет постоянно. По поводу багов – как и у других клиентов Amazon, у нас есть способ позвонить им или написать и сказать об этом. Если это что-то критичное, то мы начинаем думать, как нам сделать так, чтобы эту критичность обойти. Если Amazon идёт навстречу, и говорит, что они это решат, мы счастливы.

**ДМ**: С чем в Netflix тебе не нравится мириться? Есть ли такое?

**АК**: Я уже не молодой и не горячий, я могу смириться со многим (смех зала)

**Зал**: Есть ли в Netflix те, кто работает 20 лет? И какая разница между теми, кто пришёл сейчас?

**АК**: Это всё вопрос роста. Если в компании возрастает количество людей, то появляется много тех, кто работает по полгода-год, и те, кто работает дольше, занимают меньшую часть – это логично. Есть люди, которые работают долго, но тех, кто работает 20 лет, я не видел. Но retention долгий. Большинство людей в моей компании работают 4-5 лет. В Твиттере я был где-то посредине, в Пинтересте – самый старший, а сейчас я чуть ли не самый младший.

**Зал**: То есть, там 45+?

**АК**: Я не могу сказать насчёт всей компании, но в моём случае они на 5-6 лет меня старше.

**Зал**: Это как-то помогает в восприятии принципа freedom & responsibility?

**АК**: Я думаю, что возраст плохо коррелирует с самосознанием. Но самосознание – ключевой момент. 

**ДМ**: Вопрос онлайн: куда ты можешь расти дальше после senior?

**АК**: Рост это не тайтл, рост это то, сколько человек мне доверяет, сколькими сервисами я оперирую, сколько людей ко мне прислушивается. Это leadership. Компания не занимается тем, чтобы построить вам план роста. Если у вас в голове есть план роста, компания может вам помочь и как-то сотрудничать для этого. Компания не пытается сделать из вас взрослого человека. Я взрослый человек, я знаю, чего я хочу, и у нас есть взаимодействие с компанией, когда я говорю: “Я хотел бы попробовать это и это”.

**Зал**: Вы описали процесс, когда Вы пришли в команду и стали с ней работать. А как происходит процесс зарождения нового сервиса и выделение команды для этого сервиса? 

**АК**: Процесс начинается с того, что команда видит какую-то необходимость, начинает что-то делать, потом сервис становится всё более популярным и используемым, и в итоге вырастает количество людей, которые это всё ведут вперёд. 

**Зал**: То есть, вы видите потребность, идёте к менеджеру и говорите: “Давайте я буду два дня в неделю работать над этой штукой”, а он соглашается или нет?

**АК**: Да, но это всё растянуто на более длительное время. Сначала мы предположили, решили посмотреть, “давай сделаем то”, и так далее.

**ДМ**: Вопрос онлайн: про будущее персонализированного контента. Довольно обширный вопрос. Не знаю, как несколькими предложениями на него ответить, но давай попробуем.

**АК**: Если рекомендации это контент, то оно уже есть. Если контент это именно то видео, которое я буду смотреть, то я не уверен, что мы всё время хотим смотреть что-то персонализированное. Например, я люблю смотреть на искусство, потому что кто-то другой вложил туда что-то своё, и мне интересно видеть это. Как с шутками – смеяться над своими неинтересно, а над чужими – прикольно, потому что они видят что-то такое, чего не вижу я. Моя субъективная точка зрения – полная персонализация контента будет выглядеть не так хайпово, как она звучит.

**Зал**: Как решаются спорные вопросы внутри команды? Например, выбор фреймворка для тестирования, внедрение какого-то процесса?

**АК**: Спасибо за вопрос. Я вернусь к фундаментальному принципу коммуникации – если вы уважаете друг друга, если вы доверяете друг другу, то вы понимаете, что вы работаете над одной общей целью, и что у вас есть желание построить что-то, что будет стабильным и будет выполнять поставленные задачи. Это сводится к технической аргументации. Если есть, например, 2 фреймворкера, которые одинаковые, но кому-то нравится один, а кому-то второй. Есть такая процедура “disagree and commit”, когда я говорю: “Мне это не нравится, но, поскольку большинство готово работать с этим, давайте работать с этим, чтобы двигаться вперёд”. Это техническое решение, с которым я готов жить.

**Зал**: Я хотел спросить о персонализации контента, точнее, его качества. Ты говорил про фреймворк VMAF, я немного прочитал об этом, там как раз используются AI модели, чтобы персонализировать качество контента.

**АК**: Я сделаю пару шагов назад – я говорил про VMAF, это метрика оценки качества изображения. Она не про персонализацию, и не про контент. Если мы снизим битрейт в два раза – насколько сильно человек увидит эту разницу? Если у нас есть мультик “Свинка Пеппа”, и мы снизим качество битрейта в два раза, никто не увидит, потому что он довольно эффективно кодируется. Но, если речь идёт об очень динамической сцене с супергероями, где есть зум на глаза и зрачки, мы меняем качество, и все это видят, потому что наше сознание больше всего воспринимает изменения в лицах – мы на это запрограммированы, мы это физически лучше воспринимаем. И этот VMAF пытается уловить качество восприятия, насколько качественно мы воспринимаем то или другое изображение. Персонализация тут не совсем уместна.

![Meetup Photo 9]({{ "/img/meetup_netflix/photo_5.jpg" | absolute_url }}){: .in-post-img-center .in-post-img-border}

**ДМ**: Последний вопрос онлайн: как вообще украинцу попасть в Netflix, что для этого нужно?

**АК**: У нас есть сайт – jobs.netflix.com. Вы находите позицию. Если у вас есть знакомые, например, вы можете написать мне, или другим знакомым украинцам в Netflix, и сказать “Ты не против меня зареферить?” Если вы общаетесь с этим человеком и вас знают, как специалиста, ваше резюме передадут дальше.

**Зал**: Что должно случиться в Украине, чтобы ты задумался вернуться сюда?  

**АК**: Я постоянно над этим задумываюсь. Это постоянный вопрос, который на фоне. Мне кажется, что у нас выработалось восприятие, что есть “мы”, а есть “они”. Чем меньше мы будем на этом концентрироваться, тем легче нам будет преодолевать этот ментальный барьер. Когда мы преодолеем его ментально, нам будет легче преодолеть его физически. Это работает в две стороны, то есть, такое же восприятие я вижу у людей, которые смотрят на диаспору. Грицак очень классно об этом говорит – ни одна европейская нация не была успешной без эмиграции. Ирландцы яркий тому пример. Голодоморы, выезды за границу, помощь диаспоры, и всё такое. Но, возвращаясь к твоему вопросу – что должно измениться в Украине? Мне кажется, чем больше есть понимания глобального рынка и того, как создавать глобальные продукты, тем легче вести разговор со всеми в Украине. Я вижу самую сильную сторону в IT, но что для этого нужно? Больше понимания, как создавать продукты, которые могут выходить на другие рынки, что такое рынок, что нужно людям.         

**Зал**: То есть, больше продуктовых компаний?

**АК**: Продуктовые компании это следствие того, что люди начинают понимать, что такое продукт.

**Зал**: То есть, глобальный контекст? Чтобы Украина стала частью глобального контекста, а не было мыльного пузыря, в котором мы живём сейчас?

**АК**: Мыльный пузырь это отдельный разговор. Сейчас это отдельный синдром – в Калифорнии свой мыльный пузырь, в Британии свой. Но, чем больше вы можете таких пузырей преодолеть, тем легче понимать, как вырастать в этом новом мире.

**Зал**: Спасибо тебе (аплодисменты)

**ДМ**: Спасибо тебе, что выделил время на это общение. Это очень круто для нас и поможет многим людям понять, как правильно строится структура компании, что деньги это не главное, и что product innovation и в общем мысли в контексте продукта и создания инноваций ведут компании, а не просто всё делается ради денег. Мы даже в рамках клубов, о которых я вспоминал вначале, пропагандируем идею, что Украине нужно больше продуктовых компаний, больше создавать value для наших компаний, не быть просто аутсорсом для всей остальной Европы. Нужно нарабатывать продуктовый бекграунд и создавать собственную ценность, а не быть экспортным ресурсом.

**АК**: Я не уверен, что я соглашусь со всем, что ты сказал. Мы можем обсуждать это ещё пару часов, но у меня нет времени. Но аутсорс это не плохо и не хорошо, он просто есть, и нужно с ним работать. Я вырос из аутсорса. Каждый из нас чувствует на себе влияние аутсорса, и это хорошо, мы должны принять это как своё положение дел, и с этим работать, и это использовать. У него есть сильная сторона, и её нужно использовать, хоть продукты это круто.

![Meetup Photo 10]({{ "/img/meetup_netflix/photo_10.jpg" | absolute_url }}){: .in-post-img-center .in-post-img-border}

> На этом митап окончен. 2 часа и 17 минут живого общения подошли к концу!

А чтобы не пропустить следующие части, подписывайся на мой авторский telegram канал
[«Об IT без галстуков»](https://goo.gl/E3AFL1). На канале, с позиции CTO продуктовой компании, я делюсь своим
видением технологий, пишу техничку, про менеджмент персонала, планы личностного развития и психологию построения
команд.

Если Вы готовы к серьезных челенджам и разделяете подход freedom and responsibility, готовы в релокейту в USA, то
референс в netflix запросить можно у Арсена по адресу `arsen.kostenko at gmail`. Я тоже разделяю подобные подходы
и внедряю их в Авроре, еще и сфера деятельности совпадают. Экспертов желающих поработать со мной в Киеве рад видеть и
у себя. Пишите на `d.menshikov at gmail`.

> Кстати, про свои и командные фейлы с винами я рассказывал в
[публикации про предновогодний релиз]({{ site.baseurl }}{% link _posts/2019-10-05-story-of-one-ny-release.md %})!
Это пример того что мы делаем и с чем сталкиваемся, а не эти всякие смузипроводы, формошлепсткие галеры и прожигание
жизни без цели. Мы же решаем проблемы, имеем стратегию и знаем куда идем.