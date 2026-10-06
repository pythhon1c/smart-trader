# Smart Trader – privacy policy

Effective since 2026-10-06, for the browser extension. The same text in three languages: [English](#english) · [Українська](#українська) · [Русский](#русский).

---

## English

**Effective date:** 2026-10-06 · **Contact:** ggggggdev@gmail.com

Smart Trader adds trading tools to Steam pages: trade offer summaries and item prices, faster accepting of the offers
you choose, inventory and Community Market helpers, trade history summaries, partner reputation checks and desktop
alerts. This policy describes every piece of data the extension handles, where it goes and how to delete it. It
matches the extension's code; if the code changes what it does with data, this policy and the in-extension notice
change with it, and the extension asks for your agreement again before doing anything.

### 1. Nothing happens before you agree
After installation the extension shows a data notice. Until you press "I agree", it does nothing on Steam pages: it
reads no page data, stores nothing and makes no requests.

### 2. Data kept on your computer
Stored in your browser's extension storage (`chrome.storage.local`) on this computer, never sent to us or anyone:
- your Smart Trader settings and the state of its panels and tours;
- item marks and the notes the tools keep about items;
- trade links you save (they contain the partner's trade link token) and your own trade link;
- summaries and caches built from pages you opened: trade and inventory history summaries, item descriptions,
  Community Market prices, partner reputation results, friends lists, records of offers you accepted, the store cart
  history;
- the listings you put up for sale that still wait for your confirmation (the Steam Mobile app or e-mail), so that
  the selling tools never list those items again; each is kept for a week at most;
- what the card set tools read from your own Steam badges: the sizes and card lists of the badges' card sets, your own
  badge levels and how many copies of each card you own (kept with a one-way hash of your account, so another account
  signed in on this browser never sees them), and your account level and XP; another profile's badge levels are kept
  only while its page is open, never stored;
- the choices you made in the extension's options (optional services, sound);
- your answer to the data notice and your acceptance of the License Agreement: only its version, the time and your
  choice about automation (auto accept), with no account data.

A few page features also keep small values in the Steam site's own storage in your browser (`localStorage` and
IndexedDB of steamcommunity.com or store.steampowered.com, for example the market price caches of the selling tools),
as Steam's pages do themselves.

### 3. Your Steam session and tokens
While you use Steam pages, the extension's page code uses the session id and the web token that the open Steam page
itself holds, and the trade link tokens of trade links. They are used **only** in requests to Steam
(`steamcommunity.com`, `store.steampowered.com`, `checkout.steampowered.com`, `api.steampowered.com`), exactly as the
Steam page would use them. The session id and the web token are never stored by the extension and never passed to its
background part. Trade link tokens are stored only inside the trade links you keep (section 2). None of them is ever
sent anywhere else: the extension's background part refuses any request to a host that is not Steam's that looks like
it carries one.

### 4. Requests to Steam
The tools read the Steam pages you open and ask Steam for more of the same (more history, item descriptions, prices,
offer states) with your Steam session, as the page would. The card set tools read your own badges' details from Steam
(the card sets, your levels and XP), and a public profile's badge pages only when you ask for that profile's levels.
Crafting badges from card sets is a change on your account: it is sent to Steam (one craft at a time) only after you
have seen the plan — the games, the sets and the XP — and confirmed it; it can be stopped at any time. The other
changes on your account are sent to Steam only when you start them: accepting the offers you choose, putting items up
for sale on the Community Market (after the review of the prices, or — when you choose "Sell as prices come in" after
its warning — each item as soon as its price has been read) or taking listings down, turning items into gems and
opening booster packs. The one exception is auto accept (off by default): after your separate consent (its own box,
"Allow automatic acceptance of incoming gift trade offers", unticked until you tick it) and once you turn it on, it accepts, on its own, incoming offers in which you give nothing. The background
part asks Steam's public store API (`store.steampowered.com/api/appdetails`, `/api/packagedetails`) for prices and
pictures of games and packages without your cookies. Item pictures come from Steam's image servers.

### 5. Optional services
The three reputation sites are turned on only by you: on the page shown before Smart Trader starts (their box there is
unticked until you tick it; the browser asks you to allow the sites) or later in the extension's options. The keys.land price relay is allowed from the start (its host is installed with the
extension), but Smart Trader asks it only after you turn its prices on in Smart Trader's settings (KEYS.LAND → "Use
KEYS.LAND prices", off by default since 1.10.1); it receives nothing about you. You can turn any of them off in the options at any
time. None of them receives cookies from the extension. Each of them,
like any website, sees your IP address, your browser's name and version (User-Agent) and the time of the request.

