# Noções preliminares

> Anotações a partir de Topoi (cap. 11).

## Topos

Um topos é uma categoria.

## Reticulado

Um reticulado é um conjunto $R$ equipado com duas operações binárias, **meet** $(a \sqcap b)$ e **join** $(a \sqcup b)$, com relação as quais valem as seguintes identidades para todos elementos $a,b,c \in R$:

### Comutatividade
1. $a \sqcap b = b \sqcap a$;
2. $a \sqcup b = b \sqcup a$;
   
### Associatividade
3. $a \sqcap (b \sqcap c) = (a \sqcap b) \sqcap c$;
4. $a \sqcup (b \sqcup c) = (a \sqcup b) \sqcup c$;

### Absorção
5. $a \sqcup (a \sqcap b) = a$;
6. $a \sqcap (a \sqcup b) = a$;

### Idempotência
7. $a \sqcup a = a$;
8. $a \sqcap a = a$.

### Ordem

Uma ordem em um reticulado $R$ é uma relação entre elementos $a, b$ de $R$, denotada por $a \sqsubseteq b$ (a é menor ou igual a b). Essa relação respeita os seguintes axiomas.

1. $\forall a : a \sqsubseteq a$ [Reflexividade] 
2. $\forall a, b : a \sqsubseteq b \land b \sqsubseteq a \rightarrow a = b$ [Anti-simetria]
3. $\forall a, b, c : a \sqsubseteq b \land b \sqsubseteq c \rightarrow a \sqsubseteq c$ [Transitividade]

## Álgebra de Heyting

> (cap. 8)

Proposta em $1930$ por Arend Heyting, trata-se de um sistema axiomático da lógica proposicional que gera como teoremas aquelas, e apenas aquelas, "sentenças que são válidas de acordo com a *concepção intuicionista da verdade*" (p. $177$). 

> (p.177-178, sec 8.2)
>> Of course the intuitionist only accepts formal systems as **imperfect tools** for description and communication. He leaves open the possibility that his intuitive deliberations will one day reveal as yet unheard of principles of reasoning. According to Heyting, 'in principle it is impossible to set up a formal system which would be equivalent to intuitionist mathematics ... it can never be proved with mathematical rigour that the system of axioms really embraces every valid method of proof.' 

## Limite superior e limite inferior

Primeiro, precisamos ampliar o sentido da relação $\sqsubseteq$, que foi definida anteriormente apenas para pares de elementos. Nesse contexto, $x \sqsubseteq y$ denota **y é maior que x** (ou **x é menor ou igual a x**). Na extensão que será feita nesta seção, permitiremos que os parâmetros sejam conjuntos. Queremos que $A \sqsubseteq x$ denote **x é limite superior do conjunto A** e $x \sqsubseteq A$ denote **x é limite inferior do conjunto A**. Para isso, quantificaremos sobre o conjunto de elementos.

Seja $A$ um sub-conjunto de um reticulado $R = (L, \sqsubseteq)$ e $x$ um elemento de $R$. Definimos:

1. **Limite superior** $(A \sqsubseteq x)$

$$
\forall y (y \in A \rightarrow y \sqsubseteq x)
$$

2. **Limite inferior** $(x \sqsubseteq A)$

$$
\forall y (y \in A \rightarrow x \sqsubseteq y)
$$

A partir dessa extensão, poderemos definir limite superior mínimo e limite inferior máximo.

> Seja $A$ um subconjunto de um reticulado $R = (L, \sqsubseteq)$, e $x \in L$. Dizemos que $x$ é um **limite superior** de $A$ ($A \sqsubseteq x$), se, para todo $y \in A$, $y \sqsubseteq x$.
>> Ou seja, $x$ é limite superior de $A$ se $x$ for limite superior de todos os elementos de $A$.

Se, além disso, $x \sqsubseteq z$ para todo $A \sqsubseteq z$ (ou seja, todo limite superior de $A$ é um limite superior de $x$), então $x$ é minimal, que chamaremos de **limite superior mínimo** (l.s.min).

> Diremos que $x$ é o **maior elemento** de $A$ se $x \in A$ e $x$ é l.s.min de $A$.

