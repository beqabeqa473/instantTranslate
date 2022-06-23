# instantTranslate (Миттєвий переклад) #

* Автори: Alexy Sadovoy, Beqa Gozalishvili, Mesar Hameed, Alberto Buffolino
  та інші розробники NVDA.
* Завантажити [стабільну версію][1]
* Завантажити [версію в розробці][2]

Цей додаток дозволяє перекладати виділений текст чи текст з буфера обміну з
однієї мови на іншу. Для перекладу використовується Google Translate.

## Конфігурування мов ##
Щоб налаштувати мову оригіналу і перекладу, а також випадки зміни мов, перейдіть до меню NVDA >> «Налаштування» >> «Налаштування Instant Translate».

Є два комбіновані списки з назвами «Мова оригіналу» і «Мова перекладу», і
прапорець, щоб вирішити, чи потрібно копіювати переклад у буфер обміну.

Крім того, якщо ви оберете параметр «автоматично» (перший варіант) в
комбінованому списку «Мова оригіналу», ви також знайдете комбінований список
«Мова для зміни» і прапорець, який відповідає за автоматичну зміну мови.

Значення двох перших комбінованих списків та прапорця для копіювання чітке,
але решту параметрів потребують додаткових пояснень. Завжди пам’ятайте, що
наведені нижче пояснення передбачають мову оригіналу, встановлену для
параметра «автоматично».

Комбінований список «Мова для зміни» корисний у разі заміни мови оригіналу й
перекладу за сценарієм (дивіться нижче); насправді, параметр «автоматично»
для мови перекладу не має сенсу, тому додаток встановлює для неї значення з
комбінованого списку вище.

Отже, уявімо таку ситуацію: ви зазвичай перекладаєте на англійську (вашу
основну мову), але іноді (наприклад, коли пишете документ) потрібно
перекласти на італійську (припустимо, вашу другу мову); ви можете встановити
у комбінованому списку «Мова для зміни» італійську, щоб перекладати з
англійської на італійську, не переходячи безпосередньо до налаштувань
додатка. Очевидно, що ця функція має основну чи другорядну користь
відповідно до ваших частіших потреб.

Тепер про прапорець автоматичної зміни: він з’являється тоді і лише тоді,
коли ви встановили параметр «автоматично» в списку «Мова оригіналу» і
безпосередньо пов’язаний зі списком «Мова для зміни». Якщо ви активуєте
його, тоді додаток намагатиметься автоматично переходити  з конфігурації мов
оригіналу  та перекладу  до конфігурації, де мова перекладу стає мовою
оригіналу, а мова, вибрана у списку «Мова для зміни», стає новою мовою
перекладу; надзвичайно корисно, якщо оригінальною мовою тексту, який ви
хочете перекласти, є мова перекладу.

Простий приклад: знову візьмемо до уваги ситуацію, яку розглядали раніше;
якщо ви перекладаєте текст мовою, відмінною від англійської, немає проблем,
ви отримуєте правильний переклад англійською мовою. Але якщо вам потрібно
перекласти текст з англійської, зазвичай ви отримуєте переклад англійською
мовою, ідентичний оригінальному, і це даремна трата часу. Однак завдяки
функції автоматичної заміни, припускаючи, що ви хочете знати, як ваш текст
звучить італійською, додаток автоматично замінює мову перекладу на
італійську, тому він повертає дійсний переклад.

У будь-якому разі, це тимчасова конфігурація; якщо ця опція не має ефекту
(це експериментально), спробуйте перемкнутися вручну до стабільної
конфігурації, використовуючи жест для зміни, описаний нижче. Це
експериментально, оскільки в деяких ситуаціях (з короткими текстами, як
правило) Google не розпізнає справжню мову оригіналу правильно і вам
доводиться за допомогою скрипта вручну примушувати мову оригіналу стати
мовою перекладу (англійською мовою в нашому прикладі).

Принаймні, у діалозі параметрів мовлення (меню NVDA >> Налаштування >> Мовлення) ви можете встановити прапорець «Автоматичне перемикання мови (якщо підтримується)». Таким чином, якщо ви використовуєте мультимовний синтезатор, переклад буде оголошено голосом, який розмовляє мовою перекладу.

