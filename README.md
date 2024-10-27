# goit-algo-hw-09

## Жадібні алгоритми та динамічне програмування ## 
Вітаємо в домашньому завданні до теми “Жадібні алгоритми та динамічне програмування”! 🙂

Вивчення жадібних алгоритмів та алгоритмів динамічного програмування разом із практичним досвідом розв'язання завдань допоможе вам покращити свою майстерність у сфері оптимізації та аналізу алгоритмів.

Під час виконання цього домашнього завдання:

ви зможете поглибити свої знання та розуміння в реалізації жадібних алгоритмів та алгоритмів динамічного програмування;
отримаєте можливість застосувати теоретичні знання на практиці: розробка функцій жадібного алгоритму та алгоритму динамічного програмування дозволить вам легше розуміти їхню реальну природу та застосування;
через порівняння ефективності двох різних методів розв’язання одного завдання ви навчитесь проводити об'єктивний аналіз та розуміти, який метод може бути ефективнішим у конкретних умовах.
Бажаємо успіхів та нехай код буде з вами! 🚗✨

## Опис домашнього завдання ##
У конспекті ми розглянули приклад про розбиття суми на монети. Маємо набір монет [50, 25, 10, 5, 2, 1]. Уявіть, що ви розробляєте систему для касового апарату, яка повинна визначити оптимальний спосіб видачі решти покупцеві.

Вам необхідно написати дві функції для касової системи, яка видає решту покупцеві:

Функція жадібного алгоритму find_coins_greedy. Ця функція повинна приймати суму, яку потрібно видати покупцеві, і повертати словник із кількістю монет кожного номіналу, що використовуються для формування цієї суми. Наприклад, для суми 113 це буде словник {50: 2, 10: 1, 2: 1, 1: 1}. Алгоритм повинен бути жадібним, тобто спочатку вибирати найбільш доступні номінали монет.

Функція динамічного програмування find_min_coins. Ця функція також повинна приймати суму для видачі решти, але використовувати метод динамічного програмування, щоб знайти мінімальну кількість монет, необхідних для формування цієї суми. Функція повинна повертати словник із номіналами монет та їх кількістю для досягнення заданої суми найефективнішим способом. Наприклад, для суми 113 це буде словник {1: 1, 2: 1, 10: 1, 50: 2}

Порівняйте ефективність жадібного алгоритму та алгоритму динамічного програмування, базуючись на часі їх виконання або О великому та звертаючи увагу на їхню продуктивність при великих сумах. Висвітліть, як вони справляються з великими сумами та чому один алгоритм може бути більш ефективним за інший у певних ситуаціях. Свої висновки додайте у файл readme.md домашнього завдання.

## Порівняння жадібного алгоритму та алгоритму динамічного програмування ## 

Результати виконання:

| Amount | Greedy Algorithm (s) | Dynamic Programming (s) |
|--------|-----------------------|-------------------------|
|     20 |       0.00066370      |      0.02548060        |
|     75 |       0.00049960      |      0.04485210        |
|    127 |       0.00032390      |      0.07960490        |
|    207 |       0.00032990      |      0.14903870        |
|    555 |       0.00028430      |      0.50444470        |
|   1111 |       0.00101620      |      0.98574810        |


| Алгоритм                 | Результат для суми 113       | Час виконання (секунди) | Коментар                       |
|--------------------------|------------------------------|--------------------------|--------------------------------|
| Жадібний алгоритм        | `{50: 2, 10: 1, 2: 1, 1: 1}`| 0.000123                 | Швидкий, але не завжди оптимальний |
| Динамічне програмування  | `{50: 2, 10: 1, 2: 1, 1: 1}`| 0.001456                 | Забезпечує мінімальну кількість монет |

1. Жадібний алгоритм
Жадібний алгоритм вибирає монети найбільшого номіналу до повного розподілення суми.
Кожна монета перевіряється один раз: O(n), де n — кількість монет у наборі.
Складність залежить від швидкості розподілення суми найбільшими монетами.

3. Алгоритм динамічного програмування
Цей алгоритм використовує таблицю для зберігання мінімальної кількості монет для кожної можливої суми до заданої суми.
Ініціалізація таблиці: O(m), де m — сума для розподілу.
Оновлення таблиці для кожної монети і суми: O(c * m), де c — кількість монет, m — сума.
Таким чином, загальна часова складність становить O(c * m).

Висновки:
Жадібний алгоритм може працювати швидше для великих сум, оскільки він завжди вибирає найбільший номінал і потребує меншої кількості ітерацій. Однак він може не дати мінімальної кількості монет, якщо набір номіналів нестандартний.
Тобто, жадібний алгоритм є швидшим і простішим у реалізації, але він не завжди гарантує мінімальну кількість монет для будь-якого набору номіналів. 
Алгоритм динамічного програмування потребує більше часу через багаторазове проходження через різні суми, але він завжди повертає мінімальну кількість монет. Він завжди знаходить оптимальний результат, але вимагає більше часу і пам'яті.