### Exercícios
#### Exercício 1
> *A possui no máximo um limite superior mínimo.* 
> >**Prova:** Supõe que $x$ é um limite superior mínimo de $A$. Então, além de $A \sqsubseteq x$, $x$ é minimal. Agora supõe que existe outro limite superior mínimo de $A \sqsubseteq x'$. Por definição, para todo $A \sqsubseteq z$, temos que $x' \sqsubseteq z$. Como $A \sqsubseteq x$, temos que $x' \sqsubseteq x$. De maneira análoga, como $x$ é minimal, temos que $x \sqsubseteq x'$. Logo, $x = x'$ (por anti-simetria).

#### Exercício 2

> Defina **limite inferior máximo**. 
> >Seja $A$ um sub-conjunto de um reticulado $R_L = (L, \sqsubseteq)$ e $x \in L$. Diremos que $x \sqsubseteq A$ ($x$ é um limite inferior de $A$) se, e somente se, $x \sqsubseteq y$ para todo $y \in A$. Se, além disso, $z \sqsubseteq x$ para todo $z \sqsubseteq A$, então $x$ é um limite inferior máximo.

#### Exercício 3

> *Um limite inferior máximo de A é o maior elemento do conjunto de limites inferiores de A.*
> > **Prova:** Seja $x$ um limite inferior máximo de $A$. Precisamos mostrar que (1) $x$ é um elemento do conjunto de limites inferiores de $A$ (chamaremos de $\Omega$); e (2) $x$ é l.s.min de $\Omega$. Como $x$ é l.i.max de $A$, em particular $x$ é um limite inferior de $A$ e, portanto, temos que $x \in \Omega$. Resta mostar que $x$ é l.s.min de $\Omega$, ou seja: (2.a) $\Omega \sqsubseteq x$;  e (2.b) $\forall z$, se $\Omega \sqsubseteq z$, então $x \sqsubseteq z$. Sabemos que $\Omega \sqsubseteq x$ sse $y \sqsubseteq x$ para todo $y \in \Omega$. Por definição, $x$ é o l.i.max de $A$; logo, para todo limite inferior de $A$ (chamemos de $z$), vale que $z \sqsubseteq x$. Ora, $\Omega$ é justamente o conjunto de limites inferiores de $A$, portanto, para todo $x' \in \Omega$, temos que $x' \sqsubseteq x$ (2.a).

#### Exercício 4

> Defina o **menor elemento** de $A$.
> > Diremos que $x$ é o **menor elemento** de $A$ se: 
> > 1. $x \in A$;
> > 2. $x$ é l.i.min de $A$. 


> Exemplo: considere o reticulado conjunto das partes de $X$ $(P(X), \subseteq)$. Nesse reticulado, o menor elemento é o conjunto vazio $(\emptyset)$; e o maior elemento é $X$. 

### Complemento

O **complemento** (ou **pseudo-complemento**, já que pode ser uma operação não-booleana [a depender do reticulado]) de um elemento $a$ de um reticulado $R = (L, \sqsubseteq)$, denotado por $\bar{a}$, é o maior elemento disjunto de $a$:

$$
\bar{a} = max (x \in L  \mid a \sqcap x = 0)
$$

> Isso implica que, no exemplo do reticulado do conjunto das partes, $A \cap \bar{A} = \emptyset$ [porque disjunto] e, sempre que $A \cap B = \emptyset$, então $B \subseteq \bar{A}$ [porque maximal].

Um reticulado $R$ tal que todo elemento de $R$ possui um pseudo-complemento é um **reticulado pseudo-complementado**.

#### Exercício 5

> $b$ é o maior disjunto de $a$ precisamente quando $b$ satisfaz a condição: 
> 
> >$\forall x \in L$, $x \sqsubseteq b$ $\Leftrightarrow$ $a \sqcap x = 0$.
> 
> > Supõe que $b$ satisfaz a condição. Então temos que mostrar que $b$ é o maior disjunto de $a$. Considere o conjunto $\Omega$ de todos os $x \sqsubseteq b$. É fácil ver que $b$ é o maior elemento desse conjunto. Como, por hipótese, $a \sqcap x = 0$ para todo $x \in \Omega$, então, em particular, $a \sqcap b = 0$. Portanto, $b$ é o maior disjunto de $a$.

#### Exemplos

Em $(P(D), \subseteq)$, $\bar{A}$ é o pseudo-complemento de $A$. Para provar isso, temos que mostrar que

