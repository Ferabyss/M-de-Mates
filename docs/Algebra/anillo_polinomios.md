# Anillo de Polinomios

## Series de Potencias

::: mydef
Sea $A$ un anillo. Denotemos por
$$S_A=\left\{f\Big|\ensuremath{f:\mathbb{N}\cup\left\{0\right\}\rightarrow A} \right\}$$
es decir que $S_A$ es el **conjunto de sucesiones de $A$**. Si
$f\in S_A$ escribimos a $f$ como: $$f=(a_0,a_1,...)$$ Sobre $S_A$ se
definen dos operaciones, la **suma** y **producto**. A saber, si
$f=(a_0,a_1,...)$ y $g=(b_0,b_1,...)$, entonces:
$$f+g=(a_0+b_0,a_1+b_1,...,a_k+b_k,...)$$ y,
$$fg = f\cdot g = (c_0,c_1,...,c_k,...)$$ donde $$\begin{split}
                c_k&=\sum_{ i=0}^k a_ib_{ k-i}\\
                &=a_0b_k+a_1b_{ k-1}+...+a_kb_0\\
                &=\sum_{ i=0}^k a_{k-i}b_{i}\\
                &=\sum_{ i+j=k}a_ib_j\\
            \end{split}$$
:::

::: obs
En la definición anterior, se tiene que $S_A$ es un anillo con cero el
elemento $(0,0,...,0,...)$ e inverso $-f=(-a_0,-a_1,...,-a_k,...)$ para
todo $f\in S_A$. Además, existe un monomorfismo de $A$ en $S_A$, a
saber: $$A\hookrightarrow S_A, a\mapsto (a,0,...,0,...)$$ Por lo cual
$A$ está encajado en $S_A$. Debido a esto, se denotará de ahora en
adelante como $$a=(a,0,...,0,...),\quad\forall a\in A$$
:::

::: mydef
Sean $A$ y $X$ un objeto tal que $X\notin A$. $X$ es llamado una
**indeterminada para $A$**. Definimos para todo
$n\in\mathbb{N}\cup\left\{0\right\}$ y para todo $a\in A$:
$$aX^n=(\underbrace{0,0,0,...,0,0,0,a}_{{n+1}-\textbf{ésima entrada}},0,...)$$
Si $A$ tiene identidad, entonces
$$1X^n=X^n=(\underbrace{0,0,0,...,0,0,0,1}_{{n+1}-\textbf{ésima entrada}},0,...)$$
En caso que $n=1$, $1X^1=X^1=x$ y si $n=0$, $1X^0=X^0=1$ (abusando en
este caso de la notación). Se tiene entonces que
$$X^n\in S_A,\quad\forall n\in\mathbb{N}\cup\left\{0\right\}$$ Ahora,
independientemente de si $A$ tiene o no identidad, tenemos que:
$$\begin{split}
                (a_0,a_1,a_2,...,a_k,...)&=(a_0,0,0,...)\\
                &+(0,a_1,0,...)\\
                &+(0,0,a_2,...)\\
                &+(0,0,...,a_k,...)\\
                &+...\\
                &=a_0X^0+a_1X+a_2X^2+-...\\
            \end{split}$$ Por lo tanto, si
$f=(a_0,a_1,a_2,...,a_k,...)$, entonces: $$\begin{split}
                f&=\sum_{i=0}^\infty a_iX^i\\
                &=a_0+a_1X+a_2X^2+...+a_kX^k+...\\
            \end{split}$$ así pues, podemos decir que una serie es una
expresión algebraica de la forma:
$$f=\sum_{i=0}^\infty a_iX^i=a_0+a_1X+a_2X^2+...+a_kX^k+...$$ donde
$a_0:=a_0X^0$.

Si $f=\sum_{ n=0}^\infty a_nX^n$ y $g=\sum_{ n=0}^\infty b_nX^n$,
entonces: $$\begin{split}
                f+g&=\sum_{n=0}^\infty(a_n+b_n)X^n\\
                f\cdot g&=\sum_{ n=0}^\infty c_nX^n\\
            \end{split}$$ siendo $c_n=\sum_{ k=0}^n a_kb_{ n-k}$ para
