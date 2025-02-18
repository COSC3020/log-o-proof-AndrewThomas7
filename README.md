# Asymptotic Equivalences

In the lectures, we said that logarithms with different bases don't affect the
asymptotic complexity of an algorithm. Prove that $O(\log_{2} n)$ is the same as
$O(\log_{5} n)$. Use the mathematical definition of $O$ -- do a formal proof,
not just the intuition.

I have started with the formal definition of $O$ below. Add your answer to this
markdown file. [This
page](https://docs.github.com/en/get-started/writing-on-github/working-with-advanced-formatting/writing-mathematical-expressions)
might help with the notation for mathematical expressions.

$T(n) \in O(f(n)) \iff \exists c, n_0: T(n) \leq c \cdot f(n) \forall n \geq n_0$

“I certify that I have listed all sources used to complete this exercise, including the use
of any Large Language Models. All of the work is my own, except where stated
otherwise. I am aware that plagiarism carries severe penalties and that if plagiarism is
suspected, charges may be filed against me without prior notice.”-Andrew Thomas

## Sources

1.)-https://www.youtube.com/watch?v=FFm-zaFW_X4- Refreshed my knowledge on change of base formula as it seemed a good avenue for the proof.

2.)-https://stackoverflow.com/questions/6701809/base-of-logarithms-in-time-complexity-algorithms -Used to get an intitution for why the time complexities might be the same


# The Proof
*Goal:* Show that $O(log_2(n))$ = $O(log_5(n))$

Proof:

$[\implies ]$(Proof in the forward direction)

Assume that $Log_5(n) \in O(log_2(n))$.

$\implies$ $\exists$ $c,n_o$ such that,

$f(n) \leq c \cdot log_2(n) \hspace{2mm} \forall \hspace{1mm}n \geq n_o$.  Where $f(n)$ is any such function that satisfies $f(n)\in O(log_2(n))$

Rewriritng with the change of base formula we obtain:

= $f(n)\leq c.\frac{log_{10}(n)}{log_{10}(2)}$

Let $c=\frac{log_{10}(2)}{log_{10}(5)}$

$\implies f(n) \leq \frac{log_{10}(2)}{log_{10}(5)} \cdot \frac{log_{10}(n)}{log_{10}(2)}$

$\implies f(n) \leq \frac{log_{10}(n)}{log_{10}(5)} $

$\implies f(n) \leq log_5(n)$

$\implies f(n)=log_5(n)$

Thus $O(log_2(n))$ = $O(log_5(n))$

The reverse direction  $[ \Longleftarrow ]$ is trivial to prove and as such I have left it out. (It would just consist of my same steps backwards)

Q.E.D

