# Отчет по лабораторной работе № 11
## по курсу "Основы информатики", "Алгоритмы и структуры данных"

Студент группы М80-108Б-23 Кулешов Дмитрий Андреевич

Работа выполнена

Преподаватель: каф. 806 Севастьянов Виктор Сергеевич

1. **Тема**: Обработка последовательности литер входного текстового файла.
2. **Цель работы**: Разработать программу на языке Си, выполняющую анализ и обработку вводимого текста в соответствии с выданным заданием.
3. **Задание (вариант №8)**: Раскодировать текст, закодированный по Цезарю с переменным ключом, равным номеру слова в строке.
4. **Идея, метод, алгоритм решения задачи**: 
   - Считать символы вводимого текста по одному символу до достижения конца строки.
   - Использовать конечный автомат (фактически, конечный автомат со стеком) для анализа и обработки символов.
   - Состояние автомата "READ_NONSPACE" используется для чтения непустой последовательности литер.
   - В этом состоянии, если символ является разделителем, переходить в состояние "READ_SPACE", чтобы прочитать пробел и обновить ключ.
   - Если символ является буквой, применять формулу Цезаря с переменным ключом для раскодировки символа и выводить его на экран.
   - Если символ не является буквой, то выводить его без изменений.
   - В состоянии "READ_SPACE" выводить пробел и, если символ не является разделителем, обновлять ключ и обработать символ аналогичным образом, как в состоянии "READ_NONSPACE".
5. **Сценарий выполнения работы**:

| Входные данные | Выходные данные |
|----------------|-----------------|
| ef ef            | bc ab         | 
| hello hello hello | ebiil dahhk czggj|
| a b c d e f g h   | x x x x x x x x  |

Представленные примеры лишь проверяют правильность работы программы, в них понятные человеку слова дешифруются в последовательность символов, но алгоритм при этом срабатывает правильно.
   - Разработать алгоритм и псевдокод решения задачи.
   - Написать программу на языке Си, используя разработанный алгоритм.
   - Провести тестирование программы, проверив ее работу на различных тестовых данных, включая граничные случаи.
6. **Протокол**: Код программы: https://github.com/dmitriikuleshov/MAI_labs/blob/main/lab11/main.c
7. **Замечания автора** по существу работы: Работа выполнена в соответствии с поставленным заданием. Программа успешно выполняет анализ и обработку вводимого текста, раскодируя его по Цезарю с переменным ключом. 

8. **Выводы**: В ходе выполнения данной лабораторной работы я освоил простейшие приёмы лексического анализа и применение конечного автомата для обработки последовательности литер в текстовом файле. Также, на практике я использовал функции стандартной библиотеки языка Си для работы с символами и написал программу, которая может обрабатывать текстовый файл любой длины и произвольной структуры.