$$
    \forall x \in P(D), x \subseteq \bar{A} \Leftrightarrow A \cap x = \emptyset
$$

Assuma que $x \subseteq \bar{A}$. Nesse caso, todo elemento de $x$ está em $A$ e $x$ não tem nenhum elemento a mais que $\bar{A}$. 


### Definição de uma álgebra de Heyting


> Uma **álgebra de Heyting** (**HA**) é um reticulado $\Omega = (H, \sqsubseteq)$ relativamente pseudo-complementado que possui um zero (**0**).



Uma álgebra de Heyting é completa quando todo subconjunto de $\Omega$ possui l.s.max e l.i.min.

# Conjuntos Heyting-valorados

## Linguagem

### Alfabeto

1. Uma lista infinita $v_1,v_2, \cdots$ de variáveis individuais;
2. Conectivos proposicionais $\land, \lor, \sim, \supset$;
3. Símbolos de quantificação $\forall, \exists$;
4. Símbolo de identidade $\approx$;
5. Parênteses ), (.

> A partir desta linguagem, podemos descrever uma estrutura listando seus **símbolos de relação**, **letras de função** e **constantes individuais**.

Exemplo: 

$$
 \textbf{BA} = \\{ 0,1,f,g,h \\}
$$

onde $f(v)$ significa "o complemento de $v$", $g(v_1,v_2)$ significa "o meet de $v_1$ com $v_2$" e $h(v_1,v_2)$ significa "o join de $v_1$ com $v_2$".

> (cap. 11, sec. 9, pp. 274--..).

Podemos compreender objetos em um topos como entidades "set-like"  **parcialmente existentes** (*partially existent*). Apenas alguns desses elementos são **fortemente existentes** (*actually existent*). O fato de que um elemento $c$ é **fortemente existente** é expresso por $\textbf{E(c)}$

1. $\textbf{E(c)} \equiv \exists v (v\approx \textbf{c})$

Para derivar (1), utiliza-se o seguinte

> **Princípio** "tudo que é igual a algo que existe, existe".

> Observe que $\textbf{E}$ é um predicado e $v$ varia entre os elementos parcialmente existentes (objetos do topos).

**Princípio** "elementos só podem ser iguais se existentes". Em outras palavras, "igualdade implica existência". Formalizando:

2. $v \approx w \supset E(v) \land E(w)$

> Este princípio é mais forte que o princípio utilizado para derivar (1). Chamaremos de **equivalência forte**.

## Dois sentidos para "sameness"


**Bicondicional** $\equiv$. Relação entre fórmulas.

$$
    A \equiv B  \Leftrightarrow (A \supset B) \land (B \supset A)
$$

Onde $A$ e $B$ são fórmulas válidas.


**Equivalência enfraquecida** ≋. Relação entre objetos. Dois elementos $v$ e $w$ são **fracamente equivalentes** quando: **(a)** nenhum deles existe; ou **(b)** quando ambos existem e são iguais.

3. $v ≋ w \equiv (E(v) \lor E(w) \supset v \approx w)$

> Essa noção de equivalência enfraquecida "não diferencia os elementos com respeito a sua inexistência". Se dois elementos não existem eles são fracamente equivalentes.

Em suma, $\approx$ e ≋ são duas relações simétricas: é possível descrever a igualdade em termos da equivalência.

4. $v \approx w \equiv (v ≋ w) \land (E(v) \land E(w))$

Ou seja, dois elementos $v$ e $w$ são idênticos se, e somente se, ambos existem e são fracamente equivalentes.

## [TODO] Exemplo do Bundle

## Concepção generalizada de conjunto

> p. 276-..

Um **conjunto** é uma coleção de elementos parciais, com alguma medida alébrica Heyting-valorada de graus de igualdade (*equality*) entre eles.

Essa noção admite o seguinte "desenvolvimento axiomático abstrato":

> Uma álgebra de Heyting completa (**AHC**) é uma álgebra de Heyting na qual todo sub-conjunto $A \subseteq \Omega$ possui um "limite superior mínimo" (*least upper bound*), denotado por $\sqcup A$, e um "limite inferior máximo" (*greatest lower bound*), denotado por $\sqcap A$.

Seja $(\Omega, \sqsubseteq)$ uma **AHC**.