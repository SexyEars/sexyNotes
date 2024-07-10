**Cohesion** (сплоченность) представляет собой степень, в которой часть базы кода образует логически единую атомарную единицу.
Он также может указать на количество связей внутри некоторой кодовой единицы. Если число мало, то, вероятно, границы для блока выбраны неправильно, код внутри блока логически не связан.
Блок (юнит) здесь необязательно является классом. Это может быть метод, класс, группа классов или даже модуль: понятие cohesion (а также coupling) применимо на разных уровнях.

**Coupling** (связанность) представляет собой степень, в которой один блок независим от других. Другими словами, это количество связей между двумя или более единицами. Чем меньше число, тем ниже связь.

По сути, высокий cohesion означает хранение связанных друг с другом частей кода в одном месте. В то же время низкий coupling заключается в максимально возможном разделении несвязанных частей кодовой базы.

![[cohesion&couplingImage.png]]

**1. Ideal** is the code that follows the guideline. It is loosely coupled and highly cohesive. We can illustrate such code with this picture:

![Ideal](https://enterprisecraftsmanship.com/images/2015/2015-09-02-1-01.png)

Ideal

Here, circles of the same color represent pieces of the code base related to each other.

**2. God Object** is a result of introducing high cohesion and high coupling. It is an [anti-pattern](https://en.wikipedia.org/wiki/God_object) and basically stands for a single piece of code that does all the work at once:

![God Object](https://enterprisecraftsmanship.com/images/2015/2015-09-02-1-02.png)

God Object

Another naming for this kind of code would be Big Ball of Mud.

**3.** The third type takes place when the boundaries between different classes or modules are selected poorly:

![Poorly selected boundaries](https://enterprisecraftsmanship.com/images/2015/2015-09-02-1-03.png)

Poorly selected boundaries

Unlike God Object, code of this type does have boundaries. The problem here is that they are selected improperly and often do not reflect the actual semantics of the domain. Such code quite often violates the [Single Responsibility Principle](https://en.wikipedia.org/wiki/Single_responsibility_principle).

**4. Destructive decoupling** is the most interesting one. It sometimes occurs when a programmer tries to decouple a code base so much that the code completely loses its focus:

![Destructive Decoupling](https://enterprisecraftsmanship.com/images/2015/2015-09-02-2-04.png)

Destructive Decoupling

- Невозможно добиться полного разделения (decoupling) без нарушения целостности (cohesion), и наоборот.

- "high cohesion и low coupling" желателен на всех уровнях вашей кодовой базы.
