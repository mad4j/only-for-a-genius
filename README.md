# Only for a Genius

*Il 95% di voi non sarà capace di dare la risposta corretta al seguente problema.*

Trovo molto spesso sul web (a dire il vero il più delle volte su Facebook) problemi pseudo-matematici che cercano di attirare click proponendo quesiti banali o che, al più, nascondono qualche noiosa ambiguità di notazione. Un po' poco soddisfacente per chi vuole sgranchirsi un po' la mente.

Questa pagina presenta qualche contributo che, spero, . 

## Episodio 01

![Episodio 01](only-for-a-genius-ep01.png)


## Episodio 02

Si tratta di trovare il numero che, logicamente, sia la continuzione della sequenza.

![Episodio 02](only-for-a-genius-ep02.png)


## Episodio 03

Quale numero non ha nulla in comune con gli altri?

![Episodio 03](only-for-a-genius-ep03.png)


## Episodio 04

![Episodio 04](only-for-a-genius-ep04.png)


## Episodio 05

![Episodio 05](only-for-a-genius-ep05.png)

## Episodio 06

![Episodio 06](Problema01.png)


# Le soluzioni

## Episodio 01

Si tratta di scomporre un numero in due fattori.
Tenendo conto dei soli numeri positivi, i valori cercati sono:

:pear: = 127

:apple: = 9721

Quindi la soluzione è **9.848**.

Il seguente programma è capace di scomporre il valore **N** in fattori primi:

```c++
#include <stdio.h>

int main() {
    int N = 1234567;
    for (int i=2; i<=N; i++) {
        while (N%i == 0) {
            printf("%d ", i);
            N /= i;
        }
    }
}
```


## Episodio 02

Il numero cercato è **363**.

Infatti le cifre di un numero in sequenza sono il conteggio delle lettere che descrivono la cifra corrispondente del numero che precede.
Esempio: **5 0 7** (cinque zero sette) -> **6 4 5**.

Ovviamente questa soluzione ha senso solo nella lingua italiana.

Da osservare che il numero tre e' l'unico punto fisso di questa trasformazione (i.e. F(3) = 3) e che tutte le cifre tenderanno a questo valore.

E' possibile verificare visivamente questa proprietà inserendo in un grafo orientato tutte le transizioni possibili.

```
digraph G {
    0 -> 4
    1 -> 3
    2 -> 3
    3 -> 3
    4 -> 7
    5 -> 6
    6 -> 3
    7 -> 5
    8 -> 4
    9 -> 4
}
```

![Episodio 02 - Sequenza](resources/only-for-a-genius-ep02-sequence.png)


## Episodio 03

Il numero cercato è **3754**.

Tutti gli altri numeri hanno 18 come somma delle loro cifre.


## Episodio 04

Il numero cercato è **1012**.
Sono delle semplici somme in base 3.


## Episodio 05

È la lettera **P**. 

Sono tutte le lettere dell'alfabeto che non hanno elementi di simmetria.

*Inserire diagramma di Venn*

