FP - программирование на чистых функциях.
Pure function - функция без side effect'ов.
Side effect - something a function does aside from simply returning a result. Examples:
- изменение переменной;
- изменение структуры данных;
- установка поля на объекте `???`;
- вызов исключения или остановка из-за ошибки;
- вывод на консоль или чтение пользовательского ввода;
- чтение или запись в файл.

`Referential transparency` - An expression e is referentially transparent if for all programs p, all occurrences of e in p can be replaced by the result of evaluating e without affecting the meaning of p.

`Purity` - A function f is pure if the expression f(x) is referentially transparent for all referentially transparent x.

`Substitution model` - позволяет проверить, является ли выражение ссылочно прозрачным. (просто подставляем одно вместо второго, но определение неточное 😥)



