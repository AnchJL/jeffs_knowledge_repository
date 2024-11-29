---
{"dg-publish":true,"permalink":"/Math/Number Theory/Chinese Remainder Theorem/","created":"2024-10-17T01:23:42.560-04:00","updated":"2024-11-23T17:26:44.647-05:00"}
---


#Math/NumberTheory 

The *Chinese Remainder Theorem* was a theorem by the ancient Chinese mathematician, Sun Tzu (not the war general).

Consider any system of congruences:
$$
\begin{align}
&x\equiv r_1 \pmod{n_1}\\
&x\equiv r_2 \pmod{n_2}\\
&...\\
&x\equiv r_m \pmod{n_m}\\
\end{align}
$$
Where modules $m_1$, $m_2$, $m_3$, are coprime to each other (this means that the [[Math/Number Theory/Greatest Common Divisor\|Greatest Common Divisor]] between them should be $1$). The Chinese remainder theorem states that for any system of congruence (like the one above), there exists a unique solution up to a certain modulus.

The solution to any system of linear congruences is the following:
$$
x=\sum_{i}{r_iN_ix_i}
$$
Where $N_i$ is the product of all the $n$ moduli divided by $n_i$.

> [!Example] Solve this system of linear congruences:
> 1. $x\equiv1\pmod{3}$
> 2. $x\equiv2\pmod{4}$
> 3. $x\equiv4\pmod{5}$
> 
> **Solution**:
> 4. $N=3*4*5$
> 5. $N_1=\frac{N}{3}=20$
> 6. $N_2=\frac{N}{4}=15$
> 7. $N_3=\frac{N}{5}=12$
> 
> Now we need to find the inverses of $N_1$, $N_2$, and $N_3$:
> - $N_1x_1\equiv1\pmod{3}$
> 	8. $20x_1\equiv1\pmod{3}$
> 	9. Since $20\equiv2\pmod{3}$, then we can reduce (8) into $2x_1\equiv1\pmod{3}$
> 	10. $x_1\equiv2\pmod{3}\Rightarrow x_1=2$
> - $N_2x_2\equiv1\pmod{4}$
> 	11. $15x_2\equiv1\pmod{4}$
> 	12. Since $15\equiv3\pmod{4}$, then we can reduce (1) into $3x_2\equiv1\pmod{4}$
> 	13.  $x_2\equiv 3\pmod{4}\Rightarrow x_2=3$
> - $N_3x_3\equiv1\pmod{5}$
> 	14. $12x_3\equiv1\pmod{5}$
> 	15. Since $12\equiv2\pmod{5}$, then we can reduce (14) into $2x_2\equiv1\pmod{5}$
> 	16. $x_2\equiv3\pmod{5} \Rightarrow x_3=3$
> 
> Our solution is in the form:
> $$
> \begin{align}
> &x=x_1N_1r_1+x_2N_2r_2+x_3N_3r_3\\\\
> &=2*20*1+3*15*2+3*12*4\\\\
> &=40+90+144\\\\
> &=274\\\\
> &\text{Check:}\\\\
> &274\mod{3}=274-273=1&\checkmark\\\\
> &274\mod{4}=274-272=2&\checkmark\\\\
> &274\mod{5}=274-270=4&\checkmark\\\\
> \end{align}
> $$
> Although $x=274$ is a solution, it is not the lowest possible solution. We have a unique solution modulo 60.
> $$
> \begin{align}
> &274\mod{60}=274-240=34\\\\
> &x\equiv34\pmod{60}\\\\
> &\text{Check:}\\\\
> &34\mod{3}=34-33=1&\checkmark\\\\
> &34\mod{4}=34-32=2&\checkmark\\\\
> &34\mod{5}=34-30=4&\checkmark\\\\
> \end{align}
> $$