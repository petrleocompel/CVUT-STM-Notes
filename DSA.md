# Datové struktury
## Informace
- 4 úkoly
- 1 test na konci semestru
- zkouška
 
### Liternatura
- Introduction to Algorithms, Third revision (Cormen)

### Zkouška
- písemná i ústní část

## O předmětu
- analýza algoritmů
- jejich optimalizace
- náročnosti, atd...

## Výpočetní problém
- očekáváné vstupy a výstupy

### Řadící problém
- vstup 
    - sekvence čísel ```(a_1,a_2,...a_n)```
- výstup
    - permutace ```(a_1',a_2',...a_n') : a_1' \le a_2' \le a_n'```
- instance problému
```math
(5,6,1,3,2) \rightarrow (1,2,3,5,6)
```
- velikost instance problému
    - ```n=5```

### Algoritmus
- konečný / nekonečny
- deterministický
- korektnost

program
- implementace algoritmu

Složitost
- operační
    - doba běhu (ms)
    - doba výpočtu
    - počet provedených operací
    - počet transakcí
- paměťová
- 

### RAM (Random access machine)
- (Model počítače)
- má neomezenou paměť (lineární)
- každá instrukce potřebuje 1 jednotku času
 
## Insertion_sort(A)


```
// komentáře = počet instrukcí
j = 2 // 1
while j ≤ A.length { // n 
    key = A[j]; // n - 1
    i = j - 1; // n-1 
    while i > 0 and A[i] > key { // (n-1) * j (každý krok násobíme) 
        A[i+1] = A[i]; // j-1 
        i = i - 1; // j-1
    }
    A[i+1] = key; //n-1
    j++; // n-1
}
```
##### Příkla A
1|2|3|4|5|6
---|---|---|---|---|---
5|1|2|7|2|3
```
execute Insertion_sort(A)
```
1|2|3|4|5|6
---|---|---|---|---|---
1|2|2|3|5|7


#### Loop invariant
- (ověření platnosti tvrzení)
- na začátku
- přes jednotlivé iterace
    - invarianty
    - důkaz pomocí matematické indukce 
    - pomocí indukčího kroku

## 2 přednáška

S(n), g(n) - programová složitost

g(n) = velikost instance
O = funkce
### Definice
```math
O(g(n)) = \{f(n) : \exists_{c >0 } \exists_{n_0 \in \mathbb{N}^+} \forall_{n\ge n_0} f(n)\le c g(n)\}

o(g(n)) = \{f(n) : \forall_{c>0} \exists_{n_0 \in \mathbb{N}^+} \forall_{n\le n_0} f(n) < c g(n)\}


\Omega(g(n)) = \{f(n) : \exists_{c > 0 } \exists_{n_0 \in \mathbb{N}^+} \forall_{n\le n_0}  f(n)\ge c g(n)\}

\omega(g(n)) = \{f(n) : \forall_{c > 0} \exists_{n_0 \in \mathbb{N}^+} \forall_{n\le n_0} f(n) > c g(n)\}

\Theta(g(n)) = \{f(n) : \exists_{c_1 >0 } \exists_{c_2 >0 } \exists_{n_0 \in \mathbb{N}^+} \forall_{n\le n_0} c_1 g(n)\le f(n)\le c_2 g(n)\}

\Theta(g(n)) = O(g(n)) \cap \Omega(g(n))

\omega


f(n) \ge 0

```

---
#### Příklad
```math
n \in^? O(n^2)

n je f(n)

n^2 je g(n)

n \le c* n^2

splneno

```
### důkaz max patří do ```\Theta```

```math

max = (f(n) \ge g(n) \rightarrow f(n)) | (f(n) < g(n) \rightarrow g(n))

max(f(n), g(n)) \in \Theta(f(n)+g(n))

1) f(n) \ge g(n)

f(n) \le c(f(n)+g(n))

2) f(n) < g(n)

f(n) \le c(f(n)+g(n))

```
obojí platí

### důkaz max patří do ```\Omega```

```math
max(f(n), g(n)) \in \Omega(f(n)+g(n))

1) f(n) \ge g(n)

f(n) \ge c(f(n)+g(n))

2) f(n) < g(n)

f(n) \ge c(f(n)+g(n))

```

### Příklad
```math
2^n \in O(n!)
```
Důkaz indukcí
```math
2^n \le n!
```
1) 2.k 
```math
n = 4 

2^4 \le 4!

16 \le 24
```
2) Indukční předpoklad platí pro
```math
2^n \le n!
```
2) důkaz pro n+1
```math
2^{n+1} \le (n+1)!

2*2^{n} \le (n+1) * n!

\frac{2}{n+1} 2^n \le n!
```
Tato nernovost je platná

### Důkaz

```math
log_b(n) \in \Theta(log_a(n))
```
Vyjádření 1 definicí ```\Theta```
```math
c_1log_a(n) \le log_b(n) \le c_2log_a(n)

c_1\frac{log_b(n)}{log_b(a)} \le log_b(n) \le c_2\frac{log_b(n)}{log_b(a)}
```
a pokud zvolíme
```math
c_1 = c_2 = log_b(a)

n_0 = 1
```
Tak nerovnost platí a dokázali jsme že 
```math
log_b(n) \in \Theta(log_a(n))
```