todo $n\in\mathbb{Z}_{\geq0}$. Con estas operaciones $S_A$ es un anillo,
cambiándose el símbolo por $A[[X]]$, en este caso $A[[X]]$ es llamado
**anillo de series de potencias con coeficientes en $A$ en la
indeterminada $X$**.

Si $f=\sum_{ n=0}^\infty a_nX^n\in A[[X]]$, los elementos
$a_0,a_1,...\in A$ son llamados **coeficientes o términos de la serie
$f$**. En particular, $a_0$ es llamado **coeficiente constante** o
**coeficiente lider de la serie $f$**. El cero de $A[[X]]$ es la serie
**serie cero** dada por:
$$0=\sum_{ n=0}^\infty a_nX^n,\quad a_n=0\quad\forall n\in\mathbb{Z}_{ \geq0}$$
:::

::: obs
Una serie de potencias $f\in A[[X]]$ cumple que $f=0$ si y sólo si
$a_n=0$ para todo $a_n=0,\forall n\in\mathbb{Z}_{\geq0}$.

En el caso de que $f$ tenga coeficientes cero, éstos no se expresan
dentro de $f$, es decir que no se expresan dentro de la sumatoria de
tipo $f=a_0+a_1X+...$.
:::

::: obs
En el caso de que el anillo $A$ tenga identidad, $A[[X]]$ también lo
tiene y es la identidad de $A$, a saber: $$1=1+0X+0X^2+...$$ En tal
caso, $1X^n=X^n$ para todo $n\in\mathbb{N}$.
:::

::: obs
Si $n,m\in\mathbb{Z}_{\geq0}$, entonces $X^n,X^m\in A[[X]]$ y,
$$X^n\cdot X^m=X^{ n+m}\in A[[X]]$$
:::

::: obs
Si $A$ es un anillo conmutativo, entonces $A[[X]]$ también lo es (se
verifica de forma inmediata de la definición de producto en $A[[X]]$).
:::

::: mydef
Sea $A$ un anillo. Para cada serie $f=\sum_{ n=0}^\infty a_nX^n\neq0$ en
$A[[X]]$ se define el **orden de $f$**, denotado por
$\ensuremath{\textup{ord}\left(f\right)}$ como el mínimo entero no
negativo $m$ tal que $a_{m}\neq0$. Así, si $f$ es una serie de potencias
no cero, entonces:
$$f=\sum_{ n=\ensuremath{\textup{ord}\left(f\right)}}^\infty a_nX^n$$
:::

::: excer
Sea $A$ un anillo con $1$. Si $f=\sum_{ n=0}^\infty a_nX^n\in A[[X]]$,
entonces existe $g=\sum_{ n=0}^\infty b_nX^n$ tal que
$\ensuremath{\textup{ord}\left(g\right)}=0$ y,
$$f=X^{\ensuremath{\textup{ord}\left(f\right)}}g$$
:::

##### Demostración: 

Se tienen dos casos:

-   $\ensuremath{\textup{ord}\left(f\right)}=0$, en cuyo caso basta
    tomar $g=f$, con lo que se obtiene que $$f=X^0f=f$$

