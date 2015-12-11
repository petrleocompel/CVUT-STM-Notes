# Matematika pro informatiku
## Informace
- Grant - Vinebil
- Webs = Hrkadla, Velebil, Habala

### Poznatky

- všímat si základního kroku

### Literatura
- Diskrétní matematik - J.Velebil (Pročíst)
- Discrete Mathemamatics and its Application - K.H.Rosan (1070 stran)
- Cyklické kódy - Jiří Adámek (Polynomy nad Z, modulo, atd...)

### Zápočet
- formální zápočet - pouze 

### Zkouška
- doplnit
- 2 hodiny

## Číselné systémy
### O kapitole
- přirozená čísla, systémy
- nakonec RSA alg.
 

#### Poznatky
- Nutno zjišťovat co to je IP
- Pozor na základní krok
- označit krok kde lze položit IP (kdy nastala dekompozice)
- IP je bohatší než původní krok -> silný princim matematické indukce (více výroků) eqvivalentní se standartní

### Přirozená čísla
#### Co to jsou přirozená čísla?
> Tvoří matematickou strukturu 

#### Axiomatický systém
(Množina, Binární [Unární] operacece, vybraný prvek)

```math
( \mathbb{N}, \sigma, 0)
```

```math
1) 0 \in \mathbb{N}, \mathbb{N} (-> ^ (\sigma)) \mathbb{N}
2) \sigma je injekce  x \ne y => \sigma x \ne \sigma y |=| \sigma x = \sigma y => x = y
3) 0 \in \sigma (\mathbb{N}) 0 \in \mathbb{N} \ \sigma (\mathbb{N})
4) 0 \in A \& (\forall n \in \mathbb{N} ) (n \in A => \sigma n \in A) => \mathbb{N} \subseteq A) mat. injekce
```

 Indukční předpoklad = IP
 
 ```math
 n \in N \& n \in A => \sigma n \in A 
 ```
 
 ##### Příklad
 Ukažte že platí
  ```math
 Z^{n}_{k=1} k = \frac{1}{2}n(n+1)
 ```
 ```math
 A = \{n \in \mathbb{N} | Z^{n}_{k=0} k = \frac{1}{2}n(n+1)\}
```
```math
 0 \in A |=| Z^{0}_{k=0} k =^? \frac{1}{2}0(0+1)
 ```

Platí
```math
Z^{n}_{k=0} k = \frac{1}{2}n(n+1)
```
Dokázáno n
Indukční krok n+1
```math
Z^{n+1}_{k=0} k = Z^{n}_{k=0} k + (n+1) = \frac{1}{2}n(n+1) + (n + 1) = (n+1)(\frac{1}{2}n+1)=\frac{1}{2}(n+1)((n+1)+1)
 ```
 dokázáno n i n+1
 To znamená že každé číslo je elementem A neboli je element Sigma
 
####Jiný axiomatický systém
##### Peano - Lawvere
- jiný pohled na věc.

> Na základě komunikace mezi jinými objektů se určují jeho vlastnosti za pomoci morfismů.


---

###### Poznámka - Morfismus 

> Funkce jenž obraz vybranýho prvku musí být rovne jiné struktuře.

- může být isomorfismus
- mohou být identická zobrazení
- Když zkoumáme jednu získáváme výsledky druhé

---

- nutno říct co zde považujeme za morfismus
- 

```math
( X , f, u) \rightarrow^s (Y,g,v)
```
```math
( X , f, u) \rightarrow^s (Y,g,v)
```
Morfismus považuje funkce z X do Y taková že respkektuje

Poznámky paper1
 ! = pouze jeden
```math
\forall (X, f, y) \exists ! (\mathbb{N}, \sigma, 0) \rightarrow^S (X, f, y)
```
paper 2

foto mobil
---
```math
X \rightarrow^f X = f \circ f ...  f \circ f
```
```math
f^n = \mathbb{N} \rightarrow^{\sigma} \mathbb{N}
```

```math
f^0 := id_x = \sigma
```
```math
f^{\sigma (n)} := f \circ f^n
```

Pokud platí inkučnost výše pak
```math
(\forall m  \in \mathbb{N})(\forall m  \in \mathbb{N})(f^m \circ g^n = g^n \circ f^m)
```
a z toho
```math
m \ in A
```

```math
0 \in A |=| (\forall m  \in \mathbb{N})(f0m \circ g^n = g^n \circ f^0)
```
z toho 
```math
g^n = g^n
```
což je pravda

jiný pohled

```math
m \in \mathbb{N}
```
```math
(\forall n \in \mathbb{N})(f^m \circ g^n = g^n \circ f^m)
```
```math
n \in A \leftrightarrow f^m \circ g^n = g^n \circ f^m
```
z čehož vyplívá
```math
\mathbb{N} \subseteq A
```

Operace unární
```math
\sigma
```

```math
\mathbb{N} \rightarrow^{\sigma} \mathbb{N}
```

Zde bude vyplávat že násobení je komutativní a součet také

```math
m,n \in \mathbb{N}
```

```math
m+n := \sigma^n(m)
```
```math
m*n := (\sigma^m)^n 0
```
```math
m+0 := m
```
```math
m+\sigma n = \sigma^{\sigma n}(m) = \sigma \circ \sigma^n (m) = \sigma (m+n) 
```
```math
m \le n \leftrightarrow (\exists x \in \mathbb{N})(n=m+x)
```
```math
m < n \leftrightarrow m \le n \& m \ne \leftrightarrow \exists x \in \mathbb{N} (lomene minus) \{0\} (n=m+x)
```
```math
\mathbb{N} (lomene minus) \{0\}= \mathbb{N}^+

```

a nakonec laborování zase doma

```math
(\mathbb{N},\sigma,0)
```
že sčítání je komutativní asociativní a neutrální
že násobení je komutativní asociativní a neutrální
pak
```math
m+n = k+n => m=k
```
```math
m*n = k*n \& n \neq 0 => m=k
```

distributivní

```math
m+n = 0 \rightarrow m=n=0
m*n = 1 \rightarrow m=n=1
```

#### Uspořádání
- možina na které je binární relace a je relfexivní, symetrická a tranzitivní
```math
(X,\le)
```
```math
A \subseteq X
```
```math
A^{\vartriangle} \{ x \in X |(\forall a \in A)(a \le x)\}
```
```math
A^{\triangledown} \{ x \in X |(\forall a \in A)(a \ge x)\}
```
MAX
```math
\{max(A)\} = A \cap A^{\vartriangle} 
```
MIN
```math
\{min(A)\} = A \cap A^{\triangledown}
```


