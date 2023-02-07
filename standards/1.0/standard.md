# OpenLit Standard v1.0

This is the Markdown resource for the OpenLit Standard (1.0).

## Preamble

### Notation

This document uses various notation to describe the OpenLit notation in unambigous completeness. To remain completely unambigious, a description of the notation used is
relevant. 

### Quick Note on Parsing

The set of all characters within a given document $D_n$ is $D^{\star}_n$.


For a given subset (match-case), we say the primary matching function $m_{\phi}(D^{\star}_n)$ returns the start and end indexes of the first set of characters which match the restrictrion expression $\phi$. If we then create a $k$-th set 

$$D^{\star}_{n, k}$$

which removes the elements before the end of the $k$-th match-case, the primary matching function $m_{\phi}(D^{\star}_{n, k})$ will match the $k+1$-th case. This is expressed in the following theorem:

$$
\begin{align}
\sum_{n = 1}^\infty M_{\phi}(D^{\star}_{a, n}) &= \mathrm{count}_{D^{\star}_{a, n}}(\phi) \\
\end{align}
$$

Where

$$
\begin{equation}
M_\phi(C) =
\left\(
    \begin{array}{lr}
        1, & \text{if } m_{\phi}(C) \neq \emptyset\\
        0, & \text{if } m_{\phi}(C) = \emptyset
    \end{array}
\right\)
\end{equation}
$$

and $\mathrm{count}_C(\phi)$ is the number of matches under the matching function $\phi$ to the set $C$. As a result, single-matching functions can still match *all* cases using a progressive system.

#### Regular Expressions

Assume all Regular Expressions as [Perl Compatible Regular Expressions](https://pcre.org). 