-   Suponga que $\ensuremath{\textup{ord}\left(f\right)}>0$. Para cada
    $m\in\mathbb{N}\cup\left\{0\right\}$ se define
    $$b_m=a_{ m+\ensuremath{\textup{ord}\left(f\right)}}$$ (siendo
    $f=a_0+a_1X+a_2X^2+...=\sum_{ n=0}^\infty a_nX^n$). Tomemos así
    $$g=\sum_{ n=0}^\infty b_nX^n=\sum_{ n=0}^\infty a_{n+\ensuremath{\textup{ord}\left(f\right)}}X^n$$
    como $a_{\ensuremath{\textup{ord}\left(f\right)}}\neq0$, entonces
    $\ensuremath{\textup{ord}\left(g\right)}=0$ ya que
    $b_0=a_{\ensuremath{\textup{ord}\left(f\right)}}\neq0$. Además, se
    cumple que $$\begin{split}
                        f&=\sum_{ n=0}^\infty a_nX^n\\
                        &=\sum_{ n=\ensuremath{\textup{ord}\left(f\right)}}^\infty a_nX^n\\
                        &=\sum_{ n=0}^\infty a_{n+\ensuremath{\textup{ord}\left(f\right)}}X^{n+\ensuremath{\textup{ord}\left(f\right)}}\\
                        &=X^{\ensuremath{\textup{ord}\left(f\right)}}\sum_{ n=0}^\infty a_{n+\ensuremath{\textup{ord}\left(f\right)}}X^{n}\\
                        &=X^{\ensuremath{\textup{ord}\left(f\right)}}\sum_{ n=0}^\infty b_{n}X^{n}\\
                        &=X^{\ensuremath{\textup{ord}\left(f\right)}}g\\
                    \end{split}$$

$\blacksquare$

::: propo
Sea $A$ anillo y $f=\sum_{ n=0}^\infty a_nX^n$ y
$\sum_{ n=0}^\infty b_nX^n$ dos series de potencias no cero en $A[[X]]$.
Entonces:

1.  $f+g=0$ ó
    $\ensuremath{\textup{ord}\left(f+g\right)}\geq\min\left\{\ensuremath{\textup{ord}\left(f\right)},\ensuremath{\textup{ord}\left(g\right)}\right\}$.

2.  $fg=0$ ó
    $\ensuremath{\textup{ord}\left(fg\right)}\geq\ensuremath{\textup{ord}\left(f\right)}+\ensuremath{\textup{ord}\left(g\right)}$.
:::

##### Demostración: 

De (1): Suponga que $f+g\neq0$, tomemos $h=f+g$ y tomemos
$m=\ensuremath{\textup{ord}\left(h\right)}$. Se tienen tres casos:

-   $\ensuremath{\textup{ord}\left(f\right)}>\ensuremath{\textup{ord}\left(g\right)}$,
    en tal caso se tiene que
    $\ensuremath{\textup{ord}\left(h\right)}=\ensuremath{\textup{ord}\left(g\right)}=\min\left\{\ensuremath{\textup{ord}\left(f\right)},\ensuremath{\textup{ord}\left(g\right)}\right\}$.

-   $\ensuremath{\textup{ord}\left(f\right)}<\ensuremath{\textup{ord}\left(g\right)}$,
    el caso es análogo al anterior.

-   $k=\ensuremath{\textup{ord}\left(f\right)}=\ensuremath{\textup{ord}\left(g\right)}$,
    se tienen dos casos:

    -   $a_{k}+b_k=0$, se sigue pues que como $h\neq0$, entonces
        $\ensuremath{\textup{ord}\left(h\right)}>\ensuremath{\textup{ord}\left(f\right)},\ensuremath{\textup{ord}\left(g\right)}=k=\min\left\{\ensuremath{\textup{ord}\left(f\right)},\ensuremath{\textup{ord}\left(g\right)}\right\}$.

    -   $a_{k}+b_k\neq0$, de donde se sigue de forma inmediata que
        $\ensuremath{\textup{ord}\left(h\right)}=k=\min\left\{\ensuremath{\textup{ord}\left(f\right)},\ensuremath{\textup{ord}\left(g\right)}\right\}$.

por los incisos anteriores se sigue que
$\ensuremath{\textup{ord}\left(f+h\right)}\geq\min\left\{\ensuremath{\textup{ord}\left(f\right)},\ensuremath{\textup{ord}\left(g\right)}\right\}$.

De (2): Es similar a (1). $\blacksquare$

::: cor
En las condiciones de la proposición anterior, si $A$ es dominio entero,
entonces
$\ensuremath{\textup{ord}\left(fg\right)}=\ensuremath{\textup{ord}\left(f\right)}+\ensuremath{\textup{ord}\left(g\right)}$.
En particular, $fg\neq0$ y $A[[X]]$ es dominio entero.
:::

