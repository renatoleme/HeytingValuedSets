# Noções preliminares

> Anotações a partir de Topoi (cap. 11) 

## Topos

Um topos é uma categoria.

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
 \textbf{BA} = \{0,1,f,g,h\}
$$

onde $f(v)$ significa "o complemento de $v$", $g(v_1,v_2)$ significa "o meet de $v_1$ com $v_2$" e $h(v_1,v_2)$ significa "o join de $v_1$ com $v_2$".


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

> Uma álgebra de Heyting completa (**CHA**) é uma álgebra de Heyting na qual todo sub-conjunto $A \subseteq \Omega$ possui um "limite superior mínimo" (*least upper bound*), denotado por $\sqcup A$, e um "limite inferior máximo" (*greatest lower bound*), denotado por $\sqcap A$.

Seja $(\Omega, \sqsubseteq)$ uma **CHA**.