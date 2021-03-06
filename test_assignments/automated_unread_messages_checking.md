## RoR + Selenium: автоматизированная проверка новых личных сообщений на форуме

Необходимо продемонстрировать умение не только решать поставленную задачу, но и качественно оформлять код:

- выбирать содержательные названия для классов, методов и переменных;

- писать разумные комментарии к каждому классу и методу, указывать тип и описание для каждого параметра;

- создавать методы и классы разумного размера (по количеству строк);

- использовать константы с понятными названиями вместо «магических чисел».

Необходимо обдумать не только «позитивный» случай, но и возможные ошибки в процессе обработки (на практике они более чем возможны). В том числе случай, когда меняется структура страниц и алгоритм перестаёт функционировать корректно. Все такие ошибки должны правильно и, по возможности, унифицированно обрабатываться.

**Задание**

Реализуйте автоматизированную проверку наличия новых личных сообщений на вашем любимом форуме.

**Предполагаемый алгоритм решения задачи**

- залогиниться на форуме, используя предоставленные логин и пароль аккаунта;

- перейти в раздел личных сообщений;

- попытаться найти элемент,содержащий число новых сообщений;

- в случае его наличия — прочитать `inner Text/value`.

Задание нужно реализовать на Ruby On Rails в виде API-вызова, где логин и пароль аккаунта являются GET-параметрами, а ответ - JSON-объектом с единственным полем `unread_messages_count`.

Рекомендуем продумать архитектуру решения: желательно выделить «низкий уровень» элементарных запросов и «высокий уровень» управления навигацией и обработки ошибок навигации. Обязательно использовать принцип «тонких контроллеров».