| Service | What is sent | When |
| --- | --- | --- |
| keys.land price relay (the host listed in the extension's permissions) | only which price is wanted: `GET …/kl/v1/market/series?item=key` (or `ticket`, `gems`) `&range=24h`. Nothing about you or your account. | when prices of TF2 keys, tickets or gems are shown (at most once a minute) — only while KEYS.LAND prices are on in Smart Trader's settings (off by default); the relay itself is allowed from the start and the options can turn it off |
| backpack.tf (`backpack.tf`) | the public SteamID64 of the profile or trade partner you look at: `GET https://backpack.tf/api/IGetUsers/v3?steamid=<SteamID64>` | when you open a profile, a trade offer or the trade history |
| SteamTrades (`www.steamtrades.com`) | the same SteamID64: `GET https://www.steamtrades.com/user/<SteamID64>` (the userscript version sends your SteamTrades cookies; the extension does not) | the same |
| CSGO-Rep (`api.csgo-rep.com`) | the same SteamID64: `POST https://api.csgo-rep.com` with `{"id": <number>, "query": {"steam_id": "<SteamID64>"}}`; now and then `GET https://api.csgo-rep.com/config` (nothing about you) | the same |

Results are kept on your computer for a few hours (section 2). The keys.land price relay is run by the author of Smart
Trader; it only forwards public price data from KEYS.LAND, an independent service whose data is used with its owner's
permission. The relay keeps only ordinary server logs (the requested address and the time) for a short time and nothing
about your account. backpack.tf, SteamTrades and CSGO-Rep each apply their own privacy policy, published on their sites.

When you turn backpack.tf on, the extension also runs its tools on the backpack.tf pages you open (listing prices in
trade offer links, backpack totals); before that it does not run there at all. On those pages only your settings, the
state of the tips and the values of the backpack.tf tools themselves are made available to the page; your saved trade
links, trade partners, offer records, reputation results, purchase history and the diagnostic log are not.

Unusual effect pictures (Smart Trader's settings → Items & inventory, off by default): when you turn them on, the
browser loads those pictures from itempedia.tf (`https://itempedia.tf/assets/particles/<effect number>_94x94.png`). Like any
picture server, it sees your IP address, your browser and the time; nothing else is sent.

Links to other sites (for example SteamDB, backpack.tf, SteamTrades, Steam Card Exchange) are ordinary links: those
sites receive nothing unless you open the link.

### 6. Diagnostic log
The diagnostic log (`dev.log`) is off unless you turn it on (Smart Trader's settings on a Steam page → General →
Diagnostics). While it is on, it keeps on your computer only what is needed to find faults and slowness: timings,
counts, error messages (scrubbed) and the status of network requests, for at most 7 days and 4 MB. It never records
profiles: no SteamIDs, names, avatars, profile or trade links, tokens, session ids or page addresses; ids of offers and
trades only as salted one-way hashes. It leaves your computer only if you download it ("Download log") and send the
file yourself; "Clear log" deletes it.

### 7. What the extension does not do
- No analytics, no tracking, no ads, no affiliate links.
- No selling, renting or sharing of your data with anyone, including advertising platforms, data brokers and
  information resellers; no use for credit-worthiness or lending.
- No human reads your data: we (the developers) never receive it.
- No remote code: all of the extension's code is in its package; answers from the internet are used only as data.
- All requests use HTTPS.

**Limited Use.** Smart Trader's use of user data complies with the Chrome Web Store User Data Policy, including the
Limited Use requirements.

### 8. Keeping and deleting data
Data stays on your computer until you delete it. The extension's options have "Delete all Smart Trader data", which
removes everything in section 2 that lives in the extension's storage (but your answer to the data notice and your
acceptance of the License Agreement) and gives
the optional services' site access back to the browser. Removing the extension removes its storage as
well. Values kept in the Steam site's own storage (section 2) stay until you clear that site's data in the browser.
Caches expire and are trimmed on their own.

### 9. Changes
When what the extension does with data changes, this policy is updated, the date above changes, and the extension
shows its data notice again and waits for your agreement before doing anything.

### 10. Contact
ggggggdev@gmail.com

Smart Trader is an independent project. It is not affiliated with, endorsed or sponsored by Valve Corporation. Steam
and the Steam logo are trademarks and/or registered trademarks of Valve Corporation in the U.S. and/or other countries.

---

## Українська

**Діє з:** 2026-10-06 · **Контакт:** ggggggdev@gmail.com

Smart Trader додає інструменти для обміну на сторінки Steam: зведення пропозицій обміну й ціни предметів, швидше
прийняття вибраних вами пропозицій, помічники для інвентарю й торговельного майданчика, підсумки історії обмінів,
перевірку репутації партнерів і сповіщення на робочому столі. Ця політика описує всі дані, з якими працює
розширення, куди вони йдуть і як їх видалити. Вона відповідає коду розширення; якщо код почне інакше поводитися з
даними, зміниться і ця політика, і повідомлення в розширенні, а розширення знову попросить вашої згоди, перш ніж
щось робити.

### 1. Нічого не відбувається без вашої згоди
Після встановлення розширення показує повідомлення про дані. Доки ви не натиснете «Погоджуюсь», воно нічого не
робить на сторінках Steam: не читає даних сторінок, нічого не зберігає й не робить запитів.

### 2. Дані на вашому комп’ютері
Зберігаються в сховищі розширення вашого браузера (`chrome.storage.local`) на цьому комп’ютері й нікому не
надсилаються, зокрема й нам:
- ваші налаштування Smart Trader і стан його панелей і турів;
- мітки предметів і нотатки, які інструменти ведуть про предмети;
- збережені вами посилання для обміну (вони містять токен посилання партнера) і ваше власне посилання;
- підсумки й кеші з відкритих вами сторінок: підсумки історії обмінів та інвентарю, описи предметів, ціни
  торговельного майданчика, результати перевірки репутації, списки друзів, записи прийнятих вами пропозицій, історія
  кошика магазину;
- ваші лоти, які ще чекають вашого підтвердження (у мобільному застосунку Steam чи поштою), щоб інструменти продажу
  ніколи не виставляли ці предмети знову; кожен зберігається не довше тижня;
- те, що інструменти наборів карток читають із ваших власних значків Steam: розміри й списки карток наборів, ваші
  рівні значків і скільки копій кожної картки у вас є (зберігаються з одностороннім хешем вашого акаунта, тож інший
  акаунт, що входить у цьому браузері, їх не бачить), а також рівень і XP вашого акаунта; рівні значків чужого профілю
  тримаються лише поки відкрита його сторінка й не зберігаються;
- ваш вибір у параметрах розширення (додаткові сервіси, звук);
- ваша відповідь на повідомлення про дані й ваше прийняття Ліцензійної угоди: лише її версія, час і ваш вибір щодо
  автоматизації (автоприйняття), без даних акаунта.

Кілька функцій сторінок також тримають невеликі значення у власному сховищі сайту Steam у вашому браузері
(`localStorage` та IndexedDB сайтів steamcommunity.com чи store.steampowered.com, як-от кеш цін ринку для
інструментів продажу), як це роблять і самі сторінки Steam.

### 3. Ваша сесія Steam і токени
Коли ви користуєтеся сторінками Steam, код розширення на сторінці використовує ідентифікатор сесії та вебтокен,
які тримає сама відкрита сторінка Steam, і токени посилань для обміну. Вони використовуються **лише** в запитах до
Steam (`steamcommunity.com`, `store.steampowered.com`, `checkout.steampowered.com`, `api.steampowered.com`) — так
само, як їх використала б сторінка Steam. Ідентифікатор сесії й вебтокен розширення ніколи не зберігає й не передає
своїй фоновій частині. Токени посилань зберігаються лише всередині посилань, які ви зберегли (розділ 2). Жоден з них
нікуди більше не надсилається: фонова частина розширення відхиляє будь-який запит до не-Steam-сайту, схожий на
такий, що його містить.

### 4. Запити до Steam
Інструменти читають відкриті вами сторінки Steam і просять у Steam більше того самого (історію, описи предметів,
ціни, стан пропозицій) з вашою сесією Steam, як це зробила б сторінка. Інструменти наборів карток читають у Steam
подробиці ваших власних значків (набори карток, ваші рівні й XP), а сторінки значків публічного профілю — лише коли ви
просите рівні цього профілю. Крафт значків із наборів карток — це зміна у вашому акаунті: він надсилається до Steam
(по одному крафту) лише після того, як ви побачили план — ігри, набори й XP — і підтвердили його; його можна зупинити
будь-коли. Інші зміни у вашому акаунті надсилаються до Steam лише тоді, коли ви самі їх запускаєте: прийняття
вибраних вами пропозицій, виставлення предметів на продаж на торговельному майданчику (після перегляду цін або — коли
ви після попередження вибираєте «Продавати, щойно прочитано ціну» — кожен предмет, щойно прочитано його ціну) чи
зняття лотів, перетворення предметів на самоцвіти й відкриття наборів карток. Єдиний виняток — автоприйняття
(типово вимкнене): після вашої окремої згоди (власний прапорець
«Дозволити автоматичне прийняття вхідних подарункових трейдів», вимкнений, доки ви його не позначите) і коли ви його
ввімкнете, воно саме приймає вхідні пропозиції, в яких ви нічого не
віддаєте. Фонова частина звертається до публічного API
магазину Steam (`store.steampowered.com/api/appdetails`, `/api/packagedetails`) по ціни й зображення ігор і пакетів
без ваших cookie. Зображення предметів завантажуються із серверів зображень Steam.

### 5. Додаткові сервіси
Три сайти репутації вмикаєте лише ви: на сторінці, що показується перед початком роботи Smart Trader (там їхній
прапорець вимкнений, доки ви його не позначите; браузер попросить дозволити сайти), або пізніше в параметрах розширення. Сервер цін keys.land дозволений від початку (його хост встановлюється разом із розширенням),
але Smart Trader звертається до нього лише після того, як ви ввімкнете ці ціни в налаштуваннях Smart Trader (KEYS.LAND →
«Використовувати ціни KEYS.LAND», з 1.10.1 типово вимкнено); він нічого про вас не отримує. Вимкнути будь-який з них можна в параметрах будь-коли. Жоден з них не отримує від розширення cookie. Кожен з них, як і
будь-який сайт, бачить вашу IP-адресу, назву й версію браузера (User-Agent) і час запиту.

| Сервіс | Що надсилається | Коли |
| --- | --- | --- |
| Сервер цін keys.land (хост, зазначений у дозволах розширення) | лише те, яка ціна потрібна: `GET …/kl/v1/market/series?item=key` (або `ticket`, `gems`) `&range=24h`. Нічого про вас чи ваш обліковий запис. | коли показуються ціни ключів TF2, квитків чи самоцвітів (не частіше ніж раз на хвилину) — лише коли ціни KEYS.LAND увімкнені в налаштуваннях Smart Trader (типово вимкнені); сам сервер дозволений від початку, у параметрах його можна вимкнути |
| backpack.tf (`backpack.tf`) | публічний SteamID64 профілю чи партнера з обміну, якого ви переглядаєте: `GET https://backpack.tf/api/IGetUsers/v3?steamid=<SteamID64>` | коли ви відкриваєте профіль, пропозицію обміну чи історію обмінів |
| SteamTrades (`www.steamtrades.com`) | той самий SteamID64: `GET https://www.steamtrades.com/user/<SteamID64>` (версія-userscript надсилає ваші cookie SteamTrades; розширення — ні) | так само |
| CSGO-Rep (`api.csgo-rep.com`) | той самий SteamID64: `POST https://api.csgo-rep.com` з `{"id": <число>, "query": {"steam_id": "<SteamID64>"}}`; час від часу `GET https://api.csgo-rep.com/config` (нічого про вас) | так само |

Результати зберігаються на вашому комп’ютері кілька годин (розділ 2). Сервер цін keys.land тримає автор Smart Trader;
він лише пересилає публічні дані про ціни з KEYS.LAND — незалежного сервісу, дані якого використовуються з дозволу його
власника. Сам сервер недовго зберігає лише звичайні журнали (запитану адресу й час) і нічого про ваш акаунт. backpack.tf,
SteamTrades і CSGO-Rep застосовують власні політики конфіденційності, опубліковані на їхніх сайтах.

Коли ви вмикаєте backpack.tf, розширення також додає свої інструменти на відкриті вами сторінки backpack.tf (ціни
лотів у посиланнях на обмін, вартість рюкзака); доти воно там зовсім не працює. На цих сторінках сторінці передаються
лише ваші налаштування, стан підказок і значення самих інструментів backpack.tf; ваші збережені посилання для обміну,
партнери, записи пропозицій, результати перевірки репутації, історія покупок і діагностичний журнал — ні.

Картинки Unusual-ефектів (налаштування Smart Trader → Предмети й інвентар, типово вимкнено): коли ви їх вмикаєте,
браузер вантажить ці картинки з itempedia.tf (`https://itempedia.tf/assets/particles/<номер ефекту>_94x94.png`). Як і
будь-який сервер зображень, він бачить вашу IP-адресу, браузер і час; нічого іншого не надсилається.

Посилання на інші сайти (наприклад, SteamDB, backpack.tf, SteamTrades, Steam Card Exchange) — звичайні посилання:
ці сайти нічого не отримують, доки ви не відкриєте посилання.

### 6. Діагностичний журнал
Діагностичний журнал (`dev.log`) вимкнений, доки ви його не ввімкнете (налаштування Smart Trader на сторінці Steam →
Загальні → Діагностика). Поки він увімкнений, він зберігає на вашому комп’ютері лише потрібне, щоб знайти помилки й
повільні місця: час, кількості, повідомлення про помилки (очищені) і стан мережевих запитів, не довше 7 днів і не
більше 4 МБ. Він ніколи не записує профілі: жодних SteamID, імен, аватарів, посилань на профілі чи обмін, токенів,
ідентифікаторів сесії чи адрес сторінок; ідентифікатори пропозицій і обмінів — лише як односторонні хеші із сіллю.
Він залишає ваш комп’ютер, лише якщо ви самі завантажите його («Завантажити журнал») і надішлете файл; «Очистити
журнал» видаляє його.

### 7. Чого розширення не робить
- Жодної аналітики, стеження, реклами чи партнерських посилань.
- Жодного продажу, оренди чи передавання ваших даних будь-кому, зокрема рекламним платформам, брокерам даних і
  перепродавцям інформації; жодного використання для оцінки кредитоспроможності чи кредитування.
- Ніхто з людей не читає ваших даних: ми (розробники) їх ніколи не отримуємо.
- Жодного віддаленого коду: увесь код розширення в його пакеті; відповіді з інтернету використовуються лише як дані.
- Усі запити йдуть через HTTPS.

**Limited Use.** Використання даних користувачів у Smart Trader відповідає політиці Chrome Web Store щодо даних
користувачів (Chrome Web Store User Data Policy), зокрема вимогам Limited Use.

### 8. Зберігання й видалення даних
Дані лишаються на вашому комп’ютері, доки ви їх не видалите. У параметрах розширення є «Видалити всі дані Smart
Trader» — це видаляє все з розділу 2, що лежить у сховищі розширення (крім вашої відповіді на повідомлення про
дані й вашого прийняття Ліцензійної угоди), і повертає браузеру доступ додаткових сервісів до їхніх сайтів. Видалення розширення теж видаляє його
сховище. Значення у власному сховищі сайту Steam (розділ 2) лишаються, доки ви не очистите дані цього сайту в
браузері. Кеші застарівають і скорочуються самі.

### 9. Зміни
Коли змінюється те, що розширення робить з даними, ця політика оновлюється, дата вгорі змінюється, а розширення
знову показує повідомлення про дані й чекає вашої згоди, перш ніж щось робити.

### 10. Контакт
ggggggdev@gmail.com

Smart Trader — незалежний проєкт. Він не пов’язаний з Valve Corporation, не схвалений і не спонсорований нею. Steam і
логотип Steam — товарні знаки та/або зареєстровані товарні знаки Valve Corporation у США та/або інших країнах.

---

## Русский

**Действует с:** 2026-10-06 · **Контакт:** ggggggdev@gmail.com

Smart Trader добавляет инструменты для обмена на страницы Steam: сводки предложений обмена и цены предметов, более
быстрое принятие выбранных вами предложений, помощники для инвентаря и торговой площадки, итоги истории обменов,
проверку репутации партнёров и уведомления на рабочем столе. Эта политика описывает все данные, с которыми работает
расширение, куда они уходят и как их удалить. Она соответствует коду расширения; если код начнёт иначе обращаться с
данными, изменятся и эта политика, и уведомление в расширении, а расширение снова попросит вашего согласия, прежде чем
что-либо делать.

### 1. Ничего не происходит без вашего согласия
После установки расширение показывает уведомление о данных. Пока вы не нажмёте «Согласен», оно ничего не делает на
страницах Steam: не читает данные страниц, ничего не сохраняет и не делает запросов.

### 2. Данные на вашем компьютере
Хранятся в хранилище расширения вашего браузера (`chrome.storage.local`) на этом компьютере и никому не отправляются,
в том числе нам:
- ваши настройки Smart Trader и состояние его панелей и туров;
- метки предметов и заметки, которые инструменты ведут о предметах;
- сохранённые вами ссылки для обмена (они содержат токен ссылки партнёра) и ваша собственная ссылка;
- итоги и кеши с открытых вами страниц: итоги истории обменов и инвентаря, описания предметов, цены торговой
  площадки, результаты проверки репутации, списки друзей, записи принятых вами предложений, история корзины магазина;
- ваши лоты, которые ещё ждут вашего подтверждения (в мобильном приложении Steam или по почте), чтобы инструменты
  продажи никогда не выставляли эти предметы снова; каждый хранится не дольше недели;
- то, что инструменты наборов карточек читают из ваших собственных значков Steam: размеры и списки карточек наборов,
  ваши уровни значков и сколько копий каждой карточки у вас есть (хранятся с односторонним хешем вашего аккаунта, так
  что другой аккаунт, входящий в этом браузере, их не видит), а также уровень и XP вашего аккаунта; уровни значков
  чужого профиля держатся только пока открыта его страница и не сохраняются;
- ваш выбор в параметрах расширения (дополнительные сервисы, звук);
- ваш ответ на уведомление о данных и ваше принятие Лицензионного соглашения: только его версия, время и ваш выбор
  насчёт автоматизации (автопринятия), без данных аккаунта.

Несколько функций страниц также хранят небольшие значения в собственном хранилище сайта Steam в вашем браузере
(`localStorage` и IndexedDB сайтов steamcommunity.com или store.steampowered.com, например кеш цен торговой
площадки для инструментов продажи), как это делают и сами страницы Steam.

### 3. Ваша сессия Steam и токены
Когда вы пользуетесь страницами Steam, код расширения на странице использует идентификатор сессии и веб-токен,
которые держит сама открытая страница Steam, и токены ссылок для обмена. Они используются **только** в запросах к
Steam (`steamcommunity.com`, `store.steampowered.com`, `checkout.steampowered.com`, `api.steampowered.com`) — так же,
как их использовала бы страница Steam. Идентификатор сессии и веб-токен расширение никогда не сохраняет и не передаёт
своей фоновой части. Токены ссылок хранятся только внутри сохранённых вами ссылок (раздел 2). Ни один из них никуда
больше не отправляется: фоновая часть расширения отклоняет любой запрос к сайту не Steam, похожий на содержащий его.

### 4. Запросы к Steam
Инструменты читают открытые вами страницы Steam и запрашивают у Steam больше того же (историю, описания предметов,
цены, состояние предложений) с вашей сессией Steam, как это сделала бы страница. Инструменты наборов карточек читают у
Steam подробности ваших собственных значков (наборы карточек, ваши уровни и XP), а страницы значков публичного
профиля — только когда вы просите уровни этого профиля. Крафт значков из наборов карточек — это изменение в вашем
аккаунте: он отправляется в Steam (по одному крафту) только после того, как вы увидели план — игры, наборы и XP — и
подтвердили его; его можно остановить в любой момент. Остальные изменения в вашем аккаунте отправляются в Steam
только тогда, когда вы сами их запускаете: принятие выбранных вами предложений, выставление предметов на продажу на
торговой площадке (после просмотра цен или — когда вы после предупреждения выбираете «Продавать, как только прочитана
цена» — каждый предмет, как только прочитана его цена) или снятие лотов, превращение предметов в самоцветы и открытие
наборов карточек. Единственное исключение — автопринятие (по умолчанию выключено): после вашего отдельного согласия (собственный
флажок «Разрешить автоматическое принятие входящих подарочных трейдов», выключен, пока вы его не отметите) и когда вы
его включите, оно само принимает входящие предложения, в которых вы ничего не отдаёте. Фоновая часть обращается к
публичному API магазина Steam (`store.steampowered.com/api/appdetails`, `/api/packagedetails`) за ценами и
изображениями игр и пакетов без ваших cookie. Изображения предметов загружаются с серверов изображений Steam.

### 5. Дополнительные сервисы
Три сайта репутации включаете только вы: на странице, показанной перед началом работы Smart Trader (там их флажок
выключен, пока вы его не отметите; браузер попросит разрешить сайты), или позже в параметрах расширения. Сервер цен keys.land разрешён с самого начала (его хост устанавливается вместе с
расширением), но Smart Trader обращается к нему только после того, как вы включите эти цены в настройках Smart Trader
(KEYS.LAND → «Использовать цены KEYS.LAND», с 1.10.1 по умолчанию выключено); он ничего о вас не получает. Выключить любой из них можно в параметрах в любой момент. Ни один из них не получает от расширения cookie. Каждый из
них, как и любой сайт, видит ваш IP-адрес, название и версию браузера (User-Agent) и время запроса.

| Сервис | Что отправляется | Когда |
| --- | --- | --- |
| Сервер цен keys.land (хост, указанный в разрешениях расширения) | только то, какая цена нужна: `GET …/kl/v1/market/series?item=key` (или `ticket`, `gems`) `&range=24h`. Ничего о вас или вашей учётной записи. | когда показываются цены ключей TF2, билетов или самоцветов (не чаще раза в минуту) — только когда цены KEYS.LAND включены в настройках Smart Trader (по умолчанию выключены); сам сервер разрешён с самого начала, в параметрах его можно выключить |
| backpack.tf (`backpack.tf`) | публичный SteamID64 профиля или партнёра по обмену, которого вы просматриваете: `GET https://backpack.tf/api/IGetUsers/v3?steamid=<SteamID64>` | когда вы открываете профиль, предложение обмена или историю обменов |
| SteamTrades (`www.steamtrades.com`) | тот же SteamID64: `GET https://www.steamtrades.com/user/<SteamID64>` (версия-userscript отправляет ваши cookie SteamTrades; расширение — нет) | так же |
| CSGO-Rep (`api.csgo-rep.com`) | тот же SteamID64: `POST https://api.csgo-rep.com` с `{"id": <число>, "query": {"steam_id": "<SteamID64>"}}`; время от времени `GET https://api.csgo-rep.com/config` (ничего о вас) | так же |

Результаты хранятся на вашем компьютере несколько часов (раздел 2). Сервер цен keys.land держит автор Smart Trader;
он только пересылает публичные данные о ценах с KEYS.LAND — независимого сервиса, данные которого используются с
разрешения его владельца. Сам сервер недолго хранит только обычные журналы (запрошенный адрес и время) и ничего о вашем
аккаунте. backpack.tf, SteamTrades и CSGO-Rep применяют собственные политики конфиденциальности, опубликованные на их сайтах.

Когда вы включаете backpack.tf, расширение также добавляет свои инструменты на открытые вами страницы backpack.tf
(цены лотов в ссылках на обмен, стоимость рюкзака); до этого оно там вовсе не работает. На этих страницах странице
передаются только ваши настройки, состояние подсказок и значения самих инструментов backpack.tf; ваши сохранённые
ссылки для обмена, партнёры, записи предложений, результаты проверки репутации, история покупок и диагностический
журнал — нет.

Картинки Unusual-эффектов (настройки Smart Trader → Предметы и инвентарь, по умолчанию выключено): когда вы их
включаете, браузер загружает эти картинки с itempedia.tf (`https://itempedia.tf/assets/particles/<номер эффекта>_94x94.png`).
Как и любой сервер изображений, он видит ваш IP-адрес, браузер и время; ничего другого не отправляется.

Ссылки на другие сайты (например, SteamDB, backpack.tf, SteamTrades, Steam Card Exchange) — обычные ссылки: эти
сайты ничего не получают, пока вы не откроете ссылку.

### 6. Диагностический журнал
Диагностический журнал (`dev.log`) выключен, пока вы его не включите (настройки Smart Trader на странице Steam → Общие
→ Диагностика). Пока он включён, он хранит на вашем компьютере только нужное, чтобы найти ошибки и медленные места:
время, количества, сообщения об ошибках (очищенные) и состояние сетевых запросов, не дольше 7 дней и не больше 4 МБ.
Он никогда не записывает профили: никаких SteamID, имён, аватаров, ссылок на профили или обмен, токенов,
идентификаторов сессии или адресов страниц; идентификаторы предложений и обменов — только как односторонние хеши с
солью. Он покидает ваш компьютер, только если вы сами скачаете его («Скачать журнал») и отправите файл; «Очистить
журнал» удаляет его.

### 7. Чего расширение не делает
- Никакой аналитики, слежки, рекламы или партнёрских ссылок.
- Никакой продажи, аренды или передачи ваших данных кому-либо, в том числе рекламным платформам, брокерам данных и
  перепродавцам информации; никакого использования для оценки кредитоспособности или кредитования.
- Никто из людей не читает ваши данные: мы (разработчики) их никогда не получаем.
- Никакого удалённого кода: весь код расширения в его пакете; ответы из интернета используются только как данные.
- Все запросы идут через HTTPS.

**Limited Use.** Использование данных пользователей в Smart Trader соответствует политике Chrome Web Store в отношении
данных пользователей (Chrome Web Store User Data Policy), включая требования Limited Use.

### 8. Хранение и удаление данных
Данные остаются на вашем компьютере, пока вы их не удалите. В параметрах расширения есть «Удалить все данные Smart
Trader» — это удаляет всё из раздела 2, что лежит в хранилище расширения (кроме вашего ответа на уведомление о
данных и вашего принятия Лицензионного соглашения), и возвращает браузеру доступ дополнительных сервисов к их сайтам. Удаление расширения тоже удаляет его
хранилище. Значения в собственном хранилище сайта Steam (раздел 2) остаются, пока вы не очистите данные этого сайта в
браузере. Кеши устаревают и сокращаются сами.

### 9. Изменения
Когда меняется то, что расширение делает с данными, эта политика обновляется, дата вверху меняется, а расширение снова
показывает уведомление о данных и ждёт вашего согласия, прежде чем что-либо делать.

### 10. Контакт
ggggggdev@gmail.com

Smart Trader — независимый проект. Он не связан с Valve Corporation, не одобрен и не спонсируется ею. Steam и логотип
Steam — товарные знаки и/или зарегистрированные товарные знаки Valve Corporation в США и/или других странах.
