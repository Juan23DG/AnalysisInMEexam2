# ME Analysis 1 — Exam 2: Quick Method-Picker Guide & Formula Sheet

> **How to Use This Guide:** Look down the **"What Your ODE Looks Like"** column to spot your problem type, grab the **Formula**, and follow the **Short Steps**.

---

## 1. First-Order ODE Guide (Only $y'$ Appears)

| 👀 What Your ODE Looks Like | 📐 Key Formula | ✅ Short Steps (Plain English) |
| :--- | :--- | :--- |
| **Separable**<br>$y' = g(x)\,h(y)$ *(can split $x$'s and $y$'s)* | $\displaystyle\int \frac{1}{h(y)}\,dy = \int g(x)\,dx + C$ | **1.** Group $y$'s with $dy$ and $x$'s with $dx$, then integrate.<br>**2.** Plug in $y(x_0)$ for $C$ (match $+$ or $-$ root sign to $y_0$).<br>**3.** *Domain:* open interval around $x_0$ before denom $=0$ or $\ln/\sqrt{\cdot}$ breaks. |
| **Linear 1st-Order**<br>$a(x)y' + b(x)y = g(x)$ *(plain $y'$ and $y$ only)* | $\mu(x) = e^{\int P(x)\,dx}$<br>$\mu(x)y = \displaystyle\int \mu(x)Q(x)\,dx + C$ | **1.** **Divide first** so $y'$ stands alone: $y' + P(x)y = Q(x)$.<br>**2.** Find $\mu(x)$ (keep any minus sign on $P$!).<br>**3.** Integrate RHS, then divide **every term (even $+C$)** by $\mu(x)$. |
| **Bernoulli ($y^n$ Power)**<br>$y' + P(x)y = Q(x)y^n$ *(extra $y^n$ on RHS)* | $u = y^{1-n}$<br>$u' + (1-n)Pu = (1-n)Q$ | **1.** Divide so $y'$ stands alone & check $n$ *(e.g. $n=-2 \implies u=y^3$)*.<br>**2.** Plug in $u = y^{1-n}$ to turn it into a Linear ODE.<br>**3.** Solve for $u(x)$ with $\mu(x)$, then solve back for $y(x)$. |
| **$y/x$ Ratio (Homogeneous)**<br>$y' = F(y/x)$ *(or equal total power in each term)* | $y = vx$<br>$y' = v + x v'$ | **1.** Rewrite in terms of $y/x$, then plug in $y = vx$ and $y' = v + xv'$.<br>**2.** Separate $v$ and $x$: $\int \frac{dv}{F(v)-v} = \int \frac{dx}{x} + C$.<br>**3.** Integrate, then replace $v$ with $y/x$. |
| **Inside Group ($ax+by+c$)**<br>$y' = f(ax + by + c)$ *(like $\cos(x+y)$)* | $u = ax + by + c$<br>$u' = a + b y'$ | **1.** Set $u = ax+by+c$ and replace $y'$ using $u' = a + by'$.<br>**2.** Separate $u$ and $x$: $\int \frac{du}{a + bf(u)} = \int dx + C$.<br>**3.** Integrate, then plug $ax+by+c$ back in for $u$. |

---

## 2. 2nd & Higher-Order ODE Guide ($y'', y''', y^{(4)}$)

