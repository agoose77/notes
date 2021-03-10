Reactions
=========

Nuclear reactions are typically written in the form $X(a,b)Y$, which is effectively shorthand for $a+X\rightarrow Y+b$, where $a$ is the projectile, $X$ the target, and $b,Y$ the products.

Q Value
-------
In any reaction, the total energy is conserved, i.e.
$$
\tag{a}
T_a + m_ac^2 + T_X + m_Xc^2 = T_b + m_bc^2 + T_Y + m_Yc^2\,,
$$
where $m_X$ is the _rest mass_ of $X$. The *Q value* of the reaction is simply the change in mass energy
$$
\begin{aligned}
\tag{b}
Q &= \pqty{m_a+m_X-m_b-m_Y}c^2\\
&= T_b+T_Y - T_a-T_X\,.
\end{aligned}
$$

Excitation Energy
-----------------
<!-- this is a simplified case of the X(a,b)Y case i.e. X(Y, Z*)-->
Consider a simple two particle collision of $a$ and $X$, which leads to the formation of an (excited) compound nucleus $Z^*$. 

```bob
                   .-----.                    |
                   | Lab |                    |
                   '-----'                    |
     _____                       _____        |            _____    
   ,'     `.                   ,'     `.      |          ,'     `.  
  /         \     u1      u2  /         \     |         /         \    u(cm)
 (     a     ) --------> <-- (     X     )    |        (     Z*    )  ----->
  \         /                 \         /     |         \         / 
   `._____,'                   `._____,'      |          `._____,'  
                                                       
```

*In the centre of mass frame*, from **(a)** we have
$$
    m_{Z^*}c^2 = m_ac^2 + T_a + m_Xc^2 + T_X\,.
$$ 
<!-- If it's not immediately clear below, E = γmc^2 = mc^2 + T where T = (γ-1)mc^2 -->
This also follows from the definition of the invariant mass :
$$m_{Z^*}c^2 = \sqrt{E_{Z^*}^2 - (p_{Z^*}c)^2}\,.$$
With $\norm{\vb{p_{Z^*}}}=0$ in a centre of mass frame, this expression simplifies to $m_{Z^*}c^2 = E_{Z^*} = E_a+E_X$.

From **(b)**, the Q value for this reaction is simply 
$$
    \tag{d}
    Q = \pqty{m_a + m_X - m_Z^*}c^2=-\pqty{T_a+T_X}\,,
$$
More frequently we are interested in the *excitation* $E_\text{ex} = \pqty{m_{Z^*}-m_Z}c^2$ above the ground state energy $m_Zc^2$. In this case, it is more convenient to define the Q value in terms of the (known) ground-state value:
$$
\begin{aligned}
\tag{e}
    Q &= \pqty{m_a + m_X - m_{Z^*}}c^2\\
    &= \pqty{m_a + m_X - \pqty{m_Z + \Delta m_{Z^*}}}c^2\\
    &= \pqty{m_a + m_X - m_Z}c^2 - \Delta m_{Z^*}c^2\\
    &= Q_\text{gs}-E_\text{ex}\,,
\end{aligned}
$$
where $\Delta m_{Z^*}$ is the additional mass due to excitation. 
With $Q$ given by **(d)**, it follows from **(e)** that $E_\text{ex} = Q_\text{gs} + T_a+T_X$.