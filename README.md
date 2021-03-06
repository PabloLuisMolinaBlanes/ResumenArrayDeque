# ArrayDeque

Implementación de la interfaz Deque. Puede variar su tamaño conforme se vaya necesitando, por ende, no teniendo restricciones en su capacidad (no más allá de la capacidad de almacenamiento en RAM). Sin sincronización externa, son no recomendables para programación concurrente. No se permiten elementos null. Parece ser más rápida que Stack usada como Stack y más rápida que LinkedList usada como queue.

La mayoría de operaciones corren en tiempo constante amortizado (es decir, siempre tardará lo mismo), excepto contains, iterator y las relacionadas con remove, que corren en tiempo lineal amortizado.

Si el Deque se modificase después de crearse el iterador, más allá de su método remove(), se producirá una ConcurrentModificationException. Esta excepción solo se debe usar para evitar errores, por lo que un programa no debe usar esta excepción para asegurar que exista una modificación concurrente no sincronizada.

Hay tres métodos constructores. En el primero (ArrayDeque()), se construye un Array Deque vacío, en el segundo (ArrayDeque(int integer)), se le da una capacidad inicial, aunque extendible, y en el tercero (ArrayDeque(Collection<? Extends E> c), el ArrayDeque admitiría solo valores de la clase detrás de 'Extends'.

Métodos propios de la clase (no provenientes de su extensión) incluyen 'getFirst()', 'getLast()', 'pop()', 'push(E e)', 'removeFirst()' y 'removeLast()'.

Ejemplos de su uso:

```java

import java.util.ArrayDeque;
public class arraything {
	public static void main(String[] args) {
		ArrayDeque<String> array = new ArrayDeque<>();
		array.add("Cat");
		array.add("God");
		System.out.println(array.size());
		System.out.println(array.getFirst());
		System.out.println(array.getLast());
		array.removeLast();
		array.removeLast();
		System.out.println(array.size());
	}
}

```
Resultado:

```sh
2
Cat
God
0

```


```java

import java.util.ArrayDeque;
public class arrays {
	public static void main(String[] args) {
		ArrayDeque array = new ArrayDeque<>();
		array.add("Cat");
		array.add(1);
		array.add(2);
		array.add(true);
		array.add("God");
		System.out.println(array.size());
		System.out.println(array.getFirst());
		System.out.println(array.getLast());
		array.removeLast();
		array.removeLast();
		System.out.println(array.size());
	}
}


```
Resultado:

```sh
5
Cat
God
3

```