supremum
```math
sup(A) = min(A^{\vartriangle})
```
infimum
```math
inf(A) = max(A^{\triangledown})
```
```math
\emptyset \ne A \subseteq \mathbb{N} => A \subset A^{\triangledown} \ne \emptyset
```
```math
\emptyset \ne A \subseteq \mathbb{N} \& A \subset A^{\triangledown} = \ne \emptyset
```
```math
\mathbb{N} \subseteq A_{\triangledown} \emptyset \ne \mathbb{N} \cap A \subseteq A^{\triangledown} \cap A = \emptyset
```

což ukazuje mat indukce <=> princip dobrého uspořádání

např dokázání sporem že nic mezi 0 a 1 neleží <img src="https://s.tylingsoft.com/emoji-icons/blush.png" width="18"/>

fermatova věta 
```math
n \ge x^n+y^n=z^n
```
- díky téhle rovnici bylo založeno mnoho odvětví (křivkové integrály atd...)


---
## Opakování přechozí kapitoly

```math
(\mathbb{N}, \sigma, 0) \mathbb{N} \rightarrow^(\sigma)\mathbb{N}

\sigma (n) = n+1 ; 0 \in \mathbb{N}

0 |->^\sigma 1 |->^\sigma 2 |->^\sigma 3 |->^\sigma

0 \in A \& (\forall n \in \mathbb{N})(n \in A => \sigma n \in A) => \mathbb{N} \subseteq A
(\forall n \in \mathbb{N})(n \in A => \sigma n \in A) = \sigma (A) \subseteq A

```

## Množiny def. indukcí


header 1 | header 2
---|---
I | množina počátečních prvků
```\mathbf{R}``` | Systém realcí parity ≥ 2 (odvozovací parita)
Q \in ```\mathbf{R}``` | ```(x_1,...,x_n,y) \in Q \rightarrow``` y je odovozeno pravidelm Q z prvků ```x_1,...,x_n```
```a \in I``` | 



V pc technice 
```math
\frac{x_1,x_2,...,x_n}{y}(Q) \leftrightarrow (x_1,...,x_n,y) \in Q

\frac{}{a}  I \cup R
```

Objekt typu string je nad abeceda ```\Sigma = \{0,1\}```
```math
S::=  0|1|S0|S1

I = \{0,1\}

R = \{\frac{S}{S0},\frac{S}{S1}\}
```

----

```math
I = \{0\}

\mathbf{R} = \{\sigma\}
```
####Definic Nechť T je množina ```Q \in \mathbf{R}```
- ```Q(T) = \{y | (\forall x_1,...,x_n \in T)((x_1,...,x_n) \in Q)\}```
- ```\mathbf{R}(T) = UQ(T) [Q \in \mathbf{R}]```
- ```T``` je ```Q``` - uzavřená ```: \leftrightarrow Q(T) \subseteq T```
- ```T``` je ```\mathbf{R}``` - uzavřená ```: \leftrightarrow \mathbf{R}(T) \subseteq T```

##### Na doma
```math
Q \in \mathbf{R}

Q(\emptyset) = \emptyset
\mathbf{R}(\emptyset) = \emptyset
S \subseteq T \rightarrow Q(S) \subseteq Q(T) \& \mathbf{R}(S) = \mathbf{R}(T)
```


####Definice Množina L je induktivně def. množina I a systém relací ```\mathbf{R}``` arity ≥ 2

```math
: \leftrightarrow
```
1. ```I \subseteq L```
2. ```L je \mathbf{R} uzavřená \mathbf{R}(L) \subseteq L```
3. ```I \subseteq T \& \mathbf{R}(T) \subseteq T \rightarrow(double) L \subseteq T ```
> Strukturální indukce

Těmito 3 podmínkami je definovaná množina. A existuje jedna jediná. Pokud by existovalo více byli by identické. 

####Uzávěr množiny I 
```math
L = C|(I,\mathbf{R})
```
1. ```I \subseteq C|(I, \mathbf{R})```
2. ```\mathbf{R}(C|(I,\mathbf{R})) = C|(I,\mathbf{R})```
    . ```C|(C|(I,\mathbf{R}), \mathbf{R}) = C|(I,\mathbf{R})```
    . ```C|(\emptyset,\mathbf{R}) = \emptyset```

```math
Set \rightarrow^\psi Set

X |-> I \cup \mathbf{R}(x)

x_0:=I

x_{n+1}:=\psi (x_n) = I\cup \mathbf{R}(x_n)
C|(I,\mathbf{R}) = UX_n [n \in \mathbb{N}]
```

----
```math
(\mathbb{N}, \sigma, 0)

R = \{\sigma\}

I=\{0\}

x_0 = \{0\}

x_1 = \{0\} \cup \mathbf{R}(x_0) = \{0,1\}

x_2 = I \cup \mathbf{R}(x_1) = \{0,1,2\}
```
----
```math
(\mathbb{R},+,0,*,1,\leq)

I=\{0\}

R = \{\sigma, \tau \}

\sigma(x) = x+1

\tau(x) = x-1

z = C|(I, \mathbf{R})
x_0 = \{0\}

x_1 = I \cup \mathbf{R}(x_0) = {0} \cup {-1,1} = {-1,0,1}

x_2 = {-2,-1,0,1,2}
```
----
```math
C|(I,\mathbf{R}) \subseteq M

1. I \subseteq M \& \mathbf{R} \subseteq M \rightarrow(double) C|(I,\mathbf{R}) \subseteq M
```
####Definice posloupnost ```x_0,x_1,...,x_n```, ```n \geq 0``` se nazývá ```(I, \mathbf{R})``` Derivace
```math
\leftrightarrow x_0 \in I \& \forall i \in (1, ..., n) x_i \in I \cup \mathbf{R}(\{x_0,x_1,...,x_{i-1}\})
```

x má ```(I,\mathbf{R})``` derivaci ```\leftrightarrow``` existuje posloupnost ```x_0,x_1,...,x_n``` která je ```(I,\mathbf{R})``` drivaci ```\& x_n = x``` 

```math
C|(I, \mathbf{R}) = \{x|x ma (I, \mathbf{R}) - derivaci\}
```

---
##### Ukázka
```math
\Sigma = \{a,b,c\}

\Sigma^* = \{ \varepsilon \} \cup \{ x_1....x_n | n \in \mathbb{N} \& x_i \in \overline{Z}\}

\overline{Z}^* = C|(I, \mathbf{R})

I = \{\varepsilon \}


1) C|(I, \mathbf{R}) \subseteq \overline{Z}^*

I\subseteq \overline{Z}^*, \mathbf{R}(\overline{Z}^*) \subseteq \overline{Z}^*
```

