I followed this course by Prof. Leeb during my #3rd_Sem a the #LMU. A considerable part of the following notes (and hence of the program of the course) are already present in [[Analysis II (Lecture)]], the approach of this lecture was more theoretical (topological).
### I. Measure Theory
#### I.1 Measure Problem
XX
#### I.2 Measuring Volume with Finite Divisions
##### I.2.1 Set-theoretic Rings and Algebras
- Def. a set-ring is $\mathcal{R} \subseteq \mathcal{P}(X)$ s.t. it is an (alg.) sub-ring of $(\mathcal{P}(X), \Delta, \cap)$.
	- for $A \Delta B := \{x \in X : (x \in A \lor x \in B) \land \lnot (x \in A \land x \in B)\}$, $\chi_\emptyset \equiv 0$ and $\chi_X \equiv 1$.
	- for $\mathcal{R} \subset \mathcal{P}(X)$: $\mathcal{R}$ is a ring $\Leftrightarrow \emptyset \in \mathcal{R} \land \mathcal{R}$ is $\setminus$-stable $\land \mathcal{R}$ is $\cup$-stable.
		- $A \Delta B = (A \setminus B) \cup (B \setminus A)$, $A \cap B = A \setminus (A \setminus B)$ 
		-  $\forall_{A, B \in \mathcal{R}}A \setminus B \in \mathcal{R} \land A \cap B \in \mathcal{R} \land B \setminus A \in \mathcal{R}$ 
- Def. a set-alg. $\mathcal{A}$ is a set-ring s.t. $1_\mathcal{A} \in \mathcal{A}$.
	 - $\mathcal{A}$ is a set-alg. $\Leftrightarrow \emptyset \in \mathcal{A} \land \mathcal{A}$ is $\cup$-stable $\land \mathcal{A}$ is $\cdot^C$-stable
	-  $\forall_{A, B \in \mathcal{R}}A \setminus B \in \mathcal{R} \land A \cap B \in \mathcal{R} \land B \setminus A \in \mathcal{R} \land (A \cup B)^C$
- For $\mathcal{E} \subseteq \mathcal{P}(X)$, def. the set-ring  $\mathcal{R}_\mathcal{E} = \bigcap\{\mathcal{R} : \mathcal{E} \subseteq \mathcal{R} \land \mathcal{R}$ is a ring$\}$ on $X$.
- Define $\mathcal{F}_0 \subseteq ... \subseteq \mathcal{F}_n \subseteq ... \subseteq \mathcal{P}(X)$, for $\mathcal{F}_0:= \mathcal{E} \cup \emptyset$, $\mathcal{F}_n := \{A \setminus B, A \cup B : A, B \in \mathcal{F}_{n-1}\} \supseteq \mathcal{F}_{n -1}$;  $\bigcup_{n \in \mathbb{N}} \mathcal{F}_n$. 
	- $\mathcal{R}_\mathcal{E}$ is the smallest ring containing $\mathcal{E}$. ==Q==
- Def. $\mathcal{H} \subseteq \mathcal{P}(X)$ halfr. if (i) $\emptyset \in \mathcal{H}$, (ii) $\mathcal{H}$ is $\mathcal{H}$-st., (iii) $\forall_{A, B \in \mathcal{H}} \exists_{C_1, ..., C_n \in \mathcal{H}} A \setminus B = C_1 \sqcup ... \sqcup C_n$. 
	- $\mathcal{R}$ is an hafr.
	- Principal Exampe, (PE) $\mathcal{I} = \{[a, b) : a \le b \land a, b \in \mathbb{R}\}$ is halfr. on $\mathbb{R}$.
	- (Simultane Zerlegung) $\forall_{H_1, ..., H_n \in \mathcal{H}} \exists_{H_1', ..., H_n' \in \mathcal{H}} H_i = H_j', ..., H_{j'}'$ 
	- $\mathcal{R}(\mathcal{H})$ def. ==Q==
