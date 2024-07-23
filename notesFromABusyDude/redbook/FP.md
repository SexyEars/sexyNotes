FP - программирование на чистых функциях
Pure function - функция без side effect'ов
Side effect:
- Изменение переменной
- Изменение структуры данных
- Установка поля на объекте
- Вызов исключения или остановка из-за ошибки. Вывод на консоль или чтение пользовательского ввода. Чтение или запись в файл.

Referential transparency (ссылочная прозрачность) and purity

An expression e is referentially transparent if for all programs p, all occurrences of e in p can be replaced by the result of evaluating e without affecting the meaning of p.

A function f is pure if the expression f(x) is referentially transparent for all referentially transparent x.5