---
##### Ukázka
```math

(\mathbf{R}, +, 0, *, 1, \leq )

I = \{2\}

\mathbf{R} = \{\frac{x,y}{x+y} (+)\}

(+) = \{(x,y,x+y) | x,y \in \mathbb{R})

C|(I, \mathbf{R}) = 2\mathbb{N}^+ = \{2,4,6,8,...\} 

1) I \subseteq 2\mathbb{N}^+
2) 2\mathbb{N}^1 = R \rightarrow R(2\mathbb{N}^+) \subseteq 2\mathbb{N}^+

    x \in \mathbf{R}(2\mathbb{N}^+) = (+)(2\mathbb{N}^+)
    
C|(I,\mathbf{R}) \subseteq 2\mathbb{N}^+
```

---
##### Obrácená inkluze
```math
V = \{k z\in \mathbb{N}^* | 2k \subset (I,\mathbf{R}) - derivaci\}

Predpoklad

\mathbb{N}^+ \subseteq V

1 \leftarrow V \leftrightarrow 2 ma(I,\mathbf{R} - derivaci)
```
> nechť ```k \in V, 2k ``` má ```(I,\mathbf{R})``` - derivaci ```2, x_1,x_2,...,2k,2k+2```

>```2(k+1)``` má ```(I,\mathbf{R})``` - derivaci ```\Rightarrow``` tutíž ```k+1 \in V```

#### doma 
Abeceda
```math
\overline{Z} = \{a,b\}, \overline{Z}^*

M = {w_1abw_2 | w_1,w_2 \in \overline{Z}^*}

```
- zadejte množinu M induktivně
- Ověření faktů že množina M je iduktivně definováná množina  ```M = C|(I, \mathbf{R})```

2 uloha

```math
w_1 \in \overline{Z} = \{a_1, a_n\}

M = \{w_1, ..., w_n | n \in \mathbb{N}^+ \& revers(w_1,...,w_n) = w_1,...,w_n\}

M = C|(I, \mathbf{R})
```

## Rekurentní rovnice
Neznámá je posloupnost

```math
\forall n \in \mathbb{N}

x(n+2) - 3x(n+1) + 2x(n)= y(n)

x(n) = \lambda^n

\lambda^{n+2} - 3\lambda^{n+1} + 2\lambda^{n} = 0

\lambda^{4}(\lambda^{2} - 3\lambda + 2) = 0

res.

x(n) = c_1\lambda^{n}_1+c_2\lambda^{n}_2

\{\lambda^{n}_1,n\lambda^{n}_2\}


```


```math 
(X, *) grupoid - polo grupa dohromady

A. \_ \_ a(bc) = (ab)c - polo grupa dohromady


N. 1a = a1 

I. aa^{~}= a^{~}a = 1

----

K. ab=ba  - komutativni \{grupoid, pologrupa, Monoid, grupa\}
```

pologrupa = (X, *) a A. \_ \_ a(bc) = (ab)c
Monoid (magma) = A. \_ \_ a(bc) = (ab)c a N. 1a = a1 
grupa = N. 1a = a1  a I. aa^{~}= a^{~}a = 1

```math 

Monoid

(X, +, 0, (-), *, 1) - okruh

x,+,0,(-) = komutativni grupa 
x,*,1 = Monoid


D._+: 

a*(b+c) = ab+ac
(b+c)*a = ba+ca
```

```math 

0 \ne 1 ... netrivialni

K_. ... komutativni okruh

a\ne0, b\ne0, a*b\ne0
```

---
#### Celá čísla

```math 
(\mathbb{Z},+, 0, (-), *, 1) - okruh

netrivialni \& komutativni \& bez delitelu 0

0\ne1

a*b = b*a

a\ne0, b\ne0 \Rightarrow a*b\ne0

```
#####Obor integrity
```math 
\mathbb{M} \subseteq \mathbb{Z}, m,n \in \mathbb{Z} m \le n \leftrightarrow (\exists x \in \mathbb{N})(n=m+x)

tridolamine

m<n, m=n, m>n

\mathbb{Z}^+ = \{m \in \mathbb{Z} | 0 < m\} = \mathbb{N}^+
\mathbb{Z}^- = \{m \in \mathbb{Z} | m < 0\}

m*n = 1 \leftrightarrow n = m = 1 or n = m = -1

\mathbb{Z}^* = \{-1, 1\}
\mathbb{R}^* = \mathbb{R} \ {0}

mn < mk, m> 0 \rightarrow n < k

m<n \leftrightarrow m+1 \le n \leftrightarrow n-1

m+x = n  / +(-m)

0+x = n + (-m)

x = n-m

---

A^\triangle A^\triangledown

\emptyset \ne A \subseteq \mathbb{Z} 

A^\triangledown \ne \emptyset \Rightarrow A \cap  A^\triangledown \ne \emptyset

A^\triangle \ne \emptyset \Rightarrow A \cap  A^\triangle \ne \emptyset

```

----
 ```math 
 -(-m) = m, (-1)m = -m, mn = (-m)(-n) = -(m(-n)) = ((-m)(n))
 ```
----
#####Dělitelnost v ```math \mathbb{Z},\mathbb{N}```
Důkaz
```math 
 a,b \in \mathbb{Z}
 
 a|b \leftrightarrow (\exists x \in \mathbb{Z})(b = ax)
 a|_Nb \leftrightarrow (\exists x \in \mathbb{N})(b = ax)
 ```
 Vlastnosti
 
 1. ```math a|b \leftrightarrow -a|b \leftrightarrow a|-b \leftrightarrow -a|-b```
 2. ```math a|a```
 3. ```math a|b \& b|c \Rightarrow a|c```
 4. ```math a|b & b|a \Rightarrow a=b \vee a=-b```
 
---

```math \mathbb{Z}```
pro které platí 
```math 1|a \Rightarrow \subseteq D(a) = \{x\in\mathbb{Z} | x|a \} \{-a,-1,1,a \} ```

a|0         0|0

```math a|b & a|c \rightarrow a | mb+nc```

```math ac|bc & c\ne 0 \rightarrow a|b ```

```math a|1 \leftrightarrow a\in \{1,-1\}```

```math 0|a \Rightarrow a = 0```


#####Důkaz prvočísla - čísla složená
1. ```math a \in \mathbb{Z}``` se nazývá prvočíslo ```math \leftrightarrow a \notin \{-1,0,1\} & D(a) = \{-a, -1, 1, a\}```
2. ```math a \in \mathbb{Z}``` se nazývá složené č. ```math \leftrightarrow a \notin \{-1, 0, 1\} & D(a) \ne \{-a, -1, 1, a\}```


```math M = \mathbb{Z}\{-1,0,1} ``` Rozklad ```math \mathbb{Z}```

