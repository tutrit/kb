# Stream API cheet sheet

## Basic operations

```java
    List<String> collected = Stream.of("a", "b", "c")
        .collect(Collectors.toList());
```

<table>
    <tr>
        <td>
            collect(toList())
        </td>
        <td>
\n
            ```java
                List<String> collected = Stream.of("a", "b", "c")
                    .collect(Collectors.toList());
            ```
\n
        </td>
        <td>
            Порождает коллекцию из стрима
        </td>
    </tr>
    <tr>
        <td>
            map
        </td>
        <td>
List<String> collected = Stream.of("a", "b", "c")
.map(string -> string.toUpperCase())
.collect(Collectors.toList());
        </td>
        <td>
применяет функцию, которая преобразует значение одного типа в другой, и возвращает стрим нового типа
        </td>
    </tr>
    <tr>
        <td>
filter
        </td>
        <td>
List<String> collected = Stream.of("a", "b", "c")
.filter(string -> string.equals("a"))
.collect(Collectors.toList());
        </td>
        <td>
применяет функцию, которая проверяет соответствие значения заданному, и возвращает стрим соответствующих значений
        </td>
    </tr>
    <tr>
        <td>
flatMap
        </td>
        <td>
List<Integer> together = Stream.of(Arrays.asList(1, 2), Arrays.asList(3, 4))
.flatMap(numbers -> numbers.stream())
.collect(toList());
        </td>
        <td>
позволяет заменить значение объектом Stream и соединить все стримы (стрим стримов)
        </td>
    </tr>
    <tr>
        <td>
max min
        </td>
        <td>
List<Person> persons = asList(new Person("Max", 52), new Person("Vlad for Your Furs", 37), new Person("Don", 45));

persons.stream()
.min(Comparator.comparing(p -> p.getAge()))
.get();
        </td>
        <td>
нахождение максимума или минимума
       </td>
    </tr>
    <tr>
        <td>
reduce
        </td>
        <td>
int result = numbers.stream()
.reduce(0, (subtotal, element) -> subtotal + element);

0 - Identity(subtotal, element) -> subtotal + element - accumulator

List<Integer> numbers = Arrays.asList(1, 2, 3, 4, 5, 6); int result = numbers.parallelStream()
.reduce(0, (subtotal, element) -> subtotal + element, Integer::sum);

Integer::sum - combiner

if we use sequential streams and the types of the accumulator arguments and the types of its implementation match, we
don't need to use a combiner.
        </td>
        <td>
reduction stream operations allow us to produce one single result from a sequence of elements, by applying repeatedly a
combining operation to the elements in the sequence.

count , min и max - это распространенные частные случаи общего принципа редукции.

Identity – an element that is the initial value of the reduction operation and the default result if the stream is empty

Accumulator – a function that takes two parameters: a partial result of the reduction operation and the next element of
the stream

Combiner – a function used to combine the partial result of the reduction operation when the reduction is parallelized,
or when there's a mismatch between the types of the accumulator arguments and the types of the accumulator
implementation

Если начальное значение опущено, то при первом обращении к редуктору используются первые два элемента потока. Это
полезно, когда для операции reduce не существует разумного начального значения и возвращается экземпляр типа Optional .
        </td>
    </tr>
    <tr>
        <td>
.summaryStatistics()

IntSummaryStatistics

min , max , average и sum
        </td>
        <td>
IntSummaryStatistics statistics = Arrays.asList(
new Person("vlad", 23), new Person("max", 32), new Person("dima", 12), new Person("bob", 54))
.stream()
.mapToInt(p -> p.getAge())
.summaryStatistics();Stream.parralel()

Collection.parralelStream()

System.out.printf("Max: %d, Min: %d, Ave: %f, Sum: %d", statistics.getMax(), statistics.getMin(),
statistics.getAverage(), statistics.getSum());
        </td>
        <td>
        </td>
    </tr>
</table>