- **Products**
	- $\mathcal{F}_1 *...* \mathcal{F}_n : = \{M_1 \times ... \times M_n: \forall_{i \le n} M_i \in \mathcal{F}_i\} \subseteq \mathcal{P}(X_1 \times ... \times X_n)$, $\cup$-st. cover. for $\mathcal{F}_i \subseteq \mathcal{P}(X)$,
		- squares
	- $\mathcal{F}_1 \boxtimes ... \boxtimes \mathcal{F}_n := \{$finite union of subsets of $\mathcal{F}_1 *...*\mathcal{F}_n\}$
		- union of squares
	-  $\mathcal{Z}(\mathcal{F}_1, ..., \mathcal{F}_n) := \{\pi_k^{-1}(M_k) : M_k \in \mathcal{F}_k, 1 \le k \le n\}$ where $\pi_k^{-1}: X_1 \times ... \times X_n \rightarrow X_k$ is a proj.
		- Cylinder
	- $\mathcal{H}_1 *...* \mathcal{H}_n$ is an halfr. on $X_1 \times ... \times X_n$, (prod. of halfr.)
	- $\mathcal{H}_1 \boxtimes ... \boxtimes \mathcal{H}_n = \mathcal{R}(\mathcal{H}_1) \boxtimes ... \boxtimes \mathcal{R}(\mathcal{H}_n)$
	- (PE) $[a, b) : = [a_1, b_1) \times ... \times [a_d, b_d)$ elem. of $Q^d = \mathcal{I} * ....* \mathcal{I} \subset \mathcal{P}(\mathbb{R}^d)$ halfr., $\mathcal{R}(Q^d) = \mathcal{F}^d : = \mathcal{I} \boxtimes ... \boxtimes \mathcal{I} \subset \mathcal{P}(\mathbb{R}^d)$ (figures).
		- (Zerl. Lemma) every figure is a disj. union of finitely many squares
		- Any finite union of squares is also a figure
##### I.2.2 Content
- $\mu: \mathcal{H} \rightarrow [0, \infty]$ s.t. (i) $\mu(\emptyset) = 0$, (ii) $\mu(A_1 \sqcup ... \sqcup A_n) = \mu(A_1) + ...  + \mu(A_n) \land A_1 \sqcup ... \sqcup A_n \in \mathcal{H}$ (cont.)
- (PE) $\lambda_\mathcal{I}: Q^1 \rightarrow [0, \infty), [a, b) \mapsto b-a$ (euclidian lenght)
- $\forall_{A, B \in \mathcal{H}} A \subseteq B \rightarrow \mu(A) \le \mu(B)$ (monotony)
- $\forall_{A_1, ..., A_n \in \mathcal{H}} \mu(A_1 \cup ... \cup A_n) \le \mu(A_1) + ... + \mu(A_n)$ (subadditivity)
- For $\mu: \mathcal{H} \rightarrow [0, \infty]$ ex. uniq. $\overline{\mu}: \mathcal{R}(\mathcal{H}) \rightarrow [0, \infty]$.  
	- How to extend the content? ==Q==
- (PE) $\lambda^1_{Q_1}: Q^1 \longrightarrow [0, \infty], [a, b) \mapsto b-a$ extends to $\lambda^1_{\mathcal{F}^1}: \mathcal{F}^1 \longrightarrow [0, \infty]$.
- **Products**
	- If $(\mu_1 \times ... \times \mu_n)(\mathcal{H}_1 \times ... \times \mathcal{H}_n) = \mu_1(H_1) \cdot ... \cdot \mu_n(H_n)$, $\mu_1 \times ... \times \mu_n$ cont. $\mathcal{H}_1 * ... * \mathcal{H}_n$
		- convention: $0 \cdot \infty = 0$
	- (PE)  $\lambda^d_{Q^d} := \lambda^1_{Q^1} \times ... \times \lambda^1_{Q^1}$ ($d$-times) on $Q^d = Q^1 * ... * Q^1 \subset \mathcal{P}(\mathbb{R}^d)$
	- $\mu_1 \boxtimes ... \boxtimes \mu_n$ uniq. cont. on $\mathcal{R}_1 \boxtimes ... \boxtimes \mathcal{R}_n \subset \mathcal{P}(X_1 \times ... \times X_n)$ s.t.:
		- $(\mu_1 \boxtimes ... \boxtimes \mu_n)(M_1 \times ... \times M_n) = \mu_1(M_1) \cdot ... \cdot \mu_n(M_n)$,
			- recall: $(M_1 \times ... \times M_n) \in \mathcal{R}_1 * ... * \mathcal{R}_n$ for $M_i \in \mathcal{R}_i$
	- (PE) $\lambda^d_{\mathcal{F}^d}$ is unique