```math
x \in M * M \leftrightarrow x = mn, 

\mathbb{P} = (M\setminus M * M) \cap \mathbb{N}

-\mathbb{P} = (M\setminus M*M) \cap (-\mathbb{N})
```

Chceme dokáazat (ukázka)
```math
x\in M \setminus M*M  \rightarrow D(x) = \{-x,-1,1,x\}

neboli

x\in M \setminus M*M \& D(x) \supset \{-x,-1,1,x\}

a\in D(x) \& a \notin \{-x, -1, 1, x\}

x = a * b \ne 0 [a\in M, b\in M]

a \ne 0, b \ne 0

x \in M * M

```

---

#### pro každé číslo existuje přepis na prvočísla

tvrzení
```math
\forall x\in \mathbb{N}, x \ge2 \exists n \in \mathbb{N} \exists \{1,2,...,n\} \rightarrow^p \mathbb{P} : x=p_1,p_2...p_n


(jev) V(x) = \exists n \in \mathbb{N} \exists \{1,2,...,n\} \rightarrow^p \mathbb{P} : x=p_1,p_2...p_n 
```
Dokazujeme
```math
V(2) \{1\} \rightarrow^p \mathbb{P} p_1 = 2

n \in \mathbb{N}, V(2), V(3), ..., V(n)

n\ge2

n+1 \rightarrow2 varianty

n+1 \in \mathbb{P} \rightarrow n+1
n+1 \notin \mathbb{P} \rightarrow n+1 = a*b [a,b \notin \{-1,0,1\}]
```

Tudíž indukčně platí jeden z výroků a
```math
 n+1 = p_1 ... p_*{n_1} q_1 ... q_*{n_1} 
```
#### Největší společný dělitel

tvrzení
```math a,b \in \mathbb{Z}  d \in \mathbb{N}``` se nazývá
největší společný dělitel 

1. ```math d|a \& d|b```
2. ```math x|a \& x|b \rightarrow x|d```

> ```math gcd(a,b) := d```

#### Nejmenší společný násobek

tvrzení
```math a,b \in \mathbb{Z}  l \in \mathbb{N}``` se nazývá

1. ```math a|l \& b|l```
2. ```math a|X \& b|x \rightarrow l|x```

> ```math lcm(a,b) := l```

##### Doma (Triviální výplody)

```math 
gcd (a,a) = |a|

lcm(a,a) = |a|

gcd(a,b) = 0  \Rightarrow a=0 \& b=0

lcm(a,b) = 1 \Rightarrow |a| = 1 \& |b| = 1

gcd(0,a) = |a|

lcm(1, a) = |a|

gcd(1,a) = 1

lcm(0,a) = 0

lcm(a,b) = 0 \leftrightarrow a=0 \sim b=0

gcd(a,b) = gcd(b,a) = gcd(\pm a, \pm b)

gcd(\lambda a, \lambda b) = |\lambda| gcd(a,b) 

lcm(a,b) = lcm(b,a) = lcm(\pm a, \pm b)

lcm(\lambda a, \lambda b) = |\lambda| lcm(a,b)
```

### Euklidův algoritmus
Věta
> Pro každé celé číslo 

```math
(\forall a \in \mathbb{Z})(\forall b \in \mathbb{Z} \setminus\{0\})(\exists! q \in \mathbb{Z})(\exists! r\in \mathbb{Z})
```

ukázka

```math
a= bq+r

0 \le r <|b|

\emptyset \neq M = \{a-bq | q \in \mathbb{Z}\} \cap \mathbb{N}

r := min(M)

a = bq+r = bq + |b| + r-|b|
a = |b|(-neco-sgn- bq + 1) + (r-|b|)

r \le r- |b|

|r_1-r_2| = |b||a_1-a_2|

r_1,r_2 \in \{0,1,...,|b|-1\}

r_1 = r_2
```

pokud je tedy b pevně dáno lze se na to dívat jako

```math
a \rightarrow (q, r)

<a>_b = - neco -
```
---

Užití např s gausovou eliminací
```math
D(a) \cap D(b)


```

---

### Euklidův alg. rozšířený

Je dána dvojice celých čísel

```math
a,b \in \ mathbb{Z}

FOTO 3
```

Věta
1. rozšířený algoritmus pro libovonou dvojici ```math a,b \in \mathbb{Z}``` skončí v konečném počtu kroků
2. jestli pro ```math a,b \in \mathbb{Z}``` skončí s maticí [A,S,T \\ O,U,V] pak platí
    1. ```math gcd(a,b) = A```
    2. ```math gcd(a,b) = Sa+Tb```
    3. ```math lcm(a,b) = |Ua| = |Vb|=|UV|*gcd(a,b)```
    4. ```math gcd(a,b) = \alpha a + \beta b = [x,\beta] = [S,T] + \lambda[U,V]```

Stanovce gcd(17,19) = ```math \alpha```17 + ```math \beta```19
FOTO4+5

---

#####Příklad
```math
3x+5y = 1 (x,y \in \mathbb{Z})

\begin{bmatrix}
3 & 1 & 0\\ 
5 & 0 & 1 
\end{bmatrix}
= [1,x,y]

\begin{bmatrix}
3 & 1 & 0\\ 
5 & 0 & 1 
\end{bmatrix}
~
\begin{bmatrix}
3 & 1 & 0\\ 
-1 & -2 & 1 
\end{bmatrix}
~
\begin{bmatrix}
0 & -5 & 3\\ 
1 & 2 & -1 
\end{bmatrix}


```

```math
\begin{bmatrix}
a^'\\ 
b^' 
\end{bmatrix}
=
\begin{bmatrix}
0 & -1\\ 
1 & -q
\end{bmatrix}
\begin{bmatrix}
q\\ 
b
\end{bmatrix}
=
\begin{bmatrix}
b\\ 
a & -qb
\end{bmatrix}
```

####Věta o dělení

```math
\forall a \in \mathbb{Z}
\forall b \in \mathbb{Z} \\ \{0\}
\exists! \alpha \in \mathbb{Z}
\exists! r \in \mathbb{Z}

a=qb+r \& 0\le r < |b|

0\le<a>_b \le |b|

a=qb+<a>_b
```

ukázka
```math
m | ax-b

ax-b = -ym
ax+ym=b

\begin{bmatrix}
a & 1 & 0\\
m & 0 & 1
\end{bmatrix}
```


###Počítání modulo

```math
a = bq+<a>_b

0\le<a>_b < |b|

m \in \mathbb{Z}, m > 1

\mathbb{Z}_m = \{1,2,...,m-1\}

x,y \in \mathbb{Z}_m

x \oplus y := <x+y>_m

x \otimes y := <xy>_m


0 \oplus y = <0+y>_m = <y>_m = y

1 \otimes y = <1*y>_m = <y>_m = y

(\mathbb{Z},\oplus,\circ,\otimes, 1)
```


