Для начала работы с методами вам потребуется создать аккаунт на GitHub (если еще не создан), создать репозиторий с произвольным содержимым (если такого еще нет) и создать API-ключ на соответствующее приложение. 
Для создания issue с названием Issue 1 нужно использовать POST-запрос и следующий URL: https://api.github.com/repos/Artem1305/repository_name_1/issues
Для получения списка issues нужно использовать GET-запрос и следующий URL: https://api.github.com/repos/Artem1305/repository_name_1/issues
Для изменения названия задачи нужно использовать PATCH-запрос и следующий URL: https://api.github.com/repos/Artem1305/repository_name_1/issues/1
Для удаления измененной задачи нужно использовать DELETE-запрос и следующий URL: https://api.github.com/repos/Artem1305/repository_name_1/issues/1/lock       Но при удалении запрос срабатывает, но задача фактически не удаляется. По документации есть DELETE -запрос, но он касается разблокировки проблемы. По 4ому заданию (удаление issues) являются не актуальными по версии API, в документации отсутствует описание и запрос по delete issues. Просмотрев документацию связанной с нашей задачей я нашел множество значений, которые можно удалить, например такое как: «удаление комментария».
Так же сверил запрос удаление issues с UI, в девтулз уходит запрос с методом POST с условием удаления нашей задачи, попробовал воспроизвести данный запрос в постман, ответ был 404, такого запроса api не существует. 
Так как нет актуального запроса на полное удаление нашей проблемы, я взял запрос с методом DELETE с документации GitHub и проверил его работоспособность со своей заведенной issues, запрос отрабатывает корректно.
