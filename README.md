Обобщенная игра камень-ножницы-бумага (с любым числом произвольных комбинаций).

При запуске параметрами командной строки (аргументы метода Main) передаётся нечётное число неповторяющихся строк (больше либо равно трём).
При неправильно заданных аргументах выводится сообщение об ошибке — что именно неверно и пример как правильно.
Эти строки — это ходы (например, Камень Ножницы Бумага или Камень Ножницы Бумага Ящерица Спок или 1 2 3 4 5 6 7 8 9).

Победа определяется так: половина следующих по кругу выигрывает, половина предыдущих по кругу проигрывает.

Программа:
1. Генерирует случайный ключ (RandomNumberGenerator) длиной 128 бит, который будет SEED для генерации HMAC на базе SHA256;
2. Делает свой ход (также рандомом, причём ход - это строка, а не индекс);
3. Вычисляет HMAC на от хода и от сгенерированного ключа;
4. Выводит на консоль HMAC хода компьютера и меню (1 - Камень, 2 - Ножницы, 3 - Бумага, 0 - Exit, ? - Help)
5. После выбора хода на в консоль выводится результат игры (победа / поражение / ничья), ход программы, и исходный ключ (SEED),
    тем самым пользователь может проверить что программа играет честно.
6. При выборе опции "?" (Help) в консоли отображается таблица, определяющая какой ход выигрывает.