```math \oplus ``` | 0 | 1 | 2 | 3
---|---|---|---|---
0 | 0 | 1 | 2 | 3
1 | 1 | 2 | 3 | 0
2 | 2 | 3 | 0 | 1
3 | 3 | 0 | 1 | 2

```math \otimes ```  | 1 | 2 | 3
---|---|---|---
1 | 1 | 2 | 3
2 | 2 | 0 | 2 
3 | 3 | 2 | 1 

```math
\forall x,y,z \in \mathbb{Z} \forall m \in \mathbb{N}

<x+<y>_m> = <x+y>_m

<x*<y>_m>_ = <xy>_

<<x>_m + <y>_m>_m = <x+y>_m

y = q_1m+<y>_m

x+y = q_2m+<x+y>_m

x+<y>_m=q_3m+<x+<y>_m>_m


x+y - q_1m = q_3m+<x+<y>_m>_m

x+y = (q_1+q_3)m +<x+<y>_m>_m

```


Morfismus = Funkce která respektuje operace na sktrukturách


```
sequenceDiagram
Z->>Z_m: f
Z->>x: -
Z_m->>x_m: -
x->>x_m: -
```

```math
f(a+b) = f(a)\oplus f(b)

f(a*b)=f(a)\otimes f(b)

f(0) = 0

f(-a) = \ominus f(a)
```

pokud
```math
f(\mathbb{Z}) = \mathbb{Z}_m
```
Pak je to epimorfismus

> značky v kroužku se nepoužívají => další poznámky jsou v normálních znamínkách

##### příklad
```math
3x+2y = 1 (\mathbb{Z}_4)

[x,y] =
\begin{bmatrix}
3 & 1 & 0\\
2 & 0 & 1
\end{bmatrix}
=
[1,x,y]

---

\begin{bmatrix}
3 & 1 & 0\\
2 & 0 & 1
\end{bmatrix}
~
\begin{bmatrix}
1 & 1 & 1\\
2 & 0 & 1
\end{bmatrix}
~
\begin{bmatrix}
1 & 1 & 1\\
0 & 2 & 3
\end{bmatrix}

(x',y')
\begin{bmatrix}
1 & 1 & 1\\
0 & 2 & 3
\end{bmatrix}
=
[1,x,y]

[x,3]=[1,1]+y'[2,3]


x'1+ y'0 = 1x'

res

[1,1],[3,0],[1,3],[3,2]
```

#### Jiný způsob

```math

(\mathbb{Z}, \oplus,\circ,\otimes,1)

```

```math \oplus ```  | 0 | 1 | 2
---|---|---|---
0 | 0 | 1 | 2
1 | 1 | 2 | 0 
2 | 2 | 0 | 1 


```math \otimes ```  | 1 | 2
---|---|---|---
1 | 1 | 2 
2 | 2 | 1 

Třídy
```math

[0] = 3 \mathbb{Z} = \{...,-6,-3,0,3,6,9,...\}
[1] = 1+3 \mathbb{Z} = \{...,-5,-2,1,4,7,10...\}
[2] = +3 \mathbb{Z} = \{...,-4,-1,2,5,8...\}

```
Alg. vybrání reprezentanta třídy
```math
C_1,C_2 \in \mathbb{Z}_3
```
Plus
```math
C_1 \boxplus C_2, 
x \in C_1,
y \in C_2

x+y \in  C_3

C_1 \boxplus C_2 = C_3
```

Times
```math
C_1 \boxtimes C_2, 
x \in C_1,
y \in C_2

x*y \in  C_3

C_1 \boxtimes C_2 = C_3
```


Pojem Konkuence (a ekvivalence)
```math
X = \cup X_i

i\neq j \Rightarrow X_i \cap X_j = \emptyset

x~y \leftrightarrow(\forall i \in I)(x,y\in X_i)

~ \subseteq X \times X

```
reflexivní
```math
[x] = \{y\in X |y~x\}
```

tranzitivní
```math
X/_~ = \{[x] | x\in X\}

```

Symetrická
```math
\cup[x] = X [x] \neq [y]

x\in X
```

(třídy skoro stejné jako zbytky po dělení)
```math
[x]_m = [y]_m \leftrightarrow m | x-y \leftrightarrow x ~_m y

x ~_m x' \& y ~_m y' \rightarrow

x+y ~_m x' + y'

xy ~_m x' y'

```
Příklad
```math
\mathbb{Z}_m

A \boxtimes X = B

\mathbb{Z}

ax~_m b

m|ax-b

ax+ym=b

\Phi \rightarrow \mathbb{Z}_m

\Phi(ax+ym) = \Phi(b)

\Phi(a)\boxtimes \Phi(x)\boxplus \Phi(y) \boxtimes \Phi(m) = \Phi(b)

A \boxtimes \Phi(x) \boxplus é B

res

A \boxtimes \Phi(x) = B

```





#### Čínská věta o zbytcích 


```math
a_1,...a_n \in \mathbb{Z}, m_1,...,m_n \in \mathbb{N}, m_i \ge 2

i \neq j \Rightarrow g cd(m_i,m_j) = 1

```

Potom všechna řešení soustavy


```math
x= a_1 mod  m_1
x = a_n mod m_n

```
jsou dána  

```math
x = \sum^n_{i=1} M_i M^~_i a_i +  \lambda M   \lambda \in \mathbb{Z}

M = m_1 & m2 ... * m_n

M_i * m_i = M

M_i M^~_i = 1 mod m_i

<x>_{m_j}= <\sum^n_{i=1} M_i M^~_ia_i +  \lambda M>_{m_j}>
= <sum^n_{i=1} <M_i M^~_ia_i>_{m_j} +  \lambda>_{m_j}>

<<M_j M^~_j>_{m_j} a_j>_{m_j}


```
##### Příklad čínské věty o zbytcích


header 1 | header 2
---|---
x = 1 mod 3 | M_1 = 20 | 20 M^~_1 = 1 mod 3 | \mathbb{Z}_3 2M^~_1 =1  M^~_1 = 2
x = 2 mod 4 | M_2 = 15 | 15 M^~_2 = 1 mod 4 | \mathbb{Z}_4 -1M^~_2 = 1  M^~_2 = -1
x = 3 mod 5 | M_3 = 12 | 12 M^~_3 = 1 mod 5 | \mathbb{Z}_5 2M^~_3 = 1  M^~_3 = 3

řešení 

