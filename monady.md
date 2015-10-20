# Don't fear the Monad

![](http://image.spreadshirtmedia.net/image-server/v1/products/115205650/views/1,width=350,height=350,appearanceId=5.png)

## Czym jest programowanie funkcyjne?
```java
static double f (double x) {
    // ...
    return y;
}
```

W programowaniu funkcyjnym funkcje nie są specjalnym tworem. Funkcje to dane.

Dowodem na to jest fakt, że teoretycznie każdą funkcję można zastąpić odpowiednio duża tablicą. Pobieranie wyniku z takiej tablicy jest uniwersalną operacją, ale logika samej funkcji jest zamknięta w danych.

### Czyste funkcje
`int f(int)`

Jeśli używamy czystych funkcji, to możemy mówić o ich szczerości.

```
(f(3), f(3))

let x = f(3)
in (x, x)
```

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

### Jeszcze trochę notacji
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

## Monoidy
### Łączenie

```
(f . g) x <=> f (g x)

(g . f) x <=> g (f x)

h = f . g

h :: ?

h :: a -> a
```

$$f(g(x)) = (f \circ g)(x)$$

### Monoid
Esencją monoidu jest tworzenie z dwóch bytów danego typu nowego, tego samego typu.

Dodatkowo zdefiniowana operacja musi być przechodnia:
$$
\forall_{x,y,z \in \mathbb{R}} (x + y) + z = x + (y + z)
$$
Oraz element neutralny:
$$
\exists_{\eta}\forall_{x \in \mathbb{R}} x + \eta = \eta + x = x
$$

Przykłady: $$(\mathbb{R}, *, 1)$$, $$(\mathbb{R}, +, 0)$$

Tarcza zegara: $$(\{1,2,3,4,5,6,7,8,9,10,11,12\})$$

## Funkcje #2

## Monady

## Z kamerą wśród monad
### Option (scala)
### Validation (scala)
### List (scala)
### State (scalaz)
### Undo (scalaz)
### Promise (scalaz)
