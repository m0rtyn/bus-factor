# Правила работы с исходным кодом

Оформление кода — это важно. Читать уже написанный код приходится во много раз чаще, чем писать его, причем читать код приходится не только его автору, но и другим людям. Когда код выдержан в едином и хорошем стиле, читать его гораздо проще и приятнее, глаза не "спотыкаются" об оформление, и можно быстрее понять суть. В этом разделе собраны правила по работе с исходным кодом, которых мы стараемся придерживаться для всех наших проектов.

## Только английский язык

Все имена файлов, названия переменных, функций, параметров, классов, методов, комментарии, базовая документация к коду, названия структур данных, таблиц и полей в БД, заголовки коммитов, названия веток и т.д. должны быть строго на английском языке. Старайтесь писать грамотно, если вы замечаете ошибки или опечатки — исправляйте их.

## Придумывайте хорошие названия

Это бывает сложно. Но нужно. Что бы вы не называли, переменную, файл, коммит, раздел в документации или что-то еще, старайтесь, чтобы название ясно отражало суть и легко читалось. При прочих равных лаконичные названия предпочтительнее длинных, но это не должно быть в ущерб понятности и читаемости.

Пример, объявление функции:

+ `const lang = () => ...` — не годится, имя не отражает сути. Непонятно, что именно с "lang" делает эта функция;
+ `const withLanguage = () => ...` — отлично, сразу понятно назначение функции (HOC в React обычно называются, начиная с with).

## Пишите тесты

Каждый написанный модуль стоит покрывать тестами. Каждый.

## Напишите README

Новый разработчик, подключающийся к вашему проекту, должен быть в состоянии сам разобраться что в общих чертах делает этот проект, и как он может подключиться к разработке. Если у проекта есть публичное API — опишите как им пользоваться, хотя бы самое важное.

## Контроль версий

+ Держите в репозитории всю вашу работу по проекту. Документация, вики, настройки серверов, вспомогательные скрипты и утилиты — гораздо удобнее, когда все это собрано в одном месте и версионируется.
+ Не храните лишнее и избегайте дублирования. Не следует включать в репозиторий то, что может быть получено из других источников. Например, не нужно включать скомпилированные файлы, потому что они могут быть получены путем компиляции из исходников. Не включайте сторонние библиотеки, используйте менеджеры зависимостей — pip, nuget, npm, bower, composer, ...
+ Делайте атомарные коммиты с говорящими заголовками. Это ключевой принцип, обеспечивающий хорошую читаемость истории проекта, а также облегчающий проведение code review. Каждый коммит должен содержать одно логическое изменение в проекте, например, реализацию какой-то фичи, или исправление ошибки.
+ Для именования коммитов используейте [Conventional Commits и набор хуков](./git.md)

## Удаляйте мертвый код

Не оставляйте в проекте закомментированные и неиспользуемые блоки кода. Если в будущем потребуется посмотреть, как было раньше, или же откатиться на предыдущую версию — для этого есть контроль версий.

## Соблюдайте авторские права и NDA

Eсли вы включаете в состав проекта сторонний исходный код или готовые компоненты, обращайте внимание, допускается ли это их лицензионным соглашением.

Что касается вашего собственного кода, который вы пишете по работе, то он принадлежит работодателю, и не подлежит разглашению или использованию в сторонних проектах без явного на это разрешения.
