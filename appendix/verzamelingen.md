# Verzamelingenleer

Als leerling zit je in een klas, als voetballer zit je in een team, je play-list bevat een aantal leuke liedjes, .... Zo kunnen we nog een tijd doorgaan met het geven van voorbeelden. Voorbeelden die allemaal gaan over verzamelingen. In plaats van een klas, team, play list spreken we van een *verzameling*, in het Engels *set*. In een verzameling bevinden zich *elementen* (leerlingen, spelers, liedjes). We noteren een verzameling als volgt:

$$
V=\{v_1,v_2,v_3,\cdots,v_n\}
$$

Verzameling $V$ bevat elementen $v$ die we kunnen nummeren. $v_{1}$ is dan het eerste element in de verzameling, $v_{2}$ het tweede, $v_{3}$ is dan het derde, enz. De complete verzameling noteer je door accolades $\{ .. \}$ om de lijst van elementen te zetten.

Een verzameling bestaat dus uit elementen, en als $v$ *een element is van een verzameling* $V$ noteren we dit als $v \in V$. 

Voorbeeld: De verzameling winkelmandje met de elementen melk, brood, en kaas noteren we als:

$$
\text{winkelmandje} = \{\text{melk}, \text{brood}, \text{kaas}\}
$$

Als we schrijven $\text{melk} \in \text{winkelmandje}$, dan zeggen we dus dat melk in het winkelmandje aanwezig is.


::::{admonition} definitie: deelverzameling
:class: warning

:::{image} figs/deelverzameling.svg
:align: right
:::

Als voor twee verzamelingen $X$ en $Y$ geldt dat elk element van $X$ ook een element is van $Y$, 
dan is $X$ een *deelverzameling* (of *subset*) van $Y$. Notatie: $X ⊂ Y$.
::::

**Voorbeeld:** gegeven $X=\{\text{melk},\text{kaas}\}$ en $Y=\{\text{melk},\text{brood},\text{kaas}\}$,
dan is $X$ is een deelverzameling van $Y$ want melk en kaas, 
de elementen van $X$, zijn ook aanwezig in $Y$: $X ⊂ Y$ .

::::{admonition} definitie: doorsnede
:class: warning

:::{image} figs/doorsnede.svg
:align: right
:::

De *doorsnede* (of *intersection*) $X∩Y$ van twee verzamelingen $X$ en $Y$ bestaat uit de elementen die tot $X$ èn tot $Y$ behoren.  
In de figuur rechts is de doorsnede het lichtgroene gebied.
::::

**Voorbeeld:** de doorsnede van de verzamelingen $X = \{\text{melk}, \text{brood}, \text{kaas}\}$ en $Y = \{\text{melk}, \text{brood}, \text{pindakaas}\}$ is de verzameling $\{\text{melk}, \text{brood}\}$: melk en brood zijn in beide verzamelingen aanwezig. In wiskundige notatie is dit:

$\{\text{melk}, \text{brood}, \text{kaas}\} \cap \{\text{melk}, \text{brood}, \text{pindakaas}\} = \{\text{melk}, \text{brood}\}$
    
::::{admonition} definitie: vereniging
:class: warning

:::{image} figs/vereniging.svg
:align: right
:::

De *vereniging* (of *union*) $X∪Y$ van twee verzamelingen $X$ en $Y$ bestaat uit de elementen die tot $X$, tot $Y$ of tot beide horen.  
In de figuur rechts bestaat de vereniging uit de gele gebieden.
::::

**Voorbeeld:** de vereniging van de verzamelingen  $X = \{\text{melk}, \text{brood}, \text{kaas}\}$  en de verzameling $Y = \{\text{melk}, \text{brood}, \text{pindakaas}\}$ is de verzameling $\{\text{melk}, \text{brood}, \text{kaas}, \text{pindakaas}\}$ want alle elementen uit $X$ en $Y$ zijn aanwezig. Notatie:

$\{\text{melk}, \text{brood}, \text{kaas}\} \cup \{\text{melk}, \text{brood}, \text{pindakaas}\} = \{\text{melk}, \text{brood}, \text{kaas}, \text{pindakaas}\}$

    
::::{admonition} definitie: kardinaliteit

Voor een eindige verzameling $X$ definiëren we $\#X$ als het **aantal** elementen in $X$. Dit wordt ook wel de ***kardinaliteit*** genoemd.
::::

**Voorbeeld:** $\#\{\text{chips}, \text{zeep}, \text{appels}\}=3$.

Een element van een verzameling kan zelf ook een verzameling zijn. Zo bestaat de verzameling 

$$
\begin{array}{rcl}C &=& \{\{\text{chips}, \text{zeep}, \text{appels}\}\\&&, \{\text{chips}, \text{zeep}, \text{appels}\}\\&&, \{\text{zeep}, \text{bananen}\}\\&&, \{\text{chips}, \text{zeep}, \text{bananen}\}\\&&\}\end{array}
$$

uit vier elementen, ieder element is een verzameling. 

Een verzameling waarin de elementen ook weer verzamelingen zijn noemt men ook wel een *collectie*.
