---
{"dg-publish":true,"permalink":"/chapter-5-homework-analysis/","dgHomeLink":true,"dgPassFrontmatter":false,"dgShowBacklinks":false,"dgShowLocalGraph":false,"dgShowInlineTitle":false}
---

Sam Tang
Mathematical Analysis
October 19, 2022

# Chapter 5 Homework - Analysis

> [!info] Exercise 5.17 
> Use the scaffolding provided below to complete the proof of the [[Chapter 5 Homework - Analysis#Lemma 5 12 Monotone Subsequence Lemma|#Lemma 5 12 Monotone Subsequence Lemma]].
> > Every sequence in $\mathbb{R}$ has a monotone subsequence.

Let $\{ a_{n} \}_{n=1}^{\infty }$ be a sequence in $\mathbb{R}$. We will call a term $a_{M}$ a **dominant term** if and only if $a_{M}>a_{n}$ for all $n>M$.

There must either be a finite amount of dominant terms for $\{a_{n}\}_{n=1}^{\infty}$ or an or an infinite amount.

If there is an infinite number of dominant terms, then let $a_{n_{1}}$ equal the first dominant term, $a_{n_{2}}$ equal the second dominant term, and so on. By The definition of a dominant term, for any $p,q \in \mathbb{N}$, if $p<q$, then $a_{n_{p}}>a_{n_{q}}$, making $\{ a_{n_{k}} \}$ **decreasing**.

If there are a finite amount of dominant terms there must exists a greatest dominant term (greatest not in value, but in its placement in the sequence), $a_{N}$. Thus for all $n>N$, $a_{n}$ cannot be a dominant term. By negating the definition of a dominant term, we get the following fact:
 
> For every $n>N$  there must exists an $m>n \in \mathbb{N}$ such that $a_{m}\geq a_{n}$.

Thus
$$
\begin{align}
&\exists m_{1}>N\\
&\exists m_{2}>m_{1}:a_{m_{2}}\geq a_{m_{1}}\\
&\exists m_{3}>m_{1}:a_{m_{3}}\geq a_{m_{2}}\\
&\vdots\\
&\exists m_{p}>m_{p-1}:a_{m_{p}}\geq a_{m_{p-1}}\\
\end{align}
$$
If we consider the subsequence $\{a_{m_{k}}\}$, by construction the sequence will be **increasing**.

In both the case where there are a finite number of dominant terms, and in the case where there is an infinite number, we can produce a monotone subsequence, proving the theorem.
<br>
<br>
<br>
<br>

> [!info] Theorem 5.18 
> If $B$ is a bounded infinite subset of $\mathbb{R}$, then $B$ must have at least one accumulation point (i.e., $B'\neq \emptyset$).

Let $B$ be an infinite subset of $\mathbb{R}$ and let $S$ be a countably infinite subset of $B$. By definition of a countable set there is a bijection $f:\mathbb{N}\to S$. A sequence is just a function from the natural numbers to the reals, so $f$ gives us a sequence $\{ a_{n} \}$ which is in $S$. Because $\{ a_{n} \}$ is in $S$ and $S$ is bounded, $\{ a_{n} \}$ must also be bounded. And by [[Mathematical Analysis#Theorem 5.13 (Bolzano-Weierstrass Theorem for Sequences)|The Bolazno-Weierstrass Theorem for Sequences]] there must be a convergent subsequence $\{ a_{m_{k}} \}$ in $S$ which converges to some number $L$.

Because the the function $f$ which $\{ a_{n} \}$ was constructed from was a bijection, *every sequence term will be unique* and every element in $S$ will appear in the series. That means that if some term $a_{m_{i}}=L$, it will be the only term to do so. Now consider the modified sequence $\{ b_{n} \}$ such that
$$
b_{n}=
\begin{cases}
a_{m_{n}}&\text{If $a_{m_{n}}\neq L$}\\
a_{m_{n-1}}&\text{If $a_{m_{n}}= L$}
\end{cases}
$$
Clearly $\lim\limits_{ n \to \infty }a_{n}=\lim\limits_{ n \to \infty }b_{n}=L$, because we have only changed at most one term. But in making this slight modification we have ensured that $L$ does not appear in $b_{n}$. This means that $\{ b_{n} \}$ is in $S\setminus \{ L \}$. By [[Mathematical Analysis#Lemma 4.28|Lemma 4.28]] $L \in (S\setminus \{ L \})\cup(S\setminus \{ L \})'$. By definition it is not in $S\setminus \{ L \}$, so it must be an accumulation point of $S\setminus \{ L \}$.

$S\setminus \{ L \}\subseteq B$, so by [[Chapter 5 Homework - Analysis#Exercise 2 25|#Exercise 2 25]] $(S\setminus \{ L \})' \subseteq B'$. Thus because $L \in(S\setminus \{ L \})'\subseteq B'$, $B'\neq \emptyset$.

<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>

> [!info] Theorem 5.19 
> Suppose $(a_{n})_{n=1}^{\infty}$ is a sequence in $\mathbb{R}$. A number $L$ is a sub-sequential limit of $(a_{n})_{n=1}^{\infty}$ if and only if every $\varepsilon$-neighborhood of $L$ contains infinitely many terms of $(a_{n})_{n=1}^{\infty}$.

First, we will show the forward direction of the biconditional.
Suppose that $\{ a_{n} \}$ is a sequence in $\mathbb{R}$ such that $L$ is a sub-sequential limit. We must show that every $\varepsilon$-neighborhood of $L$ contains infinitely many points. Let $\varepsilon>0$ be given.

By the definition of a subsequential limit there exists a subsequence $\{ a_{m_{k}} \}$ such that there exists an $N\in \mathbb{N}|\forall k>N, \left| a_{m_{k}}-L \right|<\varepsilon$. There are only a finite number of sequences elements in $a_{m_{k}}$ before $a_{N}$, so there must be an infinite number after it, and, as shown above, they must all be within epsilon of $L$—giving the desired result.

Now we will show the backward direction of the biconditional.
Suppose that $\{ a_{n} \}$ is a sequence in $\mathbb{R}$ such that every $\varepsilon$-neighborhood of $L$ contains an infinite number of terms of $\{ a_{n} \}$. We must show that $L$ is a subsequential limit of $\{ a_{n} \}$.

For any sequence term $a_{k}$ and any $\varepsilon>0$ there must be an infinite amount of terms within the $\varepsilon$-neighborhood of $L$ *after* $a_{k}$, because there are only a finite number of terms before it, and there are an infinite number of terms in the $\varepsilon$-neighborhood of $L$. Thus there must definitely always be one term greater than it within the neighborhood. We will use that fact to construct the following sequence $\{ m_{k} \}$, made up of only natural numbers.
$$
\begin{align}
&\exists m_{1}:a_{m_{1}}\in N_{1}(L)\\
&\exists m_{2}>m_{1}:a_{m_{2}}\in N_{\frac{1}{2}}(L)\\
&\exists m_{3}>m_{2}:a_{m_{3}}\in N_{\frac{1}{3}}(L)\\
\vdots\\
&\exists m_{p}>m_{p-1}:a_{m_{p}}\in N_{\frac{1}{p}}(L)\\
\end{align}
$$
Notice by the construction of $\{ m_{k} \}$ that for any $i \in \mathbb{N}$, if $j\geq i$, then $a_{m_{j}} \in N_{\frac{1}{i}}(L)$. $\{ m_{k} \}$ is strictly increasing and in the natural numbers, so we can look at the subsequence $\{ a_{m_{k}} \}$.

Let $\varepsilon>0$ be given. By [[Mathematical Analysis#Theorem 1 3|Theorem 1.3]] there exists a $P \in \mathbb{N}$ such that $\frac{1}{P}<\varepsilon$. If $n>P$ then  $a_{m_{n}}\in N_{\frac{1}{P}}(L)\subseteq N_{\varepsilon}(L)$, satisfying the definition of a limit and showing that $\lim\limits_{ k \to \infty }a_{m_{k}}=L$. This makes $L$ a subsequential limit of $\{ a_{n} \}$ completing the proof.