## Як користуватися ##
Ви можете  використати цей додаток трьома способами:

1. Виділіть частину тексту стандартними методами (наприклад, shift зі
   стрілками), після чого натисніть відповідну клавішу, щоб перекласти
   виділений текст. після цього перекладені рядки прочитає синтезатор
   мовлення, який ви використовуєте.
2. Ви також можете перекласти текст з буфера обміну.
3. Натисніть спеціальну швидку клавішу, щоб перекласти останню вимовлену
   фразу.

## Гарячі клавіші ##
Усі нижченаведені команди необхідно натискати після комбінації
«NVDA+Shift+t»:

* T: перекладає виділений текст,
* Shift+t: перекладає текст з буфера обміну,
* S: міняє місцями мови оригіналу і перекладу,
* A: промовляє поточну конфігурацію,
* C: копіює останній результат в буфер обміну,
* I: визначає мову виділеного тексту,
* L: перекладає останню вимовлену фразу,
* O: відкриває налаштування перекладу
* H: промовляє всі доступні багаторівневі команди.

## Зміни у версії 4.4.3 ##
* Додано можливість замінювати підкреслення пробілами, що, можливо, зможе
  поліпшити результати перекладу в залежності від контексту (подяка Beka
  Gozalishvili)
* Додано сумісність з NVDA 2022.1

## Зміни у версії 4.4.2 ##
* Відновлено виявлення й автозміну мов (подяка за виправлення Cyrille)
* оновлено мови для перекладу (подяка Cyrille)

## Зміни у версії 4.4 ##
* Instant translate тепер сумісний із NVDA 2019.3 (версії NVDA на Python 3)

## Зміни у версії 4.3 ##
* виправлення сумісності з NVDA Тепер Instant Translate буде сумісний з
  останніми збірками nvda.
* знайшли спосіб знову використовувати Google як службу перекладу.

## Зміни у версії 4.2 ##
* Відновлено робочий стан з новішими версіями nvda.
* Відновлено автоматичне виявлення мови.

## Зміни у версії 4.1 ##
* Додаток InstantTranslate знову працює, але замість Google Translate
  використовує сервіс перекладу від Yandex.

## Зміни у версії 4.0 ##
* Після того, як ви поміняєте мови місцями, переклад виконається
  автоматично.
* Виправлено помилку з кешуванням.

## Зміни у версії 3.0 ##
* Змінено спосіб використання команд, тепер вам потрібно натискати
  «NVDA+Shift+t», а потім літеру для виконання низки дій (усі команди
  дивіться у розділі «Команди»).
* Додано можливість міняти мови місцями.
* Змінено формат конфігурації, тепер можна змінити налаштування миттєвого
  перекладу, перебуваючи в області лише для читання, але пам’ятайте, що це
  спрацює перед першим перезапуском NVDA.
* Видалено ліміт на обсяг тексту, який можна перекласти.
* Додано клавіатурне скорочення t для елемента меню «Налаштування Instant
  Translate»
* Параметр «автоматично» тепер розташований першим у списку мов оригіналу і
  вилучений зі списку мов перекладу.
* Додано прапорець для налаштування копіювання результатів перекладу.
* Файл конфігурації зберігається в корені папки з налаштуваннями.
* Мови оригіналу й перекладу синхронізовані з тими, які наразі надає
  перекладач Google (22 квіт 2015).


## Зміни у версії 2.1 ##
* Додаток може перекладати текст з буфера обміну, коли ви натиснете
  nvda+shift+y.

## Зміни у версії 2.0 ##
* Додано діалог вибору мов оригіналу й перекладу.
* У меню «Параметри» додано елемент меню додатка.
* Зараз налаштування прописуються в окремому конфігураційному файлі.
* Результати перекладу автоматично копіюються в буфер обміну для подальших
  дій з ними.

## Зміни у версії 1.0 ##
* Перший реліз.


[[!tag dev stable]]

[1]: https://addons.nvda-project.org/files/get.php?file=it

[2]: https://addons.nvda-project.org/files/get.php?file=it-dev