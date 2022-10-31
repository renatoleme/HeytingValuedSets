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

> Exemplo: 
>
> $$
> \textbf{BA} = \{ 0,1,f,g,h \}
> $$
>
> onde $f(v)$ significa "o complemento de $v$", $g(v_1,v_2)$ significa "o meet de $v_1$ com $v_2$" e $h(v_1,v_2)$ significa "o join de $v_1$ com $v_2$".


$E(t)$ é um predicado de existência. "t existe".


# Conjuntos Heyting-valorados

> (cap. 11, sec. 9, pp. 274--..).

Podemos compreender objetos em um topos como entidades "set-like"  **parcialmente existentes** (*partially existent*). Apenas alguns desses elementos são **existentes de fato** (*actually existent*). O fato de que um elemento $c$ existe é expresso como $\textbf{E(c)}$

$$
\textbf{E(c)} \equiv \exists v (v \approx \textbf{c})
$$

> Observe que $\textbf{E}$ é um predicado e $v$ varia entre os elementos parcialmente existentes (objetos do topos).

## Dois sentidos para "sameness"



1.
    Bicondicional $\equiv$. Relação entre fórmulas.

    $$
    A \equiv B  \Leftrightarrow (A \supset B) \land (B \supset A)
$$

    Onde A e B são fórmulas válidas.

1. Equivalência enfraquecida ≋. Relação entre objetos. Dois elementos são equivalentes quando: (a) nenhum deles existem; ou (b) quando ambos existem e são iguais.

    $$
    v ≋ w \equiv (E(v) \lor E(w) \supset v \approx w)
$$