#### I.3 Measuring Volume with Countable Divisions
##### I.3.1 Pre-measures
- def. ==Q==
- $A_n \nearrow A := \bigcup_{n = 1}^\infty A_n = A$ for $(A_i)_{i \in [1, n]}$ a $\subseteq$-chain (inside approximation), similarly $A_n \swarrow A$.
- let $A_n \nearrow A \land A'_n \swarrow A$ then $\lim_{n \rightarrow \infty} \mu(A_n) \le \mu(A) \le \lim_{n \rightarrow \infty} \mu(A'_n)$.
- **Products**
	- $\mu_1 \boxtimes ... \boxtimes \mu_n$ pmeas.
##### I.3.2 $\sigma$-Algebras
- $\mathcal{A} \subset \mathcal{P}(X)$ is $\sigma$-al. if: (i) $\emptyset \in \mathcal{A}$, (ii) $(A_n)_{n \in \mathbb{N}} \subseteq \mathcal{A} \Rightarrow \bigcup_{n \in \mathbb{N}} A_n \in \mathcal{A}$ ($\sigma$-$\cup$-st.), (iii) $\cdot^C$-st.
	- eq. to: (i)* $X \in \mathcal{A}$, (ii)* $(A_n)_{n \in \mathbb{N}} \subseteq \mathcal{A} \Rightarrow \bigcap_{n \in \mathbb{N}} A_n \in \mathcal{A}$ ($\sigma$-$\cap$-st.), (iii) $\cdot^C$-st.
- By transf. ind. define $\sigma(\mathcal{E}):= \mathcal{E}_{\omega_1}$:
	- for $A \subseteq \mathcal{P}(X)$, $A^\vartheta :=$ ==Q==
	- $\mathcal{E}_0 := \mathcal{E} \cup \{\emptyset\}$
	- $\mathcal{E}_n := \mathcal{E}_{n-1}^\vartheta$
	- $\mathcal{E}_\lambda := (\bigcup_{n < \lambda} \mathcal{E}_n)^\vartheta$ for $\lambda$ limit ordinal
- **Topological Origin**
	- $\mathcal{B}(X) := \sigma(\mathcal{T})$ for $(X, \mathcal{T})$ top. sp.
		- (PE) $\mathcal{B}^d := \mathcal{B}(\mathbb{R}^d)$
			- $\mathcal{B}^d = \sigma(A)$ for any of the following options
				- $A$ are open subsets of $X$, i.e. the topology.
				- $A$ are the closed subsets of $X$.
				- $A$ are the compact subsets of $X$.
				- $A$ are the open metrical balls
				- $A$ are the closed metrical balls
				- $A$ are the open rectangles
				- $A$ are the half-open rectangles, i.e. $Q^d$
			- $\mathcal{B}^d = \sigma(Q^d)$