```math
 \lambda \in \mathbb{Z}

x = 20 * 2 + 15 * (-1) * 2 + 12 * 3 * 3 + \lambda * 60 

x= 238 + \lambda * 60  = -2 + \lambda * 60  <0 , M)
```
---
```math
f: x \rightarrow (<x>_{m_1},<x>_{m_2},...,<x>_{m_n})

\mathbb{Z}_M \rightarrow^+ \mathbb{Z}_{m_1} \times ... \times \mathbb{Z}_{m_n}

\mathbb{Z}_M \leftarrow \mathbb{Z}_{m_1} \times ... \times \mathbb{Z}_{m_n}

g(y_1,...,y_n) = < \sum^n_{i=1} M_i M^~_i y_i >_M

```

### Eulerova věta
#### Eulerova funkce 
##### Definice

```math
\mathbb{Z}_n,\mathbb{Z}^*_n = \{a \in \mathbb{Z}_n | gcd(a,n) = 1\}

n \ge 2
```
Eulerova funkce
```math
divne L : \mathbb{N}^+ \rightarrow \mathbb{N}^+

n \rightarrow divne L(n) = card(\mathbb{Z}^*_n)

-- ukazka

divne L(6) 
\mathbb{Z}_6 = \{0,1,2,3,4,5\}

\mathbb{Z}^*_6 = \{1,5\}

divne L(6) = 2

```

Jednoduše


```math
\mathbb{Z}_{p^m}  \mathbb{Z}^*_{p^m}    p^m-p^{m-1}


0\le kp < p^m
0 \le k < p^{m-1}

divne L(p^m) = p^m - p^{m-1}

gcd(a,b) = 1

divne L (ab) = divne L (a) * divne L (B)

---- Naznaceno

\mathbb{Z}^*_{ab} \leftrightarrow \mathbb{Z}^*_{a} \times \mathbb{Z}^*_{b} 

x \rightarrow (<x>_a, <x>_b)

x \leftarrow (y_1, y_2)
x = M_a M^~_a y_1 + M_b M^~_b y_2

-- priklad

divne L (60) = divne L (2*3*2*5) = divne L (2^2 *3 *5) = divne L(2^2)* divne L(3)* divne L(5)= (2^2-2)(3^1 - 1)(5^1 -1) = 2*2*4 = 16

---

b_1 * b_2 * ... b_{divne L(n)} = ab_1 * ab_2 ... ab_{divne L(n)}

= a^{divne L(n)} * b1 ... b_{divne L(n)}

```

#### V
Jestliže ```math n \in \mathbb{N}^+, n \ge 2, gcd(a,n) = 1``` potom ```math a^{divne L(n)} = 1 mod n```

```math
v \mathbb{Z}_n

a^m = a^{k divne L(m) + <m>_{divne L(n)}} = (a^{divne L(n)}) * a^{<m>_{divne L(n)}}

gcd (a,n) = 1

= a^{<m>_{divne L(n)}} = 1
```

##### obecnější (používané v RSA)

```math
a^{divne L(n)} = 1  "mezera" k \in \mathbb{N}



a^{k*divne L(n) } = 1  "mezera" a

n je "squarefree"

n = p_1 ... p_n 

n = p * q

--- varianta z rsa

1+k divne L(n) 

a = a 
--  pravidlo z rsa

\forall a \in \mathbb{Z} \forall k \in \mathbb{N}

```

Uvedom me si ze v n je p rozděleno na 2 skupiny nikdy neopakujících se prvočísel
```math
d = gcd(a,n) 

a = \alpha d    gcd(\alpha, \ny) = 1

n = \ny d 		gcd(\ny, d) = 1

-- tudiz

<a^{1+k divne L(n)}>_n = <\apha d * (\alpha d)^{k divne L(\ny d)}>_{\ny d} = d <\alpha>_\ny = <d\alpha>_{d\ny}=<a>_n 

coz se rovna 

= a mod n


vyuziti vlastnosti <ab>_{ac} = a <b>_c
```

### RSA protokol
Nesymetrické šifrování
jedna z aplikací matematiky

zkratka Rivest, Shamir, Adleman - zveřejnili 1978 - šifrování s veřejným klíčem

```math
z \righarrow [šifrování](vstupuje klíč) \rightarrow^c zde nasloucha nekdo \rightarrow [dešifrování](vstupuje dešifrovací klíč) \rightarrow z
```

Bob chce přijímat šifrované zprávy.
A zvolí 2 různá prvočísla - volí je dle velikosti dat
```math
p,q \ in \mathbb{P}, p \ne q, n:= p*q
```
Pak zvolí e 
```math
e \in \mathbb{N}, gcd(e, divne L(n)) = 1 

divne L(n) = (p-1)(q-1)

ed = 1 mod divne L(n)

Public 

K_e = (n,e)

Private
K_d = (n,d)
```

Nyní má bob veřejní klíč a privátní
a nyní chce alice poslat bobovi zprávu "z" a šifruje ji veřejným klíčem K_e

```math
<z^e>_n = c

0 \le z < n

0 \le c < n
```

Bob přijme zprávu a dešifruje ji

```math
<c^d>_n = z
```

bobo získal dešifrovanou zprávu

Vždy platí pravidla 
```math
0 \le z < n

0 \le c < n
```
--- ukázka
```math
c = <z^e>_n

<e^d>_n =  <<z^e>^d_n>_n
<z^{cd}>_n = z
```

K prolomitelnosti je potřeba d a n a rozklad na prvočísla problém je tohle (rovnost je problem (prvni rovnase)) - [(n,e)]
```math
divne L(n) = divne L(pq) = (p - 1) (q - 1)
```


##### Princip RSA v příkladu divne L phi ???
```math
p = 11 

q = 13

n = pq = 143

divne L(n) = 10 * 12 = 120

-- volba e aby bylo nesoumerne s 120

e:= 77

-- inverze k 77

77 * d = 1 mod 120

77d + y* 120 = 1 (reseno v \mathbb{Z})
--- vypocet D
[d,y] *
\begin{bmatrix}
77 & 1 & 0\\ 
120 & 0 & 1 
\end{bmatrix}
= [1,d,y]


\begin{bmatrix}
77 & 1 & 0\\ 
120 & 0 & 1 
\end{bmatrix}
~
\begin{bmatrix}
77 & 1 & 0\\ 
43 & -1 & 1 
\end{bmatrix}
~
\begin{bmatrix}
43 & -1 & 1\\ 
34 & 2 & -1 
\end{bmatrix}
...
~
\begin{bmatrix}
1 & 53 & -34\\ 
0 & -120 & 77 
\end{bmatrix}

[d,y] *
\begin{bmatrix}
1 & 53 & -34\\ 
0 & -120 & 77 
\end{bmatrix}
= [1,d,y]

d'*1 + y' * 0 = 1 
d' = 1 
y'  \in \mathbb{Z}

-- D

d= 53 * d' - 120 y'

--- klice

(143, 77)  = K_e
(143, 53) = K_d

z = 123 

c = 123^77 mod 143

77 bin = 1 0 0 1 1 0 1 alias algoritmicky XSSSXSXSSX

```
X a S jsou funkce
```math
X: y \rightarrow y*123 \mathbb{Z}_{143}

S:  y \rightarrow y^2 


X: 123

S: 114

S: 126

S: 3

X: 83

S: 25

X: 72

S: 36

S: 9

X: 106

c = 106  -- to jest sifrovana zprava 77
```

