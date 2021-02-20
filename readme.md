Методы:

     postMessage(connectorId,data) - Отправка сообщения коннектору получателю
                  connectorId <in>   [String] - Идентификатор коннектора получателя
                  data            <in>   [String] - Данные для передачи

     connect(connectorId) - Метод для проверки доступности указанного коннектора
                  connectorId <in>   [String] - Идентификатор проверяемого коннектора

Свойства:

     id               <out>   [String] - Идентификатор текущего коннектора

     onmessage  <in>    [Object] - Задаёт ссылку на объект обратного вызова (функцию).
                                               Во время срабатывания события в функцию/метод обратного вызова передаёт 2 параметра (connectorId, data)


3) Идентификатор коннектора генерируется как уникальный GUID и задаётся внутри самого объекта
4) Вместо использования отдельных инстансов Shell Browser Window используется только один для всех коннекторов. Благодаря этому при падении скрипта / закрытии процесса в памяти не остаётся инстансов открытых окон кроме одного, обеспечивающего работу коннекторов.