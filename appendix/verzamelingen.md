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


🚨 **Deelverzameling**

:::{image} figs/deelverzameling.svg
:align: right
:::

Als voor twee verzamelingen $X$ en $Y$ geldt dat elk element van $X$ ook een element is van $Y$, 
dan zeggen we dat $X$ een *deelverzameling* (of *subset*) is van $Y$. Notatie: $ X⊂Y$.

Zo geldt bijvoorbeeld voor $X=\{\text{melk},\text{kaas}\}$ en $Y=\{\text{melk},\text{brood},\text{kaas}\}$ 
dat $X ⊂ Y$, $X$ is een deelverzameling van $Y$ want melk en kaas, 
de elementen van $X$, zijn ook aanwezig in $Y$.

🚨 **Doorsnede**

:::{image} figs/doorsnede.svg
:align: right
:::

De *doorsnede* (of *intersection*) $X∩Y$ van twee verzamelingen $X$ en $Y$ bestaat uit de gemeenschappelijke elementen van $X$ en $Y$. In de figuur rechts is de doorsnede het lichtgroene gebied.

Zo is bijvoorbeeld de doorsnede van de verzamelingen $X = \{\text{melk}, \text{brood}, \text{kaas}\}$ en $Y = \{\text{melk}, \text{brood}, \text{pindakaas}\}$ de verzameling met melk en brood, $\{\text{melk}, \text{brood}\}$, want die zijn in beide verzameling aanwezig. In wiskundige notatie is dit:

$\{\text{melk}, \text{brood}, \text{kaas}\} \cap \{\text{melk}, \text{brood}, \text{pindakaas}\} = \{\text{melk}, \text{brood}\}$
    
🚨 **Vereniging**

:::{image} figs/vereniging.svg
:align: right
:::

De *vereniging* (of *union*) $X∪Y$ van twee verzamelingen $X$ en $Y$ bestaat uit de elementen die tot $X$, tot $Y$ of tot beide horen. In de figuur rechts bestaat de vereniging uit alle enigszins gele gebieden.

Zo is bijvoorbeeld de vereniging van de verzamelingen  $X = \{\text{melk}, \text{brood}, \text{kaas}\}$  en de verzameling $Y = \{\text{melk}, \text{brood}, \text{pindakaas}\}$ verzameling met de elementen Kaas, Melk, Brood en Pindakaas, $\{\text{melk}, \text{brood}, \text{kaas}, \text{pindakaas}\}$ want alle elementen uit $X$ en $Y$ zijn aanwezig. Notatie:

$\{\text{melk}, \text{brood}, \text{kaas}\} \cup \{\text{melk}, \text{brood}, \text{pindakaas}\} = \{\text{melk}, \text{brood}, \text{kaas}, \text{pindakaas}\}$

    
🚨 **Kardinaliteit**

Voor een eindige verzameling $X$ definiëren we $\#X$ als het **aantal** elementen in $X$. Dit wordt ook wel de ***kardinaliteit*** genoemd.

Zo is bijvoorbeeld $\#\{\text{chips}, \text{zeep}, \text{appels}\}=3$.

Een element van een verzameling kan zelf ook een verzameling zijn. Zo bestaat de verzameling 

$$
\begin{array}{rcl}C &=& \{\{\text{chips}, \text{zeep}, \text{appels}\}\\&&, \{\text{chips}, \text{zeep}, \text{appels}\}\\&&, \{\text{zeep}, \text{bananen}\}\\&&, \{\text{chips}, \text{zeep}, \text{bananen}\}\\&&\}\end{array}
$$

uit vier elementen, ieder element is een verzameling. 

Een verzameling waarin de elementen ook weer verzamelingen zijn noemt men ook wel een *collectie*.