podobnym postupem  vyjde dešifrovaná zpráva


##### Mýty
e, d nemusí být prvočísla

e, d nemusí být různá (e = d)
pokud e = d při dvojím šifrování se vlastně dešifruje :) 


Popř existují případy (učitel nalzel cca 8 případů - nalezeno hrubou silou) pak 
n = e = d 
příklad
```math
p = 13

q = 29

n = 377

K_e = (377,377)

K_d = (377,377)
```

##### Princip digitálního podpisu

Alice pošle zprávu zašifrovanou bobovým veřejným klíčem a poté ji zašifruje svým klíčem privátním (vlastním)
Poté co předá zprávu bobovi 
bob ji zašifruje veřejným klíčem alice čímž zruší její šifrování protože je komutativní 
Bob má nyní zašifrovanou zprávu svým klíčem tudíž ji svým klíčem dešifruje privátním svým klíčem a dostává zprávu.

----

##### Útoky na RSA 

###### Chyba návrhu
špatný návrh viz výše :)

###### Chyba při návrhu
Pokud navrhujeme svůj klíč a zbydou pomocné výpočeky lze dopočítat klíč znovu. Za pomoci těchto výpočtů a veřejného klíče.
```math
n = pq \rightarrow divne L(n) = (p-1)(q-1)

divne L(n) \rightarrow n = (pq)

----

divne L(n) = (p-1)(q-1) = pq - (p+q) +1

p+q = n+ 1 - divne L(n)

pq = n

(x-p) (x-q) = x^2 - (p+q)x + pq = x^2 - (n+1 - divne L(n)) x + n
```

####### Hrubá síla
poznamka 
```math
eq = 1 mod divne L(n)

<z^e>_p, <e^d>
```
####### priklad
```math
n = pq

1 < p < q

p^2 < pq = n

p < \sqrt{n}

pokud vime

3 \le p < \sqrt{n}

pak

p > 3

<p>_6 = 5 nebo 1

```

tudíž z toho lze usoudit že existují pouze 2 množiny ve kterých je ono prvočíslo
```math
\mathbb{p} \subseteq \{2,3\} \cup (5+6 \mathbb{N}) \cup (7 + 6 \mathbb{Z})
```
A nyní střídavě prvočísla

5 (+2) 7 (+4) 11 (+2) 14 (+4) 17 (+2) 19 (+4) 23

A zkoušet

---- Konec hrubé síly

###### Prozrazené klíče

Pokud existuje v podniku sdílená část klíče n a pouze jiné části e (e_1, e_2 ...) a někdo vám prozradí sdílenou část

```math
z^{ed} = 7


ed = 1 mod divne L(n)

ed = 1 + (k divne L(n))

ed - 1 = k (p-1) (q - 1) = t_0


z^{ed - 1} = 1

7 \in \mathbb{Z}^*_n
```

nyní opakovanými čtverci 
```math
t_k = \frac{1}{2} t_k-1 


z = 2

z^{t_k} = y_k

z^{t_{k-1}} = y^2 _n = y_{n-1} 

y^2_k = 1

(y_n -1 ) (y_n + 1) = 0 v \mathbb{Z}_n = pq


gcd(y_n -1,n) \in \{p,q\}
```

Doma 
zadání zmocnili jste se privátního i soukromého klíče vypočítejte p,q

```math
K_e (245603, 79)
K_d (245603, 71215)

t_0 = 79*71215 - 1
```

## Polynomy
```math
(K, +, 0, ., 1)

f,g \in K[x]

f,g : \mathbb{N} \rightarrow K \& \{n | fn \ne 0 \}  je nekonečná



0 = (0,0,...)

f = (f_0, f_1, ..., f_n, 0, ...) f_n \ne 0 vedoucí koeficient f, deg(f) = n

g = (g_0, g_1, ..., g_m, 0, ...) g_m \ne 0 vedoucí koeficient g, deg(m) = m

x = (0, 1, 0, ...) deg(0) = - \infinity

1 = (1,0, ...)


(K[x], +, 0, *, 1) okruh

(f+g)_n = f_n + g_n

-(f)_n = -f_n

(f*g)_n = \sum^n_{k=0} f_k g_{n-k} = \sum_{(k,l) \in \mathbb{N}^2 | k+l = n} f_l g_e


```

K a K[x] - isomorfní pokud K[x] obsahuje podmnožinu K^'


### Posloupnosti a funkce
```math
(K, +, 0, ., 1)

K[x] \rightarrow K^k

f \rightarrow f


f = f_0+f_1x+...+f_nx^n

f(c) = f_0 + f_ic + ... + f_n c^n \in K

----

f=x+x^2

g=x^2+x^3

f,g \in \mathbb{Z}_3[x]

f=(0,1,1,0...)

g=(0,0,1,1,0...)

degf = 2

degg = 3

```

c | f(c) | g(c)
---|---|---
0 | 0 | 0
1 | 2 | 2
2 | 0 | 0


> dva různé polynomy jsou různé ale jako funkce jsou identické

proto je třeba rozlišovat symbol x jako neurčinou a c jako proměnou prostoru

```math
{f + g}^\^ = f^\^ + g^\^

{f * g}^\^ = f^\^ \dot f^\^

0^\^(c) = 0

1^\^(c) = c
```

### Polynomy 

(K[x], +, 0, *, 1)

#### Definice

```math
f,g \in K[x]
```
1.```math 
f|g \leftrightarrow \exists h \in K[x] (g=f*h)
```

2. h je největší spol dělitel f,g \leftrightarrow
```math 
h|f \& h|g \& (h^'|f \& h^'|g \rightarrow h^'|h)
```
3. h je nejmenší společný násobek \lefrightarrow
```math 
f|h \& g|h \& (f|h^' \& g|h^' \rightarrow h|h^')

h \in lcm(f,g)
```
4.
> asoc je ekvivalence
```math
1 \in gcd(f,g) \leftrightarrow f,g jsou nesoudělné

f|g^' \& g|f \leftrightarrow f asoc g  
```
Tudíž se projeví třídy ekvivalence