### Domácí procvičení
```math
3^n \in^? O(2^n)
```


---

## Rekurzivní algoritmy

Rekurentní zápis


mergesort
```math
T(n)=T([\frac{n}{2}])+T([\frac{n}{2}])+\Theta(n) = 2T(\frac{n}{2})+\Theta(n)
```

Master theorem
```math
T(n)=aT(\frac{n}{b})+f(n)

a=2

b=2

f(n)=\Theta(n)
```

Několik variant výsledku

Varianta 1
pokud 
```math
f(n)=O(n^{\log _b {(a)}-\epsilon}) ; \epsilon > 0 
```

pak
```math
f(n)=\Theta(n^{\log _b {(a)}})
```

Varianta 2
pokud 
```math
f(n)=\Theta(n^{\log _b {(a)}} \log ^k {n}) ; k \ge 0 [k = 0] 
```
časko k = 0 nejvíce
pak
```math
f(n)=\Theta(n^{\log _b {(a)}} \log ^{k+1} {n})
```

Varianta 3
pokud 
```math
f(n)=\Omega(n^{\log _b {(a)}+\epsilon}) ; \epsilon > 0; 
```
a pak splňuje regularitní podmínku
```math
af(\frac{n}{b}) \le cf(n) ; c < 1
```
pak
```math
f(n)=\Theta(f(n))
```


##### Příklad theoremu
```math
T(n) = 2T(\frac{n}{2}) + n lgn


a=2

b=2

f(n) = n\log (n)

n^{\log _2 2} = n

n\log (n) \in \Omega(n^{1+\epsilon})=\Omega(n+n^{\epsilon})

```

takové n neexistuje. Takže na tohle nelze použít master theorem. Lze ukázat limitou.

Následuje použití jedno z dalších možností řešení
1. substituční metoda - což je matematická indukce
2. Strom rekurze

##### Příklad - stromu
```math
T(n) = 3T([\frac{n}{2}]) + n

T(n) = 3T(\frac{n}{2}) + n
```

Hodnota leveleu, uzly, hloubka
```math
l = \frac{n}{2}
```
pocet uzlu n urovně
```math
3= na l
```

hloubka d
```math
\frac {n}{2^d} =  1 \Rightarrow 2^d = n

d = \log(n)
```

přečíst triky substituční - subtleties kapitola 4.3

T(n) = T(n-1)+n 

nelze master theoremem protože se nedělí na stejné části




#### Sort algoritmy

 - insertion
 - selection
 - merge sort
 - quick sort
 - heap sort



## Pravděpodobnost

Pravděpodobnostní indikátory

> indikují zda daný jev nastal či ne

### Randomize in place



## Quicksort

### Interface
```math
    put (k, v)
    
    get (k)
    
    contains(k)
```

Nejrychlejší možné procházení = asociativní array

#### Hashování typu Chaining
>Přímé adresování - Direct addressing

Existují kolize - a jednotlivé typy tyto kolize řeší

Hash funkce může pro 2 různé indexy vyhodit stejné hash indexy

V tomto případě


Zaplněnost tabulky
n = počet prvků
m = počet řádků v tabulce
```math
\alpha = \frac{n}{m}
```

##### Kapacita - příklad 

```math
m = kapacita

\alpha = 1
```
Pro vložení m + 1 prvku bylo 2m+1 práce.

Což je konstantní složitost.

```math
\frac{2m+1}{m+1} \in \Theta(1)
```

- funkce -
```math
h(k) = k*mod(m)
```

##### počítání
Počet koliz pro dané n,m
```math
n, m

X = |\{\{k,l\} : k \ne l \& h(k) = h(l) \}|
```

Střední hodnota
```math
E[X]

X = \sum_{k \ne l} X_{kl}

X_{kl} .. | \{ kolize \{k,l\}\}|

E[X_{kl}] = Pr\{kolize\{k,l\}\} = \frac{1}{m}

E[\sum_{k \ne l} X_{kl}] = \sum_{k \ne l} E[X_{kl}] = \sum_{k \ne l} \frac{1}{m} = \frac{1}{m} \sum_{k \ne l} 1 = N nad 2 \frac{1}{m}= \frac{n!}{2(n-2)!} \frac{1}{m}

= \frac{n(n-2)!}{2m} 

```

#### Hashování typu - Linear probing
 
> nejvíce v systému 
 

Více proudů = při stejné hodnotě zařadí na další řádek
```math
h(k,i) = (h(k)+i) mod (m)
```

#### Hashování typu - Quadratic probing

```math
h(k,i) = (h(k)+c_1i +c_2i^2) mod (m)
```

##### Příklad
```math
c_1 = 0
c_2 = 1

h(k,i) = (h(k)+c_1i +c_2i^2) mod (m)
```


#### Hashování typu - Double hashing

>využití dvou hash funkcí

```math
h(k,i) = (h_1(k)+ih_2(k)) mod (m)
```