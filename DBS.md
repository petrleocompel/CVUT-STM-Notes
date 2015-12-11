# Databáze
## Informace
## Logický model
- Zachycuje data, omezení 

## Relační model
- Všechna data v tabulkách
    - atributy jsou jedoduché datové typy
- joiny
-
### Zápis

```math
S(A_1:T_1,A_2:T_2, ...)
```


### 
## Semestrální práce
```math
group(\bold{id}, name)

user(\bold{id}, firstname, lastname, email, \bold{group\_id})

group\_id \subseteq group.id

book(\bold{id}, name, isbn)

author(\bold{id}, firstname, lastname, bio, birth\_date)

category(\bold{id}, name, \bold{parent\_id})

\bold{parent\_id} \subseteq category.\bold{parent\_id}

rent(\bold{id}, date\_from, date\_to, note, \bold{book\_id}, \bold{user\_id})

\bold{book\_id} \subseteq book.\bold{id}

\bold{user\_id} \subseteq user.\bold{id}

book\_has\_author(\bold{book\_id}, \bold{author\_id})

\bold{book\_id} \subseteq book.\bold{id}

\bold{author\_id} \subseteq author.\bold{id}

book\_has\_category(\bold{book\_id}, \bold{category\_id})

\bold{book\_id} \subseteq book.\bold{id}

\bold{category\_id} \subseteq category.\bold{id}
```