```math
[+]_{as} = \{g \in K[x] | g asoc f\}
frac{K[x]}{asoc} = {[f]_{as} | f \in K[x]}
```
---
```math
d \in ged(f,g) \rightarrow gcd(f,g) = [d]_as

l \in lcm(f,g) \rightarrow lcm(f,g) = [e]_as
```


---

```math
K = \mathbb{Z}_6
K[x] = \mathbb{Z}_6[x]
```
> Tento prostor má dělitele 0, protože 2 * 3 = 0 (hrůzný prostor :blush:)

(D, +, 0 , \dot, 1)
#### Tvrzení 
Nechť D je obor integrity
```math f,g \in D[x]```
Pak platí ```math f assoc g \leftrightarrow (\exists \alpha \in D^*) (f=\alpha g) ```
> hvězdičkou se označují všechny invertibilní okruhy D

```math
[f]_as = \{g | g asoc f\} = \{\alpha f | \alpha \in D^*\} = \D^*f
```


```math
\mathbb{Z} \mathbb{Z}^* = \{1, -1\}



f \in \mathbb{Z}[x]

f asoc g \leftrightarrow f = g \takove to V na spojeni dvou vyrazu f = -g
```

#### Věta (o dělení polynomů)
```math
K ... Okruh


\forall f \in K[0] \forall g \in K[x], ved(g)\in K^*

\exists !q \in K[0] \exists r \in K[x] :
f = q \dot g + r \& deg r < deg g

<f>_g = r 
```

> ved(g) stupeň polynomu g

```math
f = f_0 + f_1 x + f_2 x^2

g = g_0 + g_1 x

pokud
g_1 \in K^* 

g_1 \dot g^~_1 = 1

tak pak lze dělit

f_2 x^2 + f_1 x + f_0 : g_1x + g_0 = f_2 g^~_1 x + a g^_1

1.krok - (f_1 - g_0 f_2 g^~_1)x+f_0
(označení (f_1 - g_0 f_2 g^~_1) = a)
2.krok - (f_0 - a g^~_1 g_0)
```
Potvrzení
```math
def f < deg g

f = 0 g + f

deg f \ge deg g
```
> věta o dělení polynomů je stejně důležitá jako věta o dělení celých čísel - (věta o číslech celých číslslech je důležitá pro euklidův algoritmus aby konvergoval)


##### Příklad

```math
a = x^2 + 2

b= 2x+1

\in \mathbb{Z}_5[x]
```

Stanovte nějvětší společný dělitel
```math
gcd(a,b)
```
A také aby byla \alpha a \beta byla rovna d

```math
d \in gcd(a,b)

\alpha a + \beta b = d
```

Využití euklidova algoritmu

\begin{bmatrix}
x^2+2 & 1 & 0\\ 
2x+1 & 0 & 1 
\end{bmatrix}

Příprava
```math
x^2 + 2 : 2x+1 = 3x + 1
1krok (-3x+2)
2krok (2x+2)
zbyde 1

(-3x-1, 2, 1)
```
\begin{bmatrix}
1 & 1 & -3x-1\\ 
2x+1 & 0 & 1 
\end{bmatrix}
~
\begin{bmatrix}
1 & 1 & -3x-1\\ 
0 & -2x-1 & 1+(2x+1)(3x+1) 
\end{bmatrix}
```math
1 \in gcd(x^2+2, 2x+1) = [1]_{as} = \{1,2,3,4\}

1 = 1 \dot (x^2+2)-(3x+1)(2x+1)
```
----
#### Rovnice dyofantického typu

```math
f,g \n \mathbb{Z}_3[x]

(x+1) f + (2x+1) g = x+2

```

[f,g]
\begin{bmatrix}
(x+1) & 1 & 0\\ 
2x+1 & 0 & 1 
\end{bmatrix}
= [x+2, f, g]

Mezi toto vložíme E = 1tková matice ale

```math
\mathbb{E} = \mathbb{T}^{-1} \mathbb{T}
```

~
\begin{bmatrix}
(x+1) & 1 & 0\\ 
2x+1 & 0 & 1 
\end{bmatrix}
poznámka - (-2,1,2) 
~
\begin{bmatrix}
(x+1) & 1 & 0\\ 
-1 & -2 & 1 
\end{bmatrix}
poznámka - (x+1, 2, 1)
~
\begin{bmatrix}
0 & 1 - 2x -2 & x+1\\ 
1 & 2 & -1 
\end{bmatrix}
----
Vrácení do původní matice
```math
f^' 0 + g^' 1 = x+2

f^' \in \mathbb{Z}_3[x]
g^' = x + 2
```
A pomocí transformační matice

[f', g']
\begin{bmatrix}
0 & 2+x & x+1\\ 
1 & 2 & 2 
\end{bmatrix}
=[x+2,f,g]
```math
[f,g] = f^' [2+x, x+1] + (x+2)[2,2]

f = (2+x)f^' + 2x + 1

f^' \in \mathbb{Z}_3[x]

g = (x+1)f^' + 2x + 1
```

------

### vlastnosti

Pokud jsou polynomy nad oborem integrity a je zaručeno že nexistuje 0 prvek

pak 
```math
deg (fg) = deg (f) + deg (g) 
```
> platí v oboru integrity

-----

```math
f \in (D[x])^*

fg = 1

deg (fg) = deg f + deg g = 0
```
> konstantní polynomy neboli invertibilní prvky v D
```math
(D[x])^*  = D^*
```

#### Ireducibilní polynomy
Obor integrity polynomů nad D
```math
D[x]

D^* \cup \{0\} \in D

M = D^* \cup \{0\} \ D 

M \dot M = reducibilní

M \ M \dot M = ireducibilní

```

V ```math \mathbb{Z}```
```math
M = \mathbb{Z} \ {-1,0,1}

čísla složená(reducibilní) M * M 

\mathbb{P} \cup (-\mathbb{P})
```


V tělese F[x]
```math
M = F[x] \ F

f \in M \leftrightarrow  deg f > 0
```
#### Modulová aritmetika v polynomech

```math
F[x]
m \in F[x]

f,g \in F[x]

f~_m g \leftrightarrow m|f-g

~_m ekvivavalence

f ~_m f^' \& g  ~_m g^' \rightarrow f+g ~_m  f^' + g^'

[f]_m = \{g \in F[x] | g ~_m f\} fg ~_m f^' g^'
```
----- 

Z toho lze dokázat že pokud F[x] obsahuje ireducibilní tak F[x] je těleso

F[x] těleso \leftrightarrow m(+) je ireducibilní v F[x]