##### Demostración: 

Suponga que $A$ es dominio entero. Sean $f,g\in A[[X]]$ como en la
proposición anterior tales que $f,g\neq0$. De una proposición anterior
se sabe que existen $f_1,g_1\in A[[X]]$ tales que
$$f=X^{\ensuremath{\textup{ord}\left(f\right)}}f_1\quad\textup{y}\quad g=X^{\ensuremath{\textup{ord}\left(g\right)}}g_1$$
con
$\ensuremath{\textup{ord}\left(f_1\right)}=\ensuremath{\textup{ord}\left(g_1\right)}=0$.
En particular se tiene que
$a_{\ensuremath{\textup{ord}\left(f\right)}}\neq0$ y
$b_{\ensuremath{\textup{ord}\left(g\right)}}\neq0$, luego
$$\begin{split}
                fg&=(a_{\ensuremath{\textup{ord}\left(f\right)}}X^{\ensuremath{\textup{ord}\left(f\right)}}+...)\cdot(b_{\ensuremath{\textup{ord}\left(g\right)}}X^{\ensuremath{\textup{ord}\left(g\right)}})\\
                &=a_{\ensuremath{\textup{ord}\left(f\right)}}b_{\ensuremath{\textup{ord}\left(g\right)}}X^{\ensuremath{\textup{ord}\left(f\right)}+\ensuremath{\textup{ord}\left(g\right)}}+...\\
            \end{split}$$ donde, al ser $A$ dominio entero, sucede que
$a_{\ensuremath{\textup{ord}\left(f\right)}}b_{\ensuremath{\textup{ord}\left(g\right)}}\neq0$,
luego $fg\neq0$, en particular se tiene que
$\ensuremath{\textup{ord}\left(fg\right)}=\ensuremath{\textup{ord}\left(f\right)}+\ensuremath{\textup{ord}\left(g\right)}$.
Por ende, $A[[X]]$ es dominio entero. $\blacksquare$

::: propo
Sean $A$ anillo conmutativo con $1$ y
$f=\sum_{ n=0}^\infty a_nX^n\in A[[X]]$ una serie de potencias no cero.
Entonces $f$ es unidad de $A[[X]]$ (esto es, elemento invertible de
$A[[X]]$) si y sólo si $a_0$ (el término constante de $f$) es unidad de
$A$.
:::

##### Demostración: 

$\Rightarrow$): Suponga que $f$ es unidad de $A[[X]]$, entonces existe
$g\in A[[X]]$ tal que $$fg=1$$ en particular, se tiene que si
$f=\sum_{ n=0}^{\infty}a_nX^n$ y $g=\sum_{ n=0}^{\infty}b_nX^n$,
entonces $a_0b_0=1$, por tanto $a_0\in A^*$.

$\Leftarrow$): Suponga que $a_0\in A^*$, entonces existe $b_0\in A^*$
tal que $$a_0b_0=1$$ $\blacksquare$

::: cor
Si $K$ es campo, entonces $f=\sum_{ n=0}^\infty a_nX^n$ en
$K[[X]]\backslash\left\{0\right\}$ es unidad si y sólo si $a_0\neq0$.
:::

##### Demostración: 

Es inmediata de la proposición anterior y del hecho que las unidades de
$K$ son $K\backslash\left\{0\right\}$. $\blacksquare$

::: cor
Si $K$ es campo y
$f=\sum_{ n=0}^\infty a_nX^n\in K[[X]]\backslash\left\{0\right\}$,
entonce existe una única serie de potencias $g\in K[[X]]$ invertible tal
que $f=x^{\ensuremath{\textup{ord}\left(f\right)}}g$.
:::

::: exa
Considere en $\mathbb{R}[[X]]$ la serie de potencias
$f=1+X+X^2+...=\sum_{ n=0}^\infty X^n$. Se tiene que $f$ es invertible y
su inversa es $1-x\in\mathbb{R}[[X]]$.
:::

##### Demostración: 

Ejercicio. $\blacksquare$