| 👀 What Your ODE Looks Like | 📐 Key Formula | ✅ Short Steps (Plain English) |
| :--- | :--- | :--- |
| **Const.-Coeff Homogeneous**<br>$ay'' + by' + cy = 0$<br>*(numbers in front, RHS $= 0$)* | Plug $y = e^{rx} \implies$<br>$ar^2 + br + c = 0$ | Solve for roots $r$ *(for $y'''$, test $r=\pm 1,\pm 2$ + synthetic div.)*:<br>• **2 Real ($r_1\neq r_2$):** $c_1 e^{r_1 x} + c_2 e^{r_2 x}$<br>• **Repeated ($r$):** $(c_1 + c_2 x)e^{rx}$ *(add $x$ power for each repeat)*<br>• **Complex ($\alpha\pm i\beta$):** $e^{\alpha x}(c_1\cos\beta x + c_2\sin\beta x)$ |
| **Cauchy-Euler ($x^k y^{(k)}$)**<br>$ax^2 y'' + bxy' + cy = 0$<br>*($x$ power matches derivative)* | Plug $y = x^m \implies$<br>$am^2 + (b-a)m + c = 0$ | Solve for $m$ *(watch out: middle term is $(b-a)m$, not $bm$!)*:<br>• **2 Real ($m_1\neq m_2$):** $c_1 x^{m_1} + c_2 x^{m_2}$<br>• **Repeated ($m$):** $(c_1 + c_2\ln x)x^m$<br>• **Complex ($\alpha\pm i\beta$):** $x^\alpha[c_1\cos(\beta\ln x) + c_2\sin(\beta\ln x)]$ |
| **Reduction of Order**<br>RHS $= 0$ AND **one solution $y_1(x)$ is given** | $\displaystyle y_2 = y_1\int \frac{e^{-\int P(x)\,dx}}{y_1^2}\,dx$<br>*(or sub $y_2 = u(x)y_1(x)$)* | **1.** **Divide first** so $y''$ has a $1$ in front: $y'' + P(x)y' + Q(x)y = 0$.<br>**2.** Use the integral formula *OR* plug in $y_2 = u y_1$ (plain $u$ terms must cancel to $0$, then set $w = u'$). |
| **Undetermined Coeffs (Guess $y_p$)**<br>Const. coeffs & RHS has **only** $x^m$, $e^{\alpha x}$, $\sin$, $\cos$ | • **Poly:** $Ax^2+Bx+C$ *(all powers)*<br>• **Exp:** $Ae^{\alpha x}$<br>• **Trig:** $A\cos\beta x + B\sin\beta x$ *(both!)* | **1.** Find $y_c$ **first**!<br>**2.** **Match $y_c$?** Multiply that guess group by $x$ (or $x^2$).<br>**3.** Plug $y_p$ into ODE & match terms to get $A, B$.<br>**4.** Write $y = y_c + y_p$, **then** plug in $y(0), y'(0)$ for $c_1, c_2$. |
| **Variation of Parameters (VoP)**<br>RHS has $\sec, \tan, \csc, \ln, \frac{e^x}{x}$ **OR** variable coeffs | $W = y_1 y_2' - y_1' y_2$<br>$u_1 = -\int \frac{y_2 g}{W}dx,\; u_2 = \int \frac{y_1 g}{W}dx$ | **1.** **Divide first** so $y''$ has a $1$ in front to get the true $g(x)$!<br>**2.** Grab $y_1, y_2$ from $y_c$ and find Wronskian $W \neq 0$.<br>**3.** Integrate $u_1, u_2$ (no $+C$) and write $y_p = u_1 y_1 + u_2 y_2$. |

---

## 3. Laplace Transform Pairs & Key Rules

| Time $f(t)$ | Transform $F(s) = \mathcal{L}\{f(t)\}$ | Rule Name | How It Works |
| :--- | :--- | :--- | :--- |
| $1$ $\;\big|\;$ $t^n$ | $\dfrac{1}{s}$ $\;\Big|\;$ $\dfrac{n!}{s^{n+1}}$ | **Derivatives ($y', y''$)** | $\mathcal{L}\{y'\} = sY - y(0)$<br>$\mathcal{L}\{y''\} = s^2Y - sy(0) - y'(0)$ |
| $t^p$ *(fractional)* | $\dfrac{\Gamma(p+1)}{s^{p+1}}$ $\;\big(\Gamma(\tfrac{1}{2})=\sqrt{\pi},\,\Gamma(p+1)=p\Gamma(p)\big)$ | **$e^{at}$ Shift ($s$-Shift)** | $\mathcal{L}\{e^{at}f(t)\} = F(s-a)$ *(replace $s \to s-a$)* |
| $e^{at}$ | $\dfrac{1}{s-a}$ | **Multiply by $t^n$** | $\mathcal{L}\{t^n f(t)\} = (-1)^n F^{(n)}(s)$ $\;\big|\;$ $\mathcal{L}\{t^n e^{at}\} = \dfrac{n!}{(s-a)^{n+1}}$ |
| $\sin\omega t$ $\;\big|\;$ $\cos\omega t$ | $\dfrac{\omega}{s^2+\omega^2}$ $\;\Big|\;$ $\dfrac{s}{s^2+\omega^2}$ | **Step Delay $u(t-c)$** | Forward: $\mathcal{L}\{g(t)u(t-c)\} = e^{-cs}\mathcal{L}\{g(t+c)\}$<br>Inverse: $\mathcal{L}^{-1}\{e^{-cs}F(s)\} = f(t-c)u(t-c)$ |
| **Step** $u(t-c)$ | $\dfrac{e^{-cs}}{s}$ | **Convolution & $\int_0^t y$** | $\mathcal{L}\{f*g\} = F(s)G(s)$ $\;\Big|\;$ $\mathcal{L}\!\left\{\int_0^t y\,d\tau\right\} = \dfrac{Y(s)}{s}$ |
| **Impulse** $\delta(t-c)$ | $e^{-cs}$ $\;\big(\text{at } t=0:\; \mathcal{L}\{\delta(t)\} = 1\big)$ | **Resonance / $\sin^2$** | $\mathcal{L}^{-1}\!\left\{\frac{2\omega s}{(s^2+\omega^2)^2}\right\} = t\sin\omega t$ $\;\big|\;$ $\sin^2\omega t = \frac{1-\cos 2\omega t}{2}$ |