- **Dynkin Systems**
	- $\mathcal{D} \subseteq \mathcal{P}(X)$ is dyn. if (i) $\emptyset \in \mathcal{D}$, (ii)$(A_n)_{n \in \mathbb{N}} \subseteq \mathcal{D} \Rightarrow \bigsqcup_{n \in \mathbb{N}} A_n \in \mathcal{D}$, (iii) is $\cdot^C$-st.
	- $\mathcal{A}$ is dyn. and if $\mathcal{D}$ is $\cap$-st. it is $\sigma$-al.
	- $\forall_{D_1, D_2 \in \mathcal{D}} D_1 \subseteq D_2 \rightarrow D_2 \setminus D_1 \in \mathcal{D}$
	- $\mathcal{D}|_D : = \{M \subset D |M \in \mathcal{D}\} \subset \mathcal{P}(D)$ (Spur) is dyn on $D$.
	- $\mathcal{D}_D := \{M \subset X | M \cap D \in \mathcal{D}\} \subset \mathcal{P}(X)$ is dyn on $X$. 
	- $\mathcal{E}$ $\cap$-st., $\mathcal{D}(\mathcal{E})$ is $\sigma$-al.
- **The Measurable Category**
	- XX
- **Products**
	- $\mathcal{A}_1 \otimes ... \otimes \mathcal{A}_n = \sigma(Z(\mathcal{A}_1, ..., \mathcal{A}_n))$ ==Q==
		- $Z(\mathcal{A}_1, ..., \mathcal{A}_n) = \{\pi^{-1}_k (M_k) | M_k \in \mathcal{A}_k \land k \in [1, n]\}$
##### I.3.3 Measures
- $\mu: \mathcal{A} \rightarrow [0, \infty]$ is a meas.
	- eq. $\mu: \mathcal{A} \rightarrow [0, \infty]$ a meas. on $\mathcal{A}$ if (i) $\mu(\emptyset) = 0$, (ii) $\mu(\bigsqcup_{n \in \mathbb{N}}A_n) = \sum_{n \in \mathbb{N}}\mu(A_n)$
