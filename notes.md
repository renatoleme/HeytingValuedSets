# Noções preliminares

> Anotações a partir de Topoi (cap. 11).

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
 \textbf{BA} = \left\{ 0,1,f,g,h \right\}
$$

onde $f(v)$ significa "o complemento de $v$", $g(v_1,v_2)$ significa "o meet de $v_1$ com $v_2$" e $h(v_1,v_2)$ significa "o join de $v_1$ com $v_2$".

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

Uma ordem em um reticulado é uma relação binária $\sqsubseteq$ que respeita os seguintes axiomas

1. $\forall a : a \sqsubseteq a$ [Reflexividade] 
2. $\forall a, b : a \sqsubseteq b \land b \sqsubseteq a \rightarrow a = b$ [Anti-simetria]
3. $\forall a, b, c : a \sqsubseteq b \land b \sqsubseteq c \rightarrow a \sqsubseteq c$ [Transitividade]

## Álgebra de Heyting

> (cap. 8)

Proposta em $1930$ por Arend Heyting, trata-se de um sistema axiomático da lógica proposicional que gera como teoremas aquelas, e apenas aquelas, "sentenças que são válidas de acordo com a *concepção intuicionista da verdade*" (p. $177$). 

> "Of course the intuitionist only accepts formal systems as **imperfect tools** for description and communication. He leaves open the possibility that his intuitive deliberations will one day reveal as yet unheard of principles of reasoning. According to Heyting, 'in principle it is impossible to set up a formal system which would be equivalent to intuitionist mathematics ... it can never be proved with mathematical rigour that the system of axioms really embraces every valid method of proof.'" (p.$177$-$178$, sec $8.2$)

## Limite superior e limite inferior

Seja $A$ um subconjunto de um reticulado $R_L = (L, \sqsubseteq)$, e $x \in L$. Dizemos que $x$ é um **limite superior** de $A$ ($A \sqsubseteq x$), se, para todo $y \in A$, $y \sqsubseteq x$.

> Ou seja, $x$ é limite superior de $A$ se $x$ for limite superior de todo $y \in A$.

Se, além disso, $x \sqsubseteq z$ para todo $A \sqsubseteq z$, então $x$ é minimal, que chamaremos de **limite superior mínimo** (l.s.min).

> *$A$ possui no máximo um limite superior mínimo.* **Prova:** Supõe que $x$ um é limite superior mínimo de $A$. Então, além de $A \sqsubseteq x$, $x$ é minimal. Agora supõe que existe outro limite superior mínimo de $A \sqsubseteq x'$. Por definição, para todo $A \sqsubseteq z$, temos que $x' \sqsubseteq z$. Como $A \sqsubseteq x$, temos que $x' \sqsubseteq x$. De maneira análoga, como $x$ é minimal, temos que $x \sqsubseteq x'$. Logo, $x = x'$ (por anti-simetria).

> Limite inferior máximo. 


> Uma álgebra de Heyting é completa quando todo subconjunto de $\Omega$ possui l.s.max e l.i.min.

# Conjuntos Heyting-valorados

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