---

## 4. Short Game Plans for Laplace & Mechanics Problems

1. **Finding an Inverse Laplace Transform ($\mathcal{L}^{-1}\{F(s)\}$):**
   - **See $e^{-cs}$ on top?** Set $e^{-cs}$ aside, invert $F(s) \to f(t)$ first, then replace **every $t$ with $(t-c)$** and multiply by $u(t-c)$.
   - **Denominator factors?** Use Partial Fractions (cover-up shortcut for simple poles).
   - **Denominator won't factor?** Complete the square $(s+\alpha)^2 + \omega^2$, then match $(s+\alpha)$ for $e^{-\alpha t}\cos\omega t$ and $\omega$ for $e^{-\alpha t}\sin\omega t$.
2. **Solving an IVP with Switches $u(t-c)$ or Hammer Blows $\delta(t-c)$:**
   - **Step 1:** Rewrite piecewise forces using steps: $f(t) = f_{\text{start}} + (f_{\text{new}} - f_{\text{start}})u(t-c)$. *(Pulse on $[a,b]$: multiply by $[u(t-a)-u(t-b)]$.)*
   - **Step 2:** Take $\mathcal{L}$ of the whole equation & plug in $y(0), y'(0)$ right away.
   - **Step 3:** Solve for $Y(s)$ (keep $e^{-cs}$ pieces separate from plain pieces), split fractions, and invert back to $y(t)$.
3. **Springs ($mx''+cx'+kx = F(t)$), RLC Circuits & Integral Equations:**
   - **Damping check:** $c^2 > 4mk$ (overdamped) • $c^2 = 4mk$ (critical: $(c_1+c_2 t)e^{-rt}$) • $c^2 < 4mk$ (underdamped) • $c=0, \omega=\omega_n$ (resonance: $t\sin\omega_n t$).
   - **Transfer Function (zero ICs):** $H(s) = \frac{X(s)}{F(s)} = \frac{1}{ms^2+cs+k}$; impulse response $h(t) = \mathcal{L}^{-1}\{H(s)\}$.
   - **Integral Eq. ($\int_0^t$):** Transform $\int_0^t k(t-\tau)y(\tau)\,d\tau \to K(s)Y(s)$, solve algebraically for $Y(s)$, and invert.
4. **Beam Deflection ($EI\,w^{(4)}(x) = q(x)$):**
   - **Step 1:** Point load at $x=a$ is $P_0\delta(x-a)$; distributed load starting at $a$ is $q_0 u(x-a)$.
   - **Step 2:** Transform using $x=0$ supports (**Clamped:** $w=w'=0$; **Pinned:** $w=w''=0$; **Free:** $w''=w'''=0$); call the 2 unknown $x=0$ derivatives $C_1, C_2$.
   - **Step 3:** Invert using $\mathcal{L}^{-1}\!\left\{\frac{e^{-as}}{s^{n+1}}\right\} = \frac{(x-a)^n}{n!}u(x-a)$, then plug in the $x=L$ support conditions to find $C_1, C_2$.
