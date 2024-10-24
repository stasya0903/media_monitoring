# media_monitoring
система медиамониторинга
Задача: вам нужно разработать REST API (только backend!) для системы, которая поможет собирать информацию и готовить сводные отчёты о новостных публикациях в Интернете.

### Пользовательские сценарии:

1) Добавление новости. В систему передаётся URL новостного материала в Интернете. Система скачивает HTML по этому URL и создаёт на его основе сущность со следующими полями:

- дата (текущая дата)
- URL (нам его передали в запросе)
- название новости (его проще всего взять из тега title)

В ответ возвращается ID сущности.

2) Получение списка новостей. Система возвращает список (массив) ранее созданных сущностей с полями:

- ID
- дата
- URL
- название новости

3) Формирование сводного отчёта. В систему передаётся массив из нескольких ID. Система формирует и сохраняет на диск простой HTML-файл со списком примерно такого вида:

<ul>
  <li><a href="...">Заголовок новости 1</a><li>
  <li><a href="...">Заголовок новости 2</a><li>
</ul>
В ответ возвращается ссылка на этот файл.

### Важные замечания:

1) Вам нужно самостоятельно продумать всё, что касается архитектуры этого приложения. Если будут вопросы — задавайте. Не бойтесь допускать ошибки: весь смысл домашки в том, чтобы потом их обсудить и исправить.

2) Вы можете взять за основу любой фреймворк, но обращаться к методам и классам фреймворка можно только на слое Infrastructure. Другими словами, ни на слое Domain, ни на слое Application не должно использоваться ничего, кроме написанных вами классов.

3) Для хранения сущностей вы можете использовать БД или файловую систему, это не принципиально, но — см. предыдущее замечание.
