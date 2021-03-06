# Sort
## Сортировка методом пузырька

Сортиро́вка простыми обменами, сортировка пузырько́м (англ. bubble sort) — простой алгоритм сортировки. Для понимания и реализации этот алгоритм — простейший, но эффективен он лишь для небольших массивов. 

Алгоритм состоит из повторяющихся проходов по сортируемому массиву. За каждый проход элементы последовательно сравниваются попарно и, если порядок в паре неверный, выполняется перестановка элементов. Проходы по массиву повторяются N-1 раз или до тех пор, пока на очередном проходе не окажется, что обмены больше не нужны, что означает — массив отсортирован. При каждом проходе алгоритма по внутреннему циклу, очередной наибольший элемент массива ставится на своё место в конце массива рядом с предыдущим «наибольшим элементом», а наименьший элемент перемещается на одну позицию к началу массива («всплывает» до нужной позиции, как пузырёк в воде — отсюда и название алгоритма).

### Реализация 

Особенность данного алгоритма заключается в следующем: после первого завершения внутреннего цикла максимальный элемент массива всегда находится на N-ой позиции. При втором проходе, следующий по значению максимальный элемент находится на N-1 месте. И так далее. Таким образом, на каждом следующем проходе число обрабатываемых элементов уменьшается на 1 и нет необходимости «обходить» весь массив от начала до конца каждый раз.

Так как подмассив из одного элемента не нуждается в сортировке, то для сортировки требуется делать не более N-1 итераций внешнего цикла. Поэтому в некоторых реализациях внешний цикл всегда выполняется ровно N-1 и не отслеживается, были или не были обмены на каждой итерации.

## Сортировка вставками

Сортировка вставками (Insertion Sort) — это простой алгоритм сортировки. Суть его заключается в том что, на каждом шаге алгоритма мы берем один из элементов массива, находим позицию для вставки и вставляем. Стоит отметить что массив из 1-го элемента считается отсортированным.

### Реализация

Основной цикл алгоритма начинается не с 0-го элемента а с 1-го, потому что элемент до 1-го элемента будет нашей отсортированной последовательностью (помним что массив состоящий из одного элемента является отсортированным) и уже относительно этого элемента с номером 0 мы будем вставлять все остальные.

