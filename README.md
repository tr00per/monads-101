# Don't fear the Monad

![](http://image.spreadshirtmedia.net/image-server/v1/products/115205650/views/1,width=350,height=350,appearanceId=5.png)

* [Don't fear the Monad](https://channel9.msdn.com/Shows/Going+Deep/Brian-Beckman-Dont-fear-the-Monads) - Brian Beckman
* [Monads Made Difficult](http://www.stephendiehl.com/posts/monads.html) - Stephen Diehl
* [Functors, Applicatives, And Monads In Pictures](http://adit.io/posts/2013-04-17-functors,_applicatives,_and_monads_in_pictures.html) - Aditya Bhargava

## Czym jest programowanie funkcyjne?
```java
static double f (double x) {
    // ...
    return y;
}
```

W programowaniu funkcyjnym funkcje nie są specjalnym tworem. Funkcje to dane.

Dowodem na to jest fakt, że teoretycznie każdą funkcję można zastąpić odpowiednio duża tablicą. Pobieranie wyniku z takiej tablicy jest uniwersalną operacją, ale logika samej funkcji jest zamknięta w danych.

## Funkcje #1
### Notacja typów
`int x;`

$$x \in \mathbb{Z}$$

`x :: Int`

`f :: Int -> Int`

### Generyki
`x :: a`

`f :: a -> a`

```java
static <A> A f (A x) {
    //...
    return y;
}
```

### Łączenie
```
x :: a
f :: a -> a
g :: a -> a
```

```
g(x)

f(g(x))

f(x)

g(f(x))

```

```
g x

f (g x)

f x

g (f x)
```

```
(f . g) x <=> f (g x)

(g . f) x <=> g (f x)
```

$$f(g(x)) = (f \circ g)(x)$$


## Monoidy

## Funkcje #2

## Monady