- **External Measures**
	- $\mu^*(M) : = inf\{\sum^\infty_{n=1}\mu(A_n):(A_n)_{n\in \mathbb{N}} \subseteq \mathcal{H} \land \bigcup^\infty_{n=1}A_n \supseteq M\}$ for $\mu$ cont.
		- if empty $\mu^*(M) = inf(\emptyset) = \infty$
		- it is enough to look at the p.disj. $(A_n)_{n \in \mathbb{N}}$.
		- $\overline{\mu^*} = \mu^*$
	- $\mu^*: \mathcal{P}(X) \rightarrow [0, \infty]$ ext. meas iff
		- $\mu^*(\emptyset) = 0$
		- $\forall_{M, M' \subseteq X} M \subseteq M' \rightarrow \mu^*(M) \le \mu^*(M')$ (monotony)
		- $(M_n)_{n \in\mathbb{N}} \subseteq \mathcal{P}(X)$, $\mu^*(\bigcup^\infty_{n = 1} M_n) = \sum^\infty_{n = 1} \mu^*(M_n)$ ($\sigma$-subadditivity)
	- Similarly define the internal measure, $\mu_*$
- **Motivation**
	- $\mu^*(M) -\mu_*(M) = \mu^*(M) +\mu^*(R-M)-\mu^*(R) \ge 0$, bound. $R$ of a fuzzy shape $M$ (discr.)
	- call $M$ meas. if $\forall_{S \subset X}\mu^*(S) = \mu^*(S \cap M) + \mu^*(S \cap M^C)$.
	- $\mu^*(N) = 0$ (nullset)
	
- **Extensions of Pre-measures to Measures**
	- (Carathéodory, 1914) $\mathcal{A}^*, \mu^*|_{\mathcal{A}^*}$ are resp. a $\sigma$-al. and a meas. ==Q==
		- $\mathcal{A}^* := \{M \subseteq X : M$ is $\mu^*$-meas$\}$.
		- (i) $\sigma(\mathcal{R}) \subseteq \mathcal{A}^*$
		- (ii) $\mu^*|_{\sigma(\mathcal{R})}$ is a meas.
			- (i), (ii) $\Rightarrow \mu^*|_\mathcal{R}$ prem., also $\mu^*|_\mathcal{R} \le \mu$ (recall $dom(\mu) = \mathcal{R}$)
		- $\mathcal{H} \subseteq \mathcal{P}(X)$, $\mu: \mathcal{H} \rightarrow [0, \infty]$ meas., then $\mu$ is finite if $\mu(X) < \infty$ (finite)
	- $\mathcal{H} \subseteq \mathcal{P}(X)$, $\mu: \mathcal{H} \rightarrow [0, \infty]$ meas., it is $\sigma$-fin. if ex $(H_n)_{n \in \mathbb{N}}$ s.t. $\forall_{x \in X} \exists_{n \in \mathbb{N}} x \in H_n \land \mu(H_n) < \infty$
	- (Extension Theorem):
		- (Existence) $\mu: \mathcal{R} \rightarrow [0, \infty]$ a prem., it def. a meas. $\mu^*$ on $\sigma(\mathcal{R})$.
		- (Maximality of  $\mu^*|_\mathcal{R}$) for any meas. $\nu$ s.t. $\nu|_{\mathcal{R}} = \mu$, $\nu \le \mu^*|_\mathcal{R}$
		- (Weak Uniq.) $\mu: \mathcal{R} \rightarrow [0, \infty]$ $\sigma$-fin. prem., then there is a uniq. ext to a meas. $\sigma(\mathcal{R})$
			- (PE) $\lambda^d := (\lambda^d_{\mathcal{F}^d})^*$
- **Approximation of Subsets**
	- $M$ is $\mu^*$-meas. $\Leftrightarrow \mu^*(\partial M) = 0 \Leftrightarrow \mu^*(I) = \mu^*(A)$
		- $I:= M - \partial M$
		- $A:= \bigcap^\infty_{n = 1} A_{\frac{1}{n}} \in \sigma(\mathcal{R})$, for $\forall_{\epsilon > 0} \exists_{A_\epsilon \in \sigma(\mathcal{R})} (M \subset A_\epsilon \land \mu^*(A_\epsilon) < \mu^*(M) + \epsilon$
	- $\mu$ is $\sigma$-fin. $\Rightarrow \mathcal{A}^* \subseteq \{\alpha : \alpha = \beta_1 \cup ... \cup \beta_n \cup \gamma_1 \cup ... \cup \gamma_m \land \forall_{i \in [1, max(n, m)]}\beta_i \in \sigma(\mathcal{R}) \land \mu^*(\gamma_i) = 0\}$.
	- $\mu$ is compl. if all $\mu$-nullsets are in $\mathcal{A}$.
		- $\mathcal{N}:= \{N \subseteq X : \exists_{N_\nu \in \mathcal{A}} N \subseteq N_\nu \land \nu(N_\nu) = 0\}$
	- $\tilde{\mathcal{A}} := \{A \cup N: A \in \mathcal{A} \land N \in \mathcal{N}\} = \{\tilde{A} \subset X : \exists_{A' \in \mathcal{A}} \tilde{A} \Delta A' \in \mathcal{N}\} \subseteq \mathcal{A}$
		- $\tilde{\mathcal{A}}$ is a $\sigma$-al. and ex a uniq. ext $\tilde{\mu}$.
- **More on the Measurable Category**
	- **Pushforward** ([Wiki](https://en.wikipedia.org/wiki/Pushforward_measure)): for $f: X_1 \rightarrow X_2$ meas., $(X_1, \mathcal{A}_1)$, $(X_2, \mathcal{A}_2)$ meas. sp. and $\mu: \mathcal{A}_1 \rightarrow [0, \infty]$ then the pushf. is the meas $f_*(\mu): \mathcal{A}_2 \rightarrow [0, \infty], A_2 \mapsto \mu(f^{-1}(A_2))$.
- **Product Measure**
	- for $(X_i, \mathcal{A}_i, \mu_i)_{i \in [1, n]}$, recall $\mathcal{A}_1 \otimes ... \otimes \mathcal{A}_n \subseteq \mathcal{A}_1 \boxtimes ... \boxtimes \mathcal{A}_1 \subseteq \mathcal{A}_1 * ... * \mathcal{A}_n \subseteq Z(\mathcal{A}_1, ..., \mathcal{A}_n)$.
		- $\mathcal{A}_1 \otimes ... \otimes \mathcal{A}_n$ is the $\sigma$-al., the other are equivalent generators.
	- def. for $(X_i, \mathcal{A}_i, \mu_i)_{i \in [1, n]}$ $\sigma$-fin. then $\mu_1 \otimes ... \otimes \mu_n$ is the product measure and $(X \times ... \times X, \mathcal{A}_1 \otimes ... \otimes \mathcal{A}_n, \mu_1 \otimes ... \otimes \mu_n)$
##### I.3.4 Lebesgue Measure
- **Topological Approximation of Measurable Sets**
	- XX	
- **Invariances and Behave under Affine Functions**
	- for $\phi: \mathbb{R}^d \rightarrow \mathbb{R}^d$ aff $\phi^*(\lambda^d) = |\frac{1}{det(A)}|\cdot \lambda^d$ 

### II. Integration Theory
#### II.1 Integration & Numeral Functions
- a num.f, is $f: X \rightarrow \overline{\mathbb{R}}$ for $X$ a set s.t. $(X, \mathcal{A})$ meas.sp. and $\overline{\mathbb{R}}:= \{- \infty, \infty\} \cup \mathbb{R}$.
	- $\overline{\mathcal{B}} := \mathcal{B}(\overline{\mathbb{R}})$ is a $\sigma$-al. generated by:
		- $\{[-\infty, a) : a \in \mathbb{R}\}$, also for $(-\infty, a],[- \infty, a]$ 
	- $f: X \rightarrow \overline{\mathbb{R}}$ num is meas. $\Leftrightarrow \forall_{a \in \mathbb{R}}\{f \le a\}$
		- $\{f \le a\} := f^{-1}([-\infty, a]) \in \mathcal{A}$
		- $\mathcal{M}_\overline{\mathbb{R}}(X, \mathcal{A})$ are the meas.num.f. on $(X, \mathcal{A})$
			- closed under $sup$, $limsup$.
		- $\mathcal{M}_\mathbb{R}(X, \mathcal{A})$ are the meas.num.f. on $(X, \mathcal{A})$ s.t. $im(f) = \mathbb{R}$
		- $\mathcal{M}_{[0, \infty]}(X, \mathcal{A})$ are the meas.num.f. on $(X, \mathcal{A})$ s.t. $im(f) =[0, \infty]$
- **Approximation trough Step Funcitons**
	- for $f$ step.f. $f$ meas. $\Leftrightarrow \forall_{i \in I} c_i$ meas. i.e. each level is meas.
		- $\Rightarrow \mathcal{T}_\mathbb{R} = \mathcal{T}_{\mathbb{R}}(X, \mathcal{A}):=$ meas.step.f. s.t. $im(f) = \mathbb{R}$
		- $\Rightarrow \mathcal{T}_{[0, \infty]} = \mathcal{T}_{[0, \infty]}(X, \mathcal{A}):=$ meas.step.f. s.t. $im(f) = {[0, \infty]}$
	- any $f \in \mathcal{M}_{[0, \infty]}$ is a monotone limit of $t_n \subseteq \mathcal{T}_{[0, \infty]}$: $t_n \nearrow f$
- **Regions below Graphs**
	- for $f: X \rightarrow \mathbb{R}$, $f \in \mathcal{M}_\overline{\mathbb{R}} \Leftrightarrow \{(x, y) \in X \times \mathbb{R}: y \le f(x)\} \in \mathcal{A} \otimes \mathcal{B}^1$ (prod.$\sigma$-al. of $X \times \mathbb{R}$)
	- $f_1, f_2 \in \mathcal{M}_{\overline{\mathbb{R}}} \Rightarrow (f_1, f_2)^{-1}(A_1 \times A_2) := f_1^{-1}(A_1) \cap f_2^{-1}(A_2) \in \mathcal{A}$
		- $f_1 + f_2$ (pointwise) is uniq. and meas. (addition)
		- ==Q== (moltiplication)
#### II.2 Lebesgue Integral
- $f: X \rightarrow \overline{\mathbb{R}}$, prod.meas. is $\mu \otimes \beta^1 = (\mu \boxtimes \mathcal{B}^1)^*|_{\mathcal{A} \otimes \mathcal{B}^1}$
##### II.2.1 Integral for Non-negative Functions
- the Integral $I: \mathcal{M}_{[0, \infty]}(X, \mathcal{A}) \rightarrow [0, \infty], f \mapsto \int_X f d \mu := (\mu \otimes \beta^1)(\{(x, y) \in X \times \mathbb{R}: 0 < y < f(x)\})$
	- $f \le g \Rightarrow \int_X f d\mu \le \int_X g d \mu$ (monotony of $\mu \otimes \beta^1$)
	- $f_n \nearrow f \in \mathcal{M}_{[0, \infty]}(X, \mathcal{A}) \Rightarrow \int_X f_n d \mu \nearrow \int_X f d \mu$ (monotone convergence, B. Levi)
- for $(f_n)_{n \in \mathbb{N}} \subseteq M_{[0, \infty]}(X, \mathcal{A})$, then $\int \lim_{n \rightarrow \infty}\inf f_n d\mu \le \lim_{n \rightarrow \infty} \inf \int_{X}f_n d\mu$ (Fatou's lemma)
- **Linearity & Homogenity**
	- $\int_X \chi_A d \mu = \mu(A)$
	- $\int_X t d \mu = \sum_{i = 1}^n \mu(A_i)a_i$ for $t = \sum^n_{i = 1} a_i \chi_{A_i}$, $\forall_{i \in [1, n]}A_i \in \mathcal{A}$, also if $A_i$ are not disj.
	- any $f_+, f_- \in \mathcal{M}_{[0, \infty]}(X, \mathcal{A})$ can be approximated by some $t_{+,n}, t_{-,n}$.
	- $I$ has monotony, is additive and pos. homogene.
##### II.2.2 Integral on Measurable Functions
- for $f \in \mathcal{M}_\overline{\mathbb{R}}(X, \mathcal{A})$, is $\mu$-int. $\Leftrightarrow\int_X |f| d \mu < \infty \Leftrightarrow \int_x f_\pm d \mu < \infty$
	- $|\int_X f d \mu| \le \int_X |f| d \mu$
- $f=g$ alm.ever. if $\mu(\{x: f(x) \not = g(x)\}) = 0$
	- $f = g$ alm. ever. $\Rightarrow \int_X f d \mu = \int_X g d \mu$
	- $f \in \mathcal{M}_\overline{\mathbb{R}}(X, \mathcal{A})$ is $\mu$-int. in $A$ ($\in \mathcal{A}$) if $\chi_A \cdot f$ is $\mu$-int.
	- $\mathcal{L}_\mathbb{R}^1 \subsetneq \mathcal{L}_{\overline{\mathbb{R}}}^1$ is te VS of meas. func.
##### II.2.3 Convergence Theorems
##### II.2.4 Integration over Products
##### II.2.5 Transformation of Measures and Integrals
### III. Manifolds, Differential Forms and Stokes' Theorem
#### III.1 Differentiable Manifolds
#### III.2 Manifolds with Boundaries
- $M \subseteq \Omega$ man. for $\Omega$ op., then $M$ has $\mathcal{C}^k$-bound. $\Leftrightarrow$ $\forall_{p \in \partial \Omega} \exists_{k \in map(U, k)} K(\Omega \cap U) = H^m \cap k(U)$ ==Q== 
	- Ex. ...

## Verschiedenes
- **Dichte** (B. 10): for $f \in \mathcal{M}_{[0, \infty]}(X, \mathcal{A})$, then $f\mu: \mathcal{A} \rightarrow  [0, \infty], A \mapsto \int_A f d \mu$.
-
	- ([Wiki](https://en.wikipedia.org/wiki/Pushforward_measure)) if $X_1 = f^{-1}(X_2)$, then $\int_{X_2} g d(f_*\mu) = \int_{X_1} g \circ f d\mu$.
	- 