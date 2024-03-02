# UserInput

## Описание
Это приложение, которое запрашивает у пользователя ввод данных в определенном формате и записывает эти данные в файл.

## Формат ввода
Пользователь должен ввести данные в следующем формате, разделенные пробелом:

**Фамилия Имя Отчество дата_рождения номер_телефона пол**


## Форматы данных
- Фамилия, имя, отчество - строки
- Дата_рождения - строка формата dd.mm.yyyy
- Номер_телефона - целое беззнаковое число без форматирования
- Пол - символ латиницей f или m

## Обработка ошибок
Приложение проверяет введенные данные по количеству. Если количество не совпадает, выводится сообщение об ошибке. Приложение также проверяет форматы данных. Если форматы данных не совпадают, выбрасывается исключение, соответствующее типу проблемы.

## Запись в файл
Если все данные введены и обработаны верно, создается файл с названием, равным фамилии, и в него записываются полученные данные. Однофамильцы записываются в один и тот же файл, в отдельные строки, однако программа не проверяет полных однофамильцев, чего можно достичь добавив например проверку на эквивалентность даты рождения. При возникновении проблемы с чтением-записью в файл, исключение обрабатывается и пользователь видит стектрейс ошибки.
