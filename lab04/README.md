# Лабораторная работа №4
## Цель работы
Приобретение практических навыков в:
* Управлении файлами
* Использование системных вызовов ФС

## Задание
Изучить технологию отображения файлов в выбранной операционной системе и
работу с основными функциями файловой системы. Составить программу на языке
Си, обрабатывающую текстовые файлы – текстовый процессор. При обработке
использовать стандартные средства управления файлами в конкретной ОС. Для
сдачи лабораторной работы на «отлично» необходимо обязательное использование
технологии отображения файлов в память. Подгружать файл целиком в оперативную
память нельзя. Необходимо предусмотреть следующие ключи текстового процессора:
- Максимальный размер оперативной памяти, которая используется программой
    (Если используется технология «File mapping», то этот параметр отвечает за
    размер окна в mapping)
- Варианты использования программы (помощь при работе с программой)
    (Например, /help, /?)
Программа должна уметь работать в 2-ух режимах:
- Интерактивный режим (в одном процессе программы может быть выполнено
    несколько действий по обработке файла):
    - Необходима функция выхода из программы
    - Функция смены файла, не закрывая приложение текстового процессора
    - Вывод состояние файла (количество строк и символов в файле)
- В режиме одной команды (например, a.exe /file:test.txt /command:getLine 5)
    - В режиме одной команды должны быть доступны все те же функции, что
        и в интерактивном режиме

## Вариант(22)
### Вывод на экран(2)
Вывести диапазон символов

### Поиск в файле(1)
Поиск по подстроке без спецсимволов. Необходимо реализовать возможность
выбора режима поиска с учетом регистра/без учета регистра. Поиск осуществлять по
строкам.

### Редактирование(2)
Запись/удаление любого количества символов с любой позиции в файле.

### Безопасность(1)
Проверка того, что конкретный файл не открыт в нескольких процессах
программы.
