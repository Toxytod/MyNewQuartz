I'm following this course by Vincent Bagayoko on #Model_Theory at the #UniKonstanz during the #2nd_Semester. Here I'll collect some essential notes; the file he gave us ([Script Model Th. (Notability)](https://notability.com/n/0JMxdb9ad54cXEEwL29f~z)) contains most of the material. There will still be a place for some notes in class in case I'll take them here instead of following the script (since he's not accurately following the script). Exercises are to find on [page](http://www.math.uni-konstanz.de/~bagayoko/Model_theory_2023.html).
Course passed with an 2.7, I'm fine with this mark considering that I was the only BSc.
# Lectures & Homeworks
## Sheet 1
The sheet is the following: [[MT_Sheet_1.pdf]]
#### Ex. 1
Consider $M$ to be a non-empty set and define $\mathcal{M}:= \langle M; (R_i^\mathcal{M})_{i\in I}; (f_j^\mathcal{M})_{j\in J};(c_k^\mathcal{M})_{k \in K} \rangle$, by definition on p. 37 this is an $\mathcal{L}$-*structure*.
**Q:** Is there anything at all that I am supposed to show here? The definition requires nothing but a non-empty set so I suppose I just had to write it in the $\langle$ brackets $\rangle$.
**corrections**: Nulla di sorprendente, pero pare si dovesse fare un qualcosa come porre tutto uguale a una costante per dare i valori ai simboli, stesso casino non ben compreso di avere cose sottolineate e normali, dove quelli sottolineati dovrebbero essere l'interpretazione

#### Ex. 2
a) Consider $\phi_a:=\forall_{v_0} \exists_{v_1} \lnot(v_0 = v_1)$ as a *sentential form* and the *truth assignment* function $\mathcal{H}$ of the *sentential variables* in $\phi_a$, namely $v_0, v_1$, then if $\mathcal{H}(v_0)=F$ then there is a $v_1$ s.t. $\mathcal{H}(v_1)=T$ and if $\mathcal{H}(v_0) = T$ then there is a $v_1$ s.t. $\mathcal{H}(v_1)=F$. 
**Q:** I found the definition of tautology on the script at page 15, 1.3.0.4, and it is the one I'm typically used to. Though here where quantifiers come into play, I'm unsure if the following statement would hold: it might be that the set of variables $V=\{v_0\}$ and therefore in this case $\phi_a$ doesn't hold; or similarly, $\forall_{v_0 \in V}\mathcal{H}(v_0) = F$. If such an argument holds, then the $\phi_a$ is not a tautology.
**A:** ...
**corrections**: A tautology is a formula $\phi$ such that $\emptyset \models \phi$, i.e. any model $\mathcal{M}$ of $\phi$ (i.e. \mathcal{L}-*structure*) satisfies $\phi$. Avevo quindi ragione nella mia domanda perché basta prendere un modello che abbia il set di base con un elemento solo e quindi non è una tautologia.
Pero cazzo devi ricordarti che le variabili prendono i valori nel set di base del modello, quindi non solo vero o falso come dici che la funzione $\mathcal{H}$ fa. Perché in realtà $$\mathcal{H}: Vbl \rightarrow M$$unica modifica da fare ma un bel po' **improtante**.

b) Consider $\phi_b:=(v_0, v_0)$ as a *sentential form*. Then, since there are no quantifiers, I might proceed with the usual truth tables. Here it's also enough to show that $\mathcal{H}(v_0) = \mathcal{H}(v_0)$ and therefore $\phi_b$ must be a tautology.

c) Consider $\phi_c := \exists_{v_0} \forall_{v_1} \exists_{v_2}(f_i(v_0,v_1)=f_i(v_0,v_2))$ as a *sentential form* and assume $\alpha_i = 2$. Since $v_1$ runs over all elements in $V$ and $v_2$ gets picked after, I can always pick $v_2 = v_1$ and therefore: $\exists_{v_0} \forall_{v_1} \exists_{v_2}(f_i(v_0,v_1)=f_i(v_0,v_2)) \Leftrightarrow \exists_{v_0} \forall_{v_1}(f_i(v_0,v_1)=f_i(v_0,v_1))$ which obviously holds, therefore $\phi_c$ is a tautology. It should look similar to $\forall_{v_0} \exists_{v_1} (v_0 = v_1)$ which, for the same reason, should be a tautology too.
**corrections**: 
- [ ] era da risolvere anche con le h(simbolo sopra e sombolo sotto) che trovi nello script. Capisci bene quelle

d) Consider $\phi_d := \exists_{v_0} R_j(v_0, c)$ as a *sentential form* and assume $\beta_j=2$. I claim it to be not a tautology and therefore should just define a relation $R_j'$ s.t. $\mathcal{H}(\phi_d)=F$. Define $R_j'$ such that: $\forall_{v_0}\forall_{v_1}(R_j'(v_0,v_1) \leftrightarrow(v_1 = c_1))$ for $\lnot(c_1=c)$. In the case $R_j=R_j'$ obviously $\mathcal{H}(\phi_d)=F$ and therefore $\phi_d$ is not a tautology.
**corrections**: tutto a posto ma sempre lo stesso punto, H va a M, non a caso in (T,F)

### Ex. 3
**corrections**: Is there a first order theory $T$ in $\rangle 1, \cdot, \cdot^{-1} \langle$ whose models are exactly tonsion free groups. Guarda cnote a penna.

### Ex. 4
Let $T$ be a first-order theory over $\mathcal{L}$, namely a set of *sentences* (namely formulae without free variables) in $\mathcal{L}$. Now assume that for each $n \in \mathbb{N}$, there is a model $\mathcal{M}_T$ of $T$ of cartinality $\ge n$. I suppose the cardinality of a model $\mathcal{M}$ to be the cardinality of its underlying set, namely $|M|$; similarly I suppose an infinite model to be a model of cardinality $\ge \aleph_0$. By our assumption there is a sequence $((\mathcal{M}_T)_n)_{n\in \mathbb{N}}$ and $\forall_{n \in \mathbb{N}}|(M_T)_n| \ge n \Rightarrow \exists_{M_T} |M_T| \ge \aleph_0$; therefore $T$ must have an infinite model. 
The idea I wrote above is completely wrong
**correction**:
we need the *completeness theorem*. Given proofs $\mathcal{P}_+, \mathcal{P}_-$ of $\phi$ and $\lnot \phi$,
the sets $A_1$ and $A_2$ of axioms of $T$ used in $\mathcal{P}_1$ and $\mathcal{P}_2$ are finite. But $A_1 \cup A_2 \subseteq T$ also proves $\phi$ and $\lnot \phi$, so it is inconsistent.
**Solution**:

## 3rd Lecture
#### End of III)
##### Some Simple Defs
**Def.** A theory $T$ of a language $\mathcal{L}$ if it has a model $\mathcal{M}$, i.e. there is an $\mathcal{L}-*structure* $\mathcal{M}$ s.t. $\mathcal{M} \models \phi$ for all $\phi \in T$; $T$ is said *inconsistent* otherwise.
$T$ proves a sentence $\phi$ if there is a finite sequence $(\phi_n,R_n)_{n\in l}$ where $\phi_0 \in T$ , and $\phi=\phi_l$ and $R_n$ is a logical rule stating that if $\phi_{n+1}$ by $R_n$.
*Def.* A theory $T$ is **consistent** if for no sentence $\phi$, $T$ proves $\phi$ and $\lnot \phi$.
*Def.* A first order Theory $T$ is said **complete** if for any sentence $\phi$ in $\mathcal{L}$, we have $T \models \phi$ or $T\models \lnot \phi$, and $T$ is consistent.
If $\mathcal{M}$ is an $\mathcal{L}$-*structure*, then by virtue of the *law of excluded middle*, its elementary theory, namely: $Th(\mathcal{M})= \{\phi \in \mathcal{L}: \phi \textit{ is a sentence and }\mathcal{M}\models \phi\}$, is complete. To make it more clear consider that if $T$ is ocmplete, and $\mathcal{M}\models T$, then $T=Th(\mathcal{M})$. Indeed, for $\phi \in Th(\mathcal{M})$, and $\mathcal{M} \models T$, by completeness, we have $T \models \phi$ or $T\models \lnot \phi$, but the latter option cannot hold by definition of the satisfaction of a formula by a theory $\mathcal{L}$-*structure*, hence $T\models \phi$. Remember that $T$ staisfies a formula if every model of $T$ statisfies the formula. 
*Def.* the set of **Theorems** is defined as: $Th(T):= \{\phi \in \mathcal{L}: \phi \textit{ is a sentence and } T \models \phi\}$.
##### Examples
Ex. The *theory of groups* is not complete: indeed it satifies neither $\forall_{v_0}\forall_{v_1}(v_0 \cdot v_1 = v_1 \cdot v_0$) nor its negation. In fact there are abelian and non abelian groups and these are two different models of the same [[Group Theory]].
Remark: Given a theory $T$ and a sentence $\phi$ the theory $T \cup \{\phi\}$ is consitent iff. $T$ is consistent, and $T$ does not satisfy $\lnot \phi$. e.g. you can take a model of $ZFC \cup CH$ and it will be consistent, you can do similarly with $\lnot CH$ which is a way to show that $CH$ is independent.
##### Compactness Theorem
**Theorem**: A first-order theory $T$ is consistent iff. every finite subset of $T$ is consistent.
*Proof.* (informal) by completeness theorem we know thath $T$ is consistent iff. $T$ doesn't prove contradiction (meaning $T \models \phi \land \lnot \phi$). Therefore $T$ is not consistent iff. threre is a formula s.t. both $\phi$ and $\lnot \phi$ are satisfacted by $T$.
#### IV) Logical Consenquence
**Def.** We say that true $\mathcal{L}$-formulae $\phi, \psi$ are **equivalent modulo a theory $T$** if $T \models (\phi \leftrightarrow \psi)$.
We say that $\phi$ and $\psi$ are logically equivalent if they are equivalent modulo the empty theory, namely $\emptyset \models(\phi \leftrightarrow \psi)$. We say that $\phi$ is a **tautology** if $\emptyset \models \phi$.
##### Examples
The following formulae are equivalent modulo the theory of groups: $v_0 \cdot v_1 = 1$ and $v_1 \cdot v_0 = 1$. The following are tautologies:
- $(v_0 = v_0)$
- $\exists_{v_0}(v_0 = v_0)$
- $(v_0 = v_1) \rightarrow (R(v_0, v_2) \leftrightarrow R(v_1,v_2))$
##### Lemma
Now let us define, by induction, a subset $\mathcal{L}^+ \subseteq \mathcal{L}$ as follows:
- all atomic fomrulas are in $\mathcal{L}^+$
- If $\phi, \psi \in \mathcal{L}^+$ then $(\phi \land \psi)\in \mathcal{L}^+$, $\lnot \phi \in \mathcal{L}^+$ and $\exists_{v_k} \phi \in \mathcal{L}^+$.
And $\mathcal{L}^+$ is the smallest set that satisfies this.
**Lemma:** Any formula $\phi \in \mathcal{L}$ is logically equivalent to a $\psi \in \mathcal{L}^+$.
*Proof.* By induction on the *rank* $n$ of $\phi \in \mathcal{L}$. If $\phi$ is atomic (i.e. $n=0$), then $\phi \in \mathcal{L}^+$ so take $\psi = \phi$. Assume that any $\phi \in \mathcal{L}$ of rank $<n$ is equivalent to an element of $\mathcal{L}^+$, and note the following: If $\phi = (\phi_1 \land \phi_2)$, then  given $\psi_1\, \psi_2 \in \mathcal{L}^+$, with $\emptyset \models (\psi_1 \leftrightarrow \phi_1)$ and $\emptyset \models (\psi_2 \leftrightarrow \phi_2)$, we have $\emptyset \models \phi \leftrightarrow (\psi_1\ \land \psi_2)$, the latter of which is in $\mathcal{L}^+$. If $\phi = (\phi_1 \land \phi_2)$ where $\psi_1$, $\psi_2 \in \mathcal{L}^+$ are as above with respect to $\psi_1$, $\psi_2$, then $\emptyset \models \phi \leftrightarrow \lnot(\lnot \psi_1 \land \lnot\psi_2)$ which is an elemnt of $\mathcal{L}^+$. The cases of negation and sententical quantification are similar. Finally, if $\phi = \forall_{v_k} \phi_1$, $k \in \mathbb{N}$, then given $\psi_1 \in \mathcal{L}^+$and $\emptyset \models (\phi \leftrightarrow \psi)$, we have $\emptyset \models \psi \leftrightarrow \lnot \exists_{v_k} (\lnot \psi_1)$.

#### V) Filters and Ultrafilters
##### Def. of Filter
We define an infinite set $I$.
*Def.* A **filter** on $I$ is a set $\mathcal{F}$, such that $\mathcal{F} \subset \mathcal{P}(I)$, non-empty with:
1. $\emptyset \not \in \mathcal{F}$
2. $\forall_{A,B \in \mathcal{F}} A \cap B \in \mathcal{F}$
3. $\forall_{A,B \subseteq I}(A \in F \land A \subseteq B) \Rightarrow B \in \mathcal{F}$
Conditions 2. and 3. can be summerised in: $M \cap N \in \mathcal{F} \leftrightarrow M, N \in \mathcal{F}$.
*Def.* For a fixed $K \subseteq I$, a **principal filter** generated by $K$ is the family of all supersets.
- [ ] Superset
- [ ] Family
Excurus: Try to think at filters as ideals of the ring $(\mathcal{P}(I), \cap, \subseteq)$, closed under $\cap$ and checking all elements of $\mathcal{P}(I)$ for $\subseteq$.
###### Examples
*Def.* $A$ is said **cofinite** iff. $\bar{A}$ is finite. Remember $\bar{A} := I \setminus A$ for a set $I$ s.t. $A \subset I$, $\bar{A}$ is called the **complement**.
- Given $i \in I$, we have a filter $\mathcal{F}_i = \{A\subseteq I: i \in A\}$.
- **Féchet Filter**, is the filter of the cofinite subsets of $I$: $\{A \subseteq I: I \setminus A \textit{ is finite}\}$.
- If $(I, <)$ is totally ordered, then the set supersets of non-empty final segments of $I$ is a filter. A final segment is a subset $A \subseteq B$ with $\forall_{i,j \in I}(i \in A \land j \ge i) \Rightarrow j\in A$
Given a subset $\mathcal{A} \subseteq T(I)$, we write: $FI(\mathcal{A}) = \{A_1 \cap ... \cap A_n n >0, A_1, ..., A_n \in \mathcal{A}\}$. and we say that $\mathcal{A}$ has the finite intersection property if $\emptyset \not \in FI(\mathcal{A})$.
- [ ] Understand filters on ordered sets
- [ ] Understand what the Féschet Filter is
- [ ] Understand the finite intersection property
- [ ] Summerise in these notes
##### Two Lemmas
**Lemma 1.** If $\mathcal{A} \subset \mathcal{T}(I)$ has the finite intersection property, then there is a filter $\mathcal{F}$ on $I$ with $\mathcal{A} \subseteq \mathcal{F}$
*Proof.* Define $\mathcal{F} := \{C\subseteq I : \exists_{B \in FI(\mathcal{A})} B\subseteq C\} \subseteq \mathcal{A}$.
*Claim.* $\mathcal{F}$ is a filter. I know $\emptyset \not \in \mathcal{F}$ by the finite interesection property, so the first point is done. If $c_1 c_2 \in \mathcal{F}$, $B_1, B_2 \in FI(\mathcal)$ with $B_1 \subseteq C_1$ and $B_2 \subseteq C_2$ then $B_1 \cap B_2 \in FI(\mathcal{A})$ is containted in $C_1 \cap C_2$, so $C_1 \cap C_2 \in \mathcal{F}$. Finally, if $C \in \mathcal{F}$, $B \in FI(\mathcal{A})$ such that $V \subseteq C$, and $C' \subseteq I$ is such that $C \subseteq C'$, then $B \subseteq C$ is $C' \in \mathcal{F}$.
**Lemma 2.** Let $\mathcal{F}$ be a filter and let $A \subseteq I$ with $\bar{A} \not \in \mathcal{F}$. Then $\mathcal{F}_A: \mathcal{F} \cup \{A \cap B \land B \subseteq I\}$ is a filter containing $\mathcal{F} \cup \{A\}$.
*Corollary:* $\mathcal{F} \cup \{A\}$ is contained is a finlter on $I$.
*Proof.* Assume for contradiction that $\emptyset \in \mathcal{F}_A$, so $\emptyset = A \cap B$ for some $B$. This means that  $B \subseteq \bar{A}$, but then $\bar{A} \in \mathcal{F}$ contradiction so $\emptyset \not \in \mathcal{F}_A$.
Given $C_1, C_2 \in \mathcal{A}$, let's examine the cases:
(i) $C_1, C_2 \in \mathcal{F}$, then $C_1 \cap C_2 \in \mathcal{F} \subseteq \mathcal{F}_A$
(ii) $C_1 \in \mathcal{F}, C_2 = A \cap B_2$, $B_2 \in \mathcal{F}$
(iii) $C_2 \in \mathcal{F}$
(iv) $C_1 \mathcal{A} B_1$, $C_2 = A \cap B$,   $B_0, B_2 \in \mathcal{F}$ then
$C_1 \cap C_2 = A \cap (B_1 \cap (B_2 \in \mathcal{F}_A$))
- [ ] Try to understand what sould the case iv be
##### Ultrafilters and Lemma
**Def.** An ultrafilter on $I$ is a filter $\mathcal{U}$ on $I$ such that for all $A \subseteq I$, we have either $A \in \mathcal{U}$ or $\bar{A} \in \mathcal{U}$; or similarly  $\mathcal{U}$ is an ultrafilter if the follwoing holds $\forall_{A \in \mathcal{P}(I)}A \in \mathcal{U} \leftrightarrow \bar{A} \not \in \mathcal{U}$.
**Ultrafilter Lemma** For $S$ a non-empty set and $\mathcal{A} \subseteq \mathcal{P}(S)$, then there is an ultrafilter $\mathcal{U} on $S$ s.t. $\mathcal{A} \subseteq \mathcal{U}$.
- [ ] Copy and understand the proof from [Proofwiki](https://proofwiki.org/wiki/Ultrafilter_Lemma)
(versione un po' più debole di axiom of choice ma cmq non in ZF)
*Proof.* Consider the set $W$ of filters on $I$ containing $\mathcal{F}$, ordere by inclusion. let  C \subseteq U be a non empty totally ordered set of (W, \subseteq) and set U = unione di  C \subseteq mathcal{F}.  For more see [[Model Theory (Lecture)#Lectures & Homeworks#Ultrafilters]].
#### Theory form Exercises Corrections
##### [[Torsion Groups]]
*Torsion Groups* are defined as: $\forall_{g \in G} \exists_{n \in \mathbb{N}}(n>0 \land g^n =1)$ and, on the other hand *Torsion Free Groups* are defined as: $\forall_{g \in G} \forall_{n \in \mathbb{N}}(n>0 \rightarrow ( g^n=1 \rightarrow g=1))$. Now the interesting question is:
$$\text{Is there a first-order theory $T_{tor-free}$ in $\langle 1, \cdot, \cdot^{-1} \rangle$?}$$
Define $T_{gr}$ as the theory of groups. Let's begin by the Torsion Free groups: looking at $\forall_{g \in G} \forall_{n \in \mathbb{N}}(n>0 \rightarrow ( g^n=1 \rightarrow g=1))$, it very looks like an axiom, though we have to remember that in our model we don't have any natural numbers yet. No problem, you can solve this by creating a sequence of formulae, $\phi_n:= \forall_{v_0} ( v_0 = 1 \land \lnot(v_0^n =1))$. Notice, again we have a similar problem as before, we can't write $v_0^n$ since we have not defined the power to a natural number yet. No problem again, define the same sequence as: $\phi_n:= \forall_{v_0} ( v_0 = 1 \land \lnot(v_0 \cdot v_0 \cdot v_0 \cdot ... \cdot v_0 =1))$ wherw the multiplication repeats $n$ times. This is an axiom schema that entails as many axioms as natural numbers, we call it an *infinite theory*. So we define $T_{tor-free}:= T_{gr} \cup \{\phi_n: n>0\}$ as model of $(G, \cdot, 1)$.
Next, what about the Torsion Groups? We might try with $\psi_n :=v_0, \cdot ... \cdot v_0 = 1$ with the multiplication repeating $n$ times. Tough in order to axiomatise this, we'd need $\forall_{v_0}(\bigvee\limits_{n \in \mathbb{N}} \psi_n)$, but the  infinite disjunction is not a simbele in the first-order logic, and therefore it can't be done yet.
Let's start a second proof then and assume for contradiction that $T_{tor}$ exists. Now let's expand the language with $\tau$, a constant. Now consider the theory in $\langle 1, \cdot,\cdot^{-1}, \tau \rangle$ given as follows $T=T_{tor} \cup \{\lnot (t \cdot t \cdot t \cdot ... \cdot t =1): n\in \mathbb{N}\}$ and we claim this as being *consistent*. Now use the *compactness theorem* and we can say that if a fini amout of elements, say $T_0 \subseteq T$ is a finite subset, then there is an $h \in \mathbb{N}$ s.t. $T_0 \subseteq T_{tor} \cup \{\lnot (t \cdot t \cdot t \cdot ... \cdot t =1): h < n\}$. Now, let $p$ be a prime number with $p \ge n$ then: $\mathbb{Z}/p\mathbb{Z}$ is a torsion group and the following is a model of $T_0$, $(\mathbb{Z}/p\mathbb{Z}, +, 0, \bar{1})$ . Then $T_0$ is consistent and *by compactness* $T$ is consistent. But given a model $\mathcal{M} = (G, 1, \cdot, -1, \tau)$ of $T$, the element $\tau \in G$ doesn't have a torsion. Therefore $(G, 1, \cdot, \cdot^{-1}) \not \models T_{tor}$. Then we get the desidered contradiction, *QED*.
**excursus**: Theories like torsion groups can be formalised by using *[[Second-Order Logic]]*; though one typically doesn't want to do so, since there *compactness theorem* doesn't hold. Let's start with a second example on such theories, consider the following ordered sets, which of them are expressible in first-order thoeries?
1. Totally ordered sets
2. Well-ordered sets
3. Dense totally ordered sets
4. Dedeking complete totally ordered sets
The first is simple, you just need three axioms, you need it to be anti-reflexive, transitive and total, just write down the axioms with the usual variables and it works simply. We can do similarly for dense totally ordered sets. Well ordered sets, though, need more work, and can be expressed in second-order logic only with the following axiom: $$ \forall_X((\exists_{v_0}v_0 \in X) \rightarrow \exists_{v_1} (v_1 \in X \land \forall_{v_2}(v_2 \in X \rightarrow ((v_1 = v_2) \lor (v_1 < v_2))))$$Similarly, Dedekind complete totally ordered sets can be formalised in second order logic.
## 4th Lecture
### Ultrafilters and Lemmas
**Lemma**: A filter \mathcal{F} on $I$ following are equivalent
1. \mathcal{F} is an ultrafilter ()
2. $\forall_{A,C \subseteq I} A \cup B \in \mathcal{F} \Rightarrow A \in \mathcal{F}$ or $B \in \mathcal{F}$ 
3. $\mathcal{F}$ is minimal among filters on $I$, i.e. it is not poperly contained in a filter on $I$
*Proof.* Assume that $\mathcal{F}$ is an ultrafilter, and let $A, B \subseteq I$ with $A \cup B \in \mathcal{F}$. Then $A \not \in \mathcal{F}$ , then $\bar{A} \in \mathcal{F}$. Let $\bar{A} \cap (A \cup B)=(\bar{A} \cap A) \cup (\bar{A}\cap B)$ is in $\mathcal{F}$. So $\bar{A} \cup B \subseteq B$ is in $\mathcal{F}$. So $1. \Rightarrow 2.$
Now assume that $\mathcal{F}$  satisfies 2., and let $\mathcal{F} \subseteq \mathcal{U}$ be a filter. Let $A \in \mathcal{U}$. We have $A \cup \bar{A} \in \mathcal{F}$ indeed $\mathcal{F}$ is non-empty by asssumption and given $B \in \mathcal{F}$, $A \cup \bar{A} \supseteq B$. So $A \in \mathcal{F}$ or $\bar{A} \in \mathcal{F}$, but the later option would imply that $\bar{A} \in \mathcal{U}$, so $A \cap \bar{A} = \emptyset \in \mathcal{U}$. Thus $A \in \mathcal{F}$. So $\mathcal{F} = \mathcal{U}$, hence $\mathcal{F}$ is minimal, so $2. \Rightarrow 3.$ Assume that $\mathcal{F}$ is minimal among ultrafilters on $I$. In particular for $A \subseteq I$ with $\bar{A} \not \in \mathcal{F}$ given a filter $\mathcal{F}_A$  on conianing $\mathcal{F} \cup \{A\}$, we have $\mathcal{F} = \mathcal{F}_A$, so $A \in \mathcal{F}$ this $\mathcal{F}$ is an ultrafilter. $QED.$
**Ex.** Given an $i \in I$, the filter $\mathcal{F}_i =\{A \subseteq I| i \in A\}$ is an ultrafilter on $I$, and we say that $\mathcal{F}_i$ is principal. An ultrafilter on $I$ is said free if it is not principal.
	**Lemma**: A filter on $I$ is **free** iff it contains the Féchet Filter $\{A \subseteq I | \bar{A} \text{ is finite }\}$.
*Proof.* Say $\mathcal{F}$ contains the Fréchet filter, then for any distinct $i, j \in I$, we have $\{\bar{i}\}$ we have $\mathcal{F}_i \not = \mathcal{F}_j$, so $\mathcal{F}$ is free. Now assume that $\mathcal{F}$ is free. Let $A \subseteq I$ be cofinite, i.e. $\bar{A}$ is finite and we write $\bar{A}= \{i_1,..., i_n\}$ for $n \in \mathbb{N}$ and $i_1, ..., i_n \in I$. We want to show that $A \in \mathcal{F}$. Assume for contradiction that $A \not \in \mathcal{F}$. So $\bar{A} \in \mathcal{F}$. By the second characterisation of ultrafilters, we have: $\bar{A}= \{i_i\} \cup ... \cup \{i_n\} \in \mathcal{F} \Rightarrow \exists_{k \in \{i_1, ..., i_n\}}$ with $\{i_k\} \in \mathcal{F}$ (by induction). But then $\mathcal{F}_{i_k} \subseteq \mathcal{F}$ since $\mathcal{F}$ is a filter. We conclude since $\mathcal{F}_{i_k}$ is minimal that $\mathcal{F}_{i_k} = \mathcal{F}$. We get then contradiction. $QED.$
Let $\mathcal{L} = \langle (f_k)_{k \in K}, (R_j)_{j \in J}, C \rangle$ be a first order language. Let $(\mathcal{M}_i)_{i \in I}$ be a family of $\mathcal{L}$-*structures* and write $\mathcal{M}_i =(M_i,  (f_k)_{k \in K}, (R_j)_{j \in J}, (\lambda_{i,c})_{c \in C})$. We will define an equivalence relation on the Cartesian product $\prod_{i \in I} M_i = \{g: I \rightarrow \bigcup_{i \in I} n_i: g(i) \in M_i \text{ for each } i \in I\}$. Let $\mathcal{U}$ be an ultrafilter on $I$. We say that $(m_i)_{i \in I}$ and $(m'_i)_{i \in I}$ in $\prod_{i \in I}M_i$ are *equivalent modulo* $\mathcal{U}$ and we write $(m_i)_{i \in I} =_\mathcal{U} (m_i')_{i \in I}$ if the set $\{i \in I | m_i = m_i'\}$ lies in $\mathcal{U}$.
	**Lemma**: This is an equivalence relation on $\prod_{i \in I} M_i$
*Proof.* Reflexivity: this is because $I \in \mathcal{U}$ (true for all filters). Simmetry: by symmetry of $=$. Transitivity: let $(m_i)_{i \in I} =_{\mathcal{U}} (m_i')_{i \in I}$ and $(m'_i)_{i \in I} =_{\mathcal{U}} (m_i'')_{i \in I}$. And let $A, B \in \mathcal{U}$ be witnesses, i.e. $\{i \in I: m_i = m_i'\}=A$ and $\{i \in I: m_i' = m_i''\}=B$. Then by transitivity of $=$ we have $m_i = m_i''$ for all $i \in A \cap B$, but $A \cap B \in \mathcal{F}$, since $(m_i)_{i \in I} =_{\mathcal{U}} (m_i'')_{i\in I}$. $QED.$
We write $\prod_{\mathcal{U}}$ with interpretation of symbols in the signature. We proceed as follows: For $k \in K$ and $m_1, ..., m_{\alpha k} \in \prod_{i \in I}M_i$, we define:$\underline{f_k}([m_1]_\mathcal{U},..., [m_{\alpha k}]_\mathcal{U}) := [(f_{i,k} (m_1(i),...,m_{\alpha k}(i))_{i \in I}]_\mathcal{U}.$ if $m_1', ..., m_{\alpha k}' are s.t. $([m_1']_\mathcal{U}, ..., [m_{\alpha k}'']_\mathcal{U})= ([m_1]_\mathcal{U}, ..., [m_{\alpha k}]_\mathcal{U})$, then for sets $A_1, ..., A_{\alpha k} \in \mathcal{U}$ witnessing each equivalence $m_1 =_\mathcal{U} m_1', ..., m_{\alpha k} =_\mathcal{U} m_{\alpha k}'$ we have that $A:= A_1 \cap ... \cap A_{\alpha k} \in \mathcal{U}$, and for each $i \in A$, $f_{i,k}(m_1(i), ..., m_{\alpha k}(i)) = f_{i,k}(m_1'(i), ..., m_{\alpha k}'(i))$ which means that $[(f_{i,k}(m_1(i), ..., m_{\alpha k}(i))_{i \in I}]_\mathcal{U} = f_{i, k}([m_1], ... [m_{\alpha k}])$.
- [ ] TODO da Notability

## Sheet 2
The sheet is [[MT_Sheet_2.pdf]], some definitions and theorems on [[ultraproducts-web-final.pdf]]
### Ex. 4
*Claim.* let $\mathcal{M}$ be an $\mathcal{L}$-*structure*, where $M$ is finite, then the natural embedding $\mathcal{M} \rightarrow \prod_\mathcal{U} \mathcal{M}$ is surjective.
*Proof.* Consider a $\mathcal{M}$ being an $\mathcal{L}$-*structure*, so $\mathcal{M}:= \langle M, (f_i)_{i \in I}, (R_j)_{j\in J}, (c_n)_{n \in N}\rangle$, and say $|M| < \aleph_0$. Let $\mathcal{U}$ be an ultrafilter on $\mathcal{M}$, and recall that a natural embedding is the mapping $d: \mathcal{M} \rightarrow \prod_\mathcal{U} \mathcal{M}$ s.t. $d(m)$ is the $\mathcal{U}$-equivalence class of the constant function with value $m$. Since the ultrapower is an ultraproduct with $\forall_{i \in I} \mathcal{M}_i = \mathcal{M}$, i.e. $\prod\mathcal{M} = \{ (m_i)_{i \in I} | \exists_{x \in I}\forall_{i \in I} m_x = m_i\}$, we can therefore notice that every element in $\prod \mathcal{M}$ is defined upon one element in $\mathcal{M}$ only by $d: m \mapsto (m_i)_{i \in I} \text{ s.t. } \forall_{i \in I}(m_i = m)$ and reducing the elements by considering the equivalence classes on $=_{\mathcal{U}}$ can't change surjectivity; thereofre the natural embedding $d: \mathcal{M} \rightarrow \prod_\mathcal{U} \mathcal{M}, m \mapsto f \text{, s.t. } f: \mathbb{N} \rightarrow \mathcal{M}, n \mapsto m$ is surjective.
**Correction**: def. of natural embedding is right, I should have added that we use the disjunctive property of ultrafilters (\forall_{A,B \subseteq X}(A \cup B \in \mathcal{U} \rightarrow A \in \mathcal{U} \land B \in \mathcal{U})). Though I don't know if it was much needed.

### Ex. 5
**a)** *Claim.* There exists a first-order thoery in $\mathcal{L}_1$ of graphs without loops.
*Proof.* Consider the given definition of a loop, namely that a loop is an element $e$ of $E$ in a graph $(V, E)$, s.t. $e= (v,v)$ for an element $v \in V$. Then the theory $T_{wl}$ must contain the following axiom $$\forall_{v \in V} \lnot(v \rightarrow v)$$This is a formula of $\mathcal{L}_1$. Similarly one could write this in $\mathcal{L}_\epsilon$ and it would be a theory $T_{wl}' := \{\forall_{v \in V} \lnot((v, v) \in E)\}$ if we consider $v \rightarrow w \Leftrightarrow (v, w) \in E$.
**Correction**: don't say $v \in V$, just state $\forall_x$ the possible domain is already nothgin but $V$.
**b)** *Claim.* There exists a first-order theory in $\mathcal{L}_1$ of connected graphs.
*Proof.* The theory $T_c$ must contain an axiom expressing:$$\forall_{v, v' \in V}(\exists_{(v_i)_{i \in [1,n]\subset \mathbb{N}}}(v_i \rightarrow v_{i+1}) \land (v_1, v_n)=(v, v'))$$This is not a theory of $\mathcal{L}_1$, since $\mathbb{N}$ is not a symbol of the language. I shall therefore instead consider $X$ to be a subset of $E$; I need $X$ to be a chain, therefore I can define the set of chains from $v$ ot $v'$ to be $$X(v, v'):= \{X \subseteq E| (\exists_{u_1 \in V} (v, u_1) \in E) \land (\exists_{u_2 \in V}(u_1, u_2) \in E) \land ... \land (\exists_{u_{n-1}\in V}(u_{n-1}, v') \in E)\}$$Since it is defined trough a *finite* conjunction (the given definition of connectivity also requires the chain to be finite) and $v \rightarrow w \Leftrightarrow (v, w) \in E$ still holds, then $X(v, v')$ is a set defined in $\mathcal{L}_1$. Therefore I can state that:$$T_c := \{\forall_{v \in V}\forall_{v' \in V}(\exists_X X \in X(v, v'))\}$$which is a first-order theory of connected graphs in $\mathcal{L}_1$.
**Correction**: Wrong, through compactness theorem we should prove that there is no first-order theory. Here is the proof: $\psi_n(v_1, v_2):= \lnot (\exists_{v_3},..., \exists_{v_{n+2}}(v_3 \rightarrow v_4)\land ...\land v_{n+1}\rightarrow v_{n+1} \land (v_3 = v1) \land (v_{n+2}=v_{2}))$. So $T' =T \cup \{\psi_n(v_1, v_2)| n\in \mathbb{N}\}$. Every finite subset $T_0 \subseteq T$ is consistent $n_0$ s.t. for $k \ge n_0$, $\psi_k(v_1, v_2) \not \in T_0$. Consider then for example the loop that has a way from $v_1$ to $v_2$ with infinite knots between and one straigh passage in the other way around. This graph is model of $T_0$. So the compactness theorem says that then $T'$ is consistent so let $\mathcal{M}$ be a model of $T'$, ad this gives us the graph $G=(V, E)$ and two vertices $x, y$. They mus tbe connected and must be not connected, $QED$ 
### Ex. 6
Thanks to surjectivity of the natural embedding proved in Ex. 4, I know that $\mathcal{R}_f$ consists only of constant sequences (or functions from $\mathbb{N}$) with values in $\mathbb{R}_f$. Though $\mathcal{R}_f$ is written with a different signature in which $F$, the only function with ariety 1, is interpreted as $f^*$, s.t. $f^*([u(x)]_\mathcal{U})= [u(f(x))]_\mathcal{U}$ for any function $u: X \rightarrow \mathbb{R}$. The natural embedding therefore is of the form: $d: \mathbb{R}_f \rightarrow \mathcal{R}_f, r \mapsto (r_i)_{i \in I}$, s.t. $\forall_{i \in I}r_i = r$ and every $f$ in $r$ gets interpreted as $f^*$ in $r_i$. Therefore every $f$ in $r$ gets interpreted as $[f \circ u]_\mathcal{U}$ in $r_i$.
**Remark**: remember that $[u]_\mathcal{U} + [v]_\mathcal{U} = [u + v]_{\mathcal{U}}$ and similarly $[u]_\mathcal{U} \cdot [v]_\mathcal{U} = [u \cdot v]_{\mathcal{U}}$.
**a)** *Claim.* I call $\epsilon$ an infinitesimal if $n\cdot max(\epsilon, -\epsilon) < 1$ for all $n \in \mathbb{N}$, then $\epsilon \in R_f$.
*Proof.* if we consider all elements of $\mathbb{R}_f$ which don't contain $f$, then we notice that those have, through the natural embedding, a simple (meaning that it is almost an identity, $x \mapsto f$ s.t. $f: n \mapsto x$) correspondent, therefore since there are infenitesimals in $\mathbb{R}$ there must be in $\mathcal{R}_f$ too.
**Correction**: We construct a funciton $u: X \rightarrow \mathbb{R}$ by induction on $\mathbb{N}$ as follows. Start with $m_0(x) =1$ for all $x \in X$. $\forall_{n \in \mathbb{N}} \forall_{n \in \mathcal{U}} n |\mathcal{M}_n(a)| < 1$ for all $a \in A_n$ $n |[( \mathcal{M}_n(x))]_\mathcal{U}| < 1$. Now let $n \in \mathbb{N}$ such that $\mathcal{M}_n$ is defined and satisfies what we just wrote and set $A_n \in \mathcal{U}$. We take an infinite subset $A_{n+1}$ of $A_n$ which lies in $\mathcal{U}$ and whose complement in $A_n$ is infinite. So let $B, C$ be infinite subsets of $A_n$ s.t. $A_n = B \cup (ma squadrata) C$ (using Ax. Choice). since $A_n \in \mathcal{U}$, we have $B \in \mathcal{U}$ or $C \in \mathcal{U}$, we take $A_{n+1}$ to  be thin set amery $B$ and $C$ with $A_{n+1} \in \mathcal{U}$. We define $u_{n+1}(a) = u_n(a) if a \not \in A_{n+1} and 1/(n+2) if a \in A_{n+1}$. WE now set $u(a):= u_n(a) for a large enoough $n$, so for each $n \in \mathbb{N}$, we have that $|u(a)| < 1/n$ for all $a \in A_{n}$ so $\{x \in X : n|u(x)| < 1\}$. E qua il tutor di Algebra gli fa il culo perche quel "large enough" non gli piace. Nemmeno lui lo ha fatto cmq, quindi 0 speranza. Sono a quello stadio di ignoranza cosi profonda che mi semrbava una cazzata.
**Correction** (of the correction): We claim that given a sequence $u \in \mathbb{R}^\mathbb{N}$ with $\lim_{n \rightarrow + \infty} u_n = 0$ we claim that $[u]_\mathcal{U}$ is infinitesimal. Indeed let $n \in \mathbb{N}$. For large enough $k \in \mathbb{N}$, we have $|u_k|<1/n$ so $\{i \in \mathbb{N}: n |n_i|<1\} \subseteq (invertito) [h, + \infty):$ cofinite. Since $[h, +\infty) \in \mathbcal{U}$, we say that $n|[u]_\mathcal{U}| < 1$. Now take a non -vanishing sequence $u: \mathbb{N} \rightarrow \mathbb{R}$ such that $\lim u = 0$.
**b)** *Claim.* $f$ is continuos $\Leftrightarrow \forall_{n \in \mathbb{N}}\forall_{r \in \mathbb{R}}\forall_{\epsilon \in \mathcal{R}_f} n \cdot |f^*(r + \epsilon) - f^*(r)|< 1$.
*Proof.* "$\Rightarrow$" Say that $f$ is continous, then by definition $\forall_{n \in \mathbb{N}}\forall_{r \in \mathbb{R}}\forall_{\epsilon \in \mathbb{R}_f} n \cdot |f(r + \epsilon) - f(r)|< 1$ where $\epsilon$ denotes an infinitesimal in $\mathbb{R}$. By remembering that every $f$ in $r$ gets interpreted as $[f \circ u]_\mathcal{U}$ in $r_i$, then the preavious statement implies, *given a continous function $u$*, that: $\forall_{n \in \mathbb{N}}\forall_{r \in \mathbb{R}}\forall_{\epsilon \in \mathbb{R}_f} n \cdot |u(f(r + \epsilon)) - u(f(r))|< 1$ $\Leftrightarrow f^*$ is continous.
**Corrections**: Assume that $f$ is continous. Let  $\epsilon in \mathcal{R}_f$ be infenitesimal, and let $n \in \mathbb{R}$. For $n \in \mathbb{N}$ there is a $\delta \in \mathbb{R}^{>0}$, $|f(n)- f(t)| < 1/n$ where $|t-1| < \delta$. Since $\epsilon$ is infinitesimal, there is a set $A \in \mathcal{U}$ with $|\epsilon_k|<\delta$ for all $k \in A$. Let for $k \in A$, we have $|f(n)- f(n + \epsilon k)|< 1/n$. So $A$ is a witness of the fact that $|f^*(n)-f^*(n + \epsilon)| < 1/n$. So $f^*(n) - f^*(n + \epsilon)$ is infinitesimal. Conversely, assume that $f$ is not continous at an $n \in \mathbb{R}$. So there is an $n \in \mathbb{N}$ s.t. for all $m \in \mathbb{N}$, there is an $\epsilon_m \in \mathbb{R}$, $|\epsilon_m| < 1/n$ but $|f(n)-f(n+ \epsilon_m)| \ge 1/n$. In particular we have a sequence $(\epslon_m)_{m \in \mathbb{N}}$, $\epsilon_0:=1$, and $\lim _{m \rightarrow + \infty} \epsilon_m=0$ and $|f(n) - f(n + \epsilon_m)| \ge 1/n$. So $[(\epsilon_m)_{m \in \mathbb{N}}]$ mi son rotto le palle 
**Q**: I suppose this doesn't hold if I don't assume $u$ to be continous, right?
"$\Leftarrow$" Say that $f^*$ is continous, means that: $\forall_{n \in \mathbb{N}}\forall_{r \in \mathbb{R}}\forall_{\epsilon \in \mathbb{R}_f} n \cdot |[u(f(r + \epsilon))]_\mathcal{U} - [u(f(r))]_\mathcal{U}|< 1$, therefore both functions $u$ and $f$ are continous.
**Remark**: Consider the ultraproduct $\mathbb{F}= M_{\mathcal{U}}\mathbb{F}_p (tildata la F)$ and \mathbb{P} = prime numbers, A \subseteq \mathbb{P} infinite set $\mathcal{U}$ free ultrafilter on $\mathbb{P}$ containing A. so \mathbb{F} is a field. For $p_0 \in \mathbb{P}, we have p_0 [(1)_p \in \mathbb{P}] \not = 0$ So $char(\mathbb{F})=0$, We can show that \mathbb{F} is uncountable. and by Łos' theorem òf is algebraically closed. Let $P \in òF [x]$.... Mi son rotto le palle anche qui, tanto non ho speranza di capire.
### LaTeX
````latex
\documentclass{article}
\usepackage{amsthm}
\usepackage{csquotes}
\usepackage{setspace}
\usepackage{amsfonts}
\usepackage[greek,english]{babel}
\usepackage[letterpaper,top=1.5cm,bottom=2cm,left=2cm,right=2cm,marginparwidth=1.75cm]{geometry}
\usepackage{graphicx}
\usepackage[colorlinks=true, allcolors=blue]{hyperref}
\usepackage[T1]{fontenc}
\usepackage{titling}
\setlength{\droptitle}{-4.5em}
\title{Model Theory Sheet II}
\author{Simone Testino }
\date{9th May 2023}

\begin{document}

\maketitle

\subsection*{Ex. 4}
\emph{Claim.} let $\mathcal{M}$ be an $\mathcal{L}$-*structure*, where $M$ is finite, then the natural embedding $\mathcal{M} \rightarrow \prod_\mathcal{U} \mathcal{M}$ is surjective.\\
\emph{Proof.} Consider a $\mathcal{M}$ being an $\mathcal{L}$-\emph{structure}, so $\mathcal{M}:= \langle M, (f_i)_{i \in I}, (R_j)_{j\in J}, (c_n)_{n \in N}\rangle$, and say $|M| < \aleph_0$. Let $\mathcal{U}$ be an ultrafilter on $\mathcal{M}$, and recall that a natural embedding is the mapping $d: \mathcal{M} \rightarrow \prod_\mathcal{U} \mathcal{M}$ s.t. $d(m)$ is the $\mathcal{U}$-equivalence class of the constant function with value $m$. Since the ultrapower is an ultraproduct with $\forall_{i \in I} \mathcal{M}_i = \mathcal{M}$, i.e. $\prod\mathcal{M} = \{ (m_i)_{i \in I} | \exists_{x \in I}\forall_{i \in I} m_x = m_i\}$, we can therefore notice that every element in $\prod \mathcal{M}$ is defined upon one element in $\mathcal{M}$ only by $d: m \mapsto (m_i)_{i \in I} \textit{ s.t. } \forall_{i \in I}(m_i = m)$ and reducing the elements by considering the equivalence classes on $=_{\mathcal{U}}$ can't change surjectivity; therefore the natural embedding $d: \mathcal{M} \rightarrow \prod_\mathcal{U} \mathcal{M}, m \mapsto f \textit{, s.t. } f: \mathbb{N} \rightarrow \mathcal{M}, n \mapsto m$ is surjective.

\subsection*{Ex. 5}
\textbf{a)} \emph{Claim.} There exists a first-order thoery in $\mathcal{L}_1$ of graphs without loops.\\
\emph{Proof.} Consider the given definition of a loop, namely that a loop is an element $e$ of $E$ in a graph $(V, E)$, s.t. $e= (v,v)$ for an element $v \in V$. Then the theory $T_{wl}$ must contain the following axiom $$\forall_{v \in V} \lnot(v \rightarrow v)$$This is a formula of $\mathcal{L}_1$. Similarly one could write this in $\mathcal{L}_\epsilon$ and it would be a theory $T_{wl}' := \{\forall_{v \in V} \lnot((v, v) \in E)\}$ if we consider $v \rightarrow w \Leftrightarrow (v, w) \in E$.\\
\textbf{b)} \emph{Claim.} There exists a first-order theory in $\mathcal{L}_1$ of connected graphs.\\
\emph{Proof.} The theory $T_c$ must contain an axiom expressing:$$\forall_{v, v' \in V}(\exists_{(v_i)_{i \in [1,n]\subset \mathbb{N}}}(v_i \rightarrow v_{i+1}) \land (v_1, v_n)=(v, v'))$$This is not a theory of $\mathcal{L}_1$, since $\mathbb{N}$ is not a symbol of the language. I shall therefore instead consider $X$ to be a subset of $E$; I need $X$ to be a chain, therefore I can define the set of chains from $v$ ot $v'$ to be $$X(v, v'):= \{X \subseteq E| (\exists_{u_1 \in V} (v, u_1) \in E) \land (\exists_{u_2 \in V}(u_1, u_2) \in E) \land ... \land (\exists_{u_{n-1}\in V}(u_{n-1}, v') \in E)\}$$Since it is defined trough a *finite* conjunction (the given definition of connectivity also requires the chain to be finite) and $v \rightarrow w \Leftrightarrow (v, w) \in E$ still holds, then $X(v, v')$ is a set defined in $\mathcal{L}_1$. Therefore I can state that:$$T_c := \{\forall_{v \in V}\forall_{v' \in V}(\exists_X X \in X(v, v'))\}$$ which is a first-order theory of connected graphs in $\mathcal{L}_1$.

\subsection*{Ex. 6}
Thanks to surjectivity of the natural embedding proved in Ex. 4, I know that $\mathcal{R}_f$ consists only of constant sequences (or functions form $\mathbb{N}$) with values in $\mathbb{R}_f$. Though $\mathcal{R}_f$ is written with a different signature in which $F$, the only function with ariety 1, is interpreted as $f^*$, s.t. $f^*([u(x)]_\mathcal{U})= [u(f(x))]_\mathcal{U}$ for any function $u: X \rightarrow \mathbb{R}$. The natural embedding therefore is of the form: $d: \mathbb{R}_f \rightarrow \mathcal{R}_f, r \mapsto (r_i)_{i \in I}$, s.t. $\forall_{i \in I}r_i = r$ and every $f$ in $r$ gets interpreted as $f^*$ in $r_i$. Therefore every $f$ in $r$ gets interpreted as $[f \circ u]_\mathcal{U}$ in $r_i$.\\
\textbf{a)} \textit{Claim.} I call $\epsilon$ an infinitesimal if $n\cdot max(\epsilon, -\epsilon) < 1$ for all $n \in \mathbb{N}$, then $\epsilon \in R_f$.\\
\textit{Proof.} if we consider all elements of $\mathbb{R}_f$ which don't contain $f$, then we notice that those have, through the natural embedding, a simple (meaning that it is almost an identity, $x \mapsto f$ s.t. $f: n \mapsto x$) correspondent, therefore since there are infenitesimals in $\mathbb{R}$ there must be in $\mathcal{R}_f$ too.\\
\textbf{b)} \textit{Claim.} $f$ is continuos $\Leftrightarrow \forall_{n \in \mathbb{N}}\forall_{r \in \mathbb{R}}\forall_{\epsilon \in \mathcal{R}_f} n \cdot |f^*(r + \epsilon) - f^*(r)|< 1$.
\emph{Proof.} "$\Rightarrow$" Say that $f$ is continous, then by definition $\forall_{n \in \mathbb{N}}\forall_{r \in \mathbb{R}}\forall_{\epsilon \in \mathbb{R}_f} n \cdot |f(r + \epsilon) - f(r)|< 1$ where $\epsilon$ denotes an infinitesimal in $\mathbb{R}$. By remembering that every $f$ in $r$ gets interpreted as $[f \circ u]_\mathcal{U}$ in $r_i$, then the preavious statement implies, \emph{given a continous function $u$}, that: $\forall_{n \in \mathbb{N}}\forall_{r \in \mathbb{R}}\forall_{\epsilon \in \mathbb{R}_f} n \cdot |u(f(r + \epsilon)) - u(f(r))|< 1$ $\Leftrightarrow f^*$ is continous.\\
\textbf{Q}: I suppose this doesn't hold if I don't assume $u$ to be continous, right?\\
"$\Leftarrow$" Say that $f^*$ is continous, means that: $\forall_{n \in \mathbb{N}}\forall_{r \in \mathbb{R}}\forall_{\epsilon \in \mathbb{R}_f} n \cdot |[u(f(r + \epsilon))]_\mathcal{U} - [u(f(r))]_\mathcal{U}|< 1$, therefore both functions $u$ and $f$ are continous.

\end{document}
````
## 5th Lecture
#### Compactness Theorem
**Theorem**: Let $T$ be a theory such that any finite subset of $T$ is consistent, then $T$ is consistent.
*Proof.* Let $I$ denote the set of finite subsets of $T$. Each $i \in I$ we write $i^* =\{j \in I| i \subseteq j\}$, and we let $I^* =\{i^* | i \in I\}$. We claim that $I^*$ has the finite intersection property (note that $\emptyset \not = i^* for all i \in I^*$) For $i_1, i_2 \in I, i_1^* \cap i_2^* = (i_1 \cup i_2)^*$ where $i_1 \cup i_2 \in I$ are $i_1^* \cap i_2^* \in I^*$. So there is an ultrafilter $\mathcal{U}$ on I which contains $I^*$. For each $i \in I$, since $i$ is consistent, there is a model $\mathcal{M}_i$ of $i$. We set $\mathcal{M}:=\prod_{\mathcal{U}}(\mathcal{M}'_i )_{i \in I}$, and we claim that $\mathcal{M}$ is a model of $T$. Let $\phi \in T$, so $\{\phi\} \in I$ where $\{\phi\}^* =\{i \in I | \phi \in i\} \subseteq \{i \in I| \mathcal{M_i}\models \phi\}$. So, by Łos' theorem, we see that $\mathcal{M} \models \phi \Leftrightarrow \{i \in I| \mathcal{M}_i \models \phi\} \in \mathcal{U}$, but the latter relation holds since $\{\phi^*\} \in \mathcal{U}$ and $\mathcal{U}$ is a filter. So $\mathcal{M} \models \phi$. Since this holds for any $\phi \in T$, we gave $\mathcal{M} \models T$, so $T$ is consistent, $QED$.
**Corollary**: there is no first-order theory in the language $\langle < \rangle$ of strict orderings, where models are exactly linearly ordered sets with the least upper bound propery for bounded sets (the LUB for bounded subsets: if $A \subseteq M$ is bounded ($\exists_{m_1, m_2 \in M} m_1 \le a \le m_2 \text{ for all } a \in A$) then $A$ has a least upper bound in $M$... basically, it means that the set has a supremum.)
*Proof.* Assume for contradiciton that such a theory $T$ exists. Consider the expanded language $\langle <, c, +\rangle$ where $c$ is a constant symbol and $+$ is a binary function symbol. Let $T'$ e the union of $T$ with the following list of sentences:
- sentences that insure a structure is a abelian group in $\langle + \rangle$
- $\forall_{v_0}\forall_{v_1}\forall_{v_2}((v_0 < v_1) \rightarrow (v_0 + v_2 < v_1 + v_2))$
- (0 < c_0 \land 0 < c_1)
- $\exists_{v_0} (\forall_{v_1}(v_0 è v_1 = v_1) \land v_0 < c_0 )$
- $c_0 + c_0 + ... + c_0 < 1$ (n-times) for all $n \in \mathbb{N}$
*Claim.* $T'$ is consistent. Indeed, if $T_0 \le T'$ is finite, then there is an $n \in \mathbb{N}$ such that $c_0 + ... + c_0 < c_1 \not \in T_0$ ($h$-times) for any $h \ge n$. Now we can see $\mathbb{R}$ as an $\langle <, c_0, c_1, + \rangle$-*structure* by itnerpreting $<, +$ as the classical realtion and sum and we can interpret $c_0$ as $1$ and $c_1$ to be $n \in \mathbb{R}$. Then, since $(\mathbb{R}, <)$ has the LUB for bounded sets, $(\mathbb{R}, +, <, 1, n) \models T_0$. So $T'$ is finitely consistent, hence consistent by compactness. Now if $\mathcal{M} = (\delta, +, <, m_0, m_1)$ is a model of $T'$, then we claim that $A=\{h \cdot c_0 |h \in \mathbb{N} \} is bounded but does not have a least upper bound. Indeed $\mathcal{M} \models c_0 + ... + c_0 < c_1$ ($n$-times) for all $n \in \mathbb{N}$, so $c_1 \ge A \ge 0: A$ is bounded. Let $\alpha \in M$ be an upper bound of $A$, then for $k \in \mathbb{N}$, we have $(k +1) m_0 < \alpha$, so $(h + 1)m_0-m_1 < \alpha - m_0$. So $\alpha - m_0$ is a strictly smaller upper bound of $A$. This constradicts the fact that $\mathcal{M} \models T$ (because $T \subseteq T'$), $QED$.
**Remark** By a theorem of Antin-Scheier, given a field $h$ and an algebraic closure $h (tildato)$ of $h$, we have $0 < [h: h(tildato)]< \infty$ iff. $h$ is a filed a model of $Th(\mathbb{R},+,\cdot)$. This seems to be not first order axiomatisable, though it is.
#### Model Contructions
##### Embeddings and Structures
We've seen filters already, which is one way, now we see more. First we need to fix a signature $((f_i)_{i \in I}, (R_j)_{j \in J}, k)$, and denote by $\mathcal{L}$ the corresponding first order language.
Def.* Let $\mathcal{M}=(M, (f_i^\mathcal{M})_{i \in I}, (R_j^\mathcal{M})_{j \in J}, (c^\mathcal{M}_{c \in K}))$ (LE F E R SONO SOTTOLINEATE)and $\mathcal{N}=(N, (f_i^\mathcal{N})_{i \in I}, (R_j^\mathcal{N})_{j \in J}, (c^\mathcal{N}_{c \in K}))$ are $\mathcal{L}$ structures, and let f $M \rightarrow N$ be a function. We say that f is an **embedding** (of $\mathcal{L}$-structures) if:
- for each $j \in J$, and all m_1,..., m_{\beta j} \in M, we have (m_1, ..., m_{\beta j}) \in R_j  (SOTTOLINEATA)
guarda ora le note su notablity
## Other Lectures are in the Notes
## Types, Extensions, Lö-Sk
**Definition**: Let $\mathcal{M}$ be an $\mathcal{L}$-structure, $A \subseteq M$ and $n \in \mathbb{N}$. An $n$-type of $\mathcal{M}$ over $A$ is a set $p(v_0, ..., v_n)$ of formulae in $\mathcal{L}_A$ with free variables among $v_0, ... , v_n$ s.t. for every finite subset $X$ of $p(v_0, ..., v_n)$, there is an elementary extension from $\mathcal{N}$ to $\mathcal{M}$ in $\mathcal{L}_A$ and a tuple $x_0, ..., x_n \in N$, s.t. $\mathcal{N} \models_{(\frac{v_0, ..., v_n}{x_0, ..., x_n})} \phi$ for all $\phi \in p(v_0, ... , v_n)$.
*Interpretazione*: Un type quindi è un insieme di formule che usano meno variabili di quelle che potrebbero inoltre esiste, dato un subset finito del type, una struttura in grado di soddisfarlo finitamente. Si tratta quindi di una nozione molto legata a quella di substructure. Lo si può anche definire come:
**Definition**: For $\bar{a} \in M^n$, the type of $\bar{a}$, $tp^{\mathcal{M}}(\bar{a}):= \{\phi(\bar{x})|\mathcal{M} \models \phi(\bar{a})\}$.
Those are then the set of all proposition that are satisfied by a constant $a$ in a given model $\mathcal{M}$.
**Definition**: An extension $\mathcal{M} \subseteq \mathcal{N}$ is **elementary** if for all $\bar{a} \in \bigcup_{n \in \omega}M^n$, $tp^{\mathcal{M}}(\bar{a}) = tp^{\mathcal{N}}(\bar{a})$. %%In particular remember that it is not true that $\mathcal{M} \models \phi \not \Rightarrow \mathcal{N} \models \phi$, but only the types on elements of $\mathcal{M}$ must remain the same.%%
**Ex**. Let $\mathcal{M} = (\omega, <)$ and $\mathcal{N} = (\{-1\}\cup \omega, <)$. Then the extension $\mathcal{M} \subseteq \mathcal{N}$ is not elementary since: $tp^{\mathcal{M}}(0) \not = tp^{\mathcal{N}}(0)$, for example we see $\phi(x) := \exists_y y < x$, we notice $\phi(x) \not \in tp^{\mathcal{M}}(0)$ and $\phi(x) \in tp^{\mathcal{N}}(0)$.
**Theorem**: Every infinite model has a proper elementary extension.
*Proof.* Let M be infinite, and let $T = Th(M,a)_{a\in M}$. Let c be a new constant, and let $T' =T\cup \{c \not=a |a\in M\}$. By the compactness theorem $T'$ has a model $\mathcal{N}$. Since $\mathcal{N} \models T, \mathcal{N}$ is an elementary extension of $\mathcal{M}$.
**Cor**: Every infinite model $\mathcal{M}$ has elementary extensions of arbitrary large cardinalities $> |M|$.
**Löwenheim-Skolem Theorem**: Let $\mathcal{N}$ be a model with at most countably many functions and constants. Then $\mathcal{N}$ has an elementary countable submodel.
**Ex**. $(\mathbb{R}, +, \times, 0, 1)$ has $2^{\aleph_0}$ countable real closed subfields. %%I'm unsure on this point%%
None of these extensions are elementary: $$(\mathbb{N},+,\times,0,1) \subseteq^1 (\mathbb{Z},+,\times,0,1) \subseteq^2 (\mathbb{Q},+,\times,0,1) \subseteq^3 (\mathbb{R},+,\times,0,1) \subseteq^4 (\mathbb{C},+,\times,0,1)$$We see that $1$ is not elementary since "there are elements before $0$" $2$ because of closure under inverse of $\times$, $3$ because of $\phi(x):= \exists_y y \times y= x$ and $4$ again because of $\phi(x)$.
**Theorem**: $\mathbb{N}$ , $\mathbb{Z}$  and $\mathbb{Q}$ have $2^{\aleph_0}$ countable elementary extensions. %%I suppose that these should be all those extensions with \omega with alle elements added and then \omega^\omega. they seem to be 2^{\aleph_0}. Obviously \omega_2 should not be one of those because it would then be uncountable.%%
%%I could continue with these kind of theorems from the slides on Elementary Extensions by Kossak, I stopped at slide 15/25.%%
**Definition**: A **nonstandard model of arithmetic** is a proper [elementary extension](https://ncatlab.org/nlab/show/elementary+extension) of the _standard model_ $(\mathbb{N},0,1,+,\times,S)$ of first-order [Peano arithmetic](https://ncatlab.org/nlab/show/Peano+arithmetic).

## Sheet 3
![[MT_Sheet_3.pdf]]
##### Ex. 7
Thanks to the Vaught's Test, I know that: Suppose every model of $T$ is infinite , $k \ge max(|\mathcal{L}|, \aleph_0)$ and $T$ is $k$-categorical. Then $T$ is complete. By definition of categoricity: $T$ is $k$-categotical iff any two models of $T$ of cardinality $k$ are isomorphic, then clearly $T$ is $k$-categorical and we also read that the language has cardinality $\aleph_0$ and therefore $k$ must only be an infinite cardinal.
I am left to prove that the Vaught's test holds from the theorems proved in class.
Suppose it doesn't hold. Then $T$ is not complete and therefore we have a $\phi$ an $\mathcal{L}$-sentence s.t. $T \not \models \phi$ and $T \not \models \lnot \phi$. Now define two other theories, $T_0 := T \cup {\phi}$ and $T_1 := {\phi}$. Since, by assumption, $T$ has only infinite models, then each $T_i$ has an infinite model. By the Löwenheim-Skolem theorem we know that there must be an $\mathcal{A}_i \models T_i$ where $\mathcal{A}_i$ has cardinality $k$. Since we know that $T$ is $k$-categorical, $\mathcal{A}_0 \cong \mathcal{A}_1$ and hence $\mathcal{A}_0 \equiv \mathcal{A}_1$ but, by assumption, $\mathcal{A}_0 \models \phi$ and $\mathcal{A}_1 \models \not \phi$, which is a contradiction
%%Guarda un po' che significa quel $\equiv$ %%
##### Ex. 8
###### a, c)
First I notice that $V$ is a model of $T$ if it is $\mathbb{Q}$-vector space, this must hold since we can simply use any torsion free divisible group to forma vector space. This observation will then be particularly useful for proving isomorphisms. Now consider $G$ as being a model of $T$, then take an element of $G$ called $g$ and natural number $n$, I can always find an $h \in G$ s.t. $nh = g$ (the two vectors are parallel). Then if, for $k \in G$, $nk = g$, then $n(k-h) =0_G$. Since the group is torsion free then we want there to be no two vectors that multiplied by $n$ give us $g$, then there is a unique $h\in G$ s.t. $nh = g$.
So I can now describe the theory $T$ as $$T:= \{\forall_{g \in G}\forall_{n \in \mathbb{N}}\exists_{h \in G}(nh = g),\forall_{g \in G}\forall_{n \in \mathbb{N}}\forall_{h \in G}\forall_{k \in G}((nk = g \land nh = g) \rightarrow n(k-h) = 0),$$$$\forall_{g \in G}\forall_{n \in \mathbb{N}} \exists_{h_1 \in G}\lnot \exists_{h_2 \in G}(\lnot(h_1 = h_2) \land (nh_1 = g) \land (nh_2 = g))\}$$One can define scalar multiplication by a natural number simply as a finite repetition of $+$ and therefore the propositions in $T$ can be written in the language $\langle +, 0 \rangle$.
Now, since I showed those models ti be vector spaces I can use the fact that two vector spaces over the same field are isomorphic if they have the same dimension. I also know that if $G$ has dimension $\lambda$, then $|G| = \lambda + \aleph_0$. Notice $k > \aleph_0$ and $G$ has cardinality $k$, then $G$ has dimension $k$, thus  any two models of cardinality $k$ are isomorphic. From what I showed already in Ex. 7, I can now use the Vaught's test in order to prove the theory to be complete and the only two requirements i need to check are that $T$ is $k$-categorica, which I just proved, and that every model of $T$ is infinite, which clearly emerges from the connection I sketched with the vector spaces since, as I shoed, if $G$ has dimension $\lambda$, then $|G| = \lambda + \aleph_0$ and clearly $\lambda \ge 0$. Therefore T is complete.

###### b)
Recall the way I defined $T$, now what we need more is simply an axiom checking that every group is also totally order. Therefore I can simply define: $$T_<:= T \cup \{\forall_{g,h \in G}(\lnot(g = h)\rightarrow((g < h \lor h < g)\land \lnot(g < h \land h < g))), \forall_{g\in G}\lnot(g<g)\}$$
###### d)
I know both $(\mathbb{Q}, +)$ and $(\mathbb{Z}, +)$ are divisible, totally ordered, abelian groups and have clearly the same cardinality since $|\mathbb{Q}| = |\mathbb{Z}|$. Therefore they are isomorphic (as proved in 8c), though clearly  $(\mathbb{Q}, +, <)$ and $(\mathbb{Z}, +, <)$ are not, since i the first it holds that $\forall_{x, y}\exists_z(x<z<y \lor y<z<x)$but in the second clearly it clearly doesn't.

##### Ex. 9
WTS: I start by noticing that the theory of dense linear complete closed intervals $DLO_c$ is complete. Then I define models on growing intervals such that the union on every $n \in \mathbb{N}$ takes the whole $\mathbb{Q}$. In such a model it won't hold anymore that there is a maximal and a minimal element.
Consider the language $\mathcal{L}:= \langle < \rangle$  and define a sequence of closed intervals $[n, -n]$ structures $M_n:=[n,-n]$ and the theory is $DLO_c:= DLO \cup \{\exists_x\forall_y(x<y), \exists_x\forall_y \lnot(x<y)\}$ where $DLO$ is the theory of dense linear ordered intervals which I know to be not complete, though $DLO_c$ is complete (am I supposed to prove it or can I take it as given from external literature?). Clearly $DLO_c$ holds on any closed interval and since $M = \bigcup_{n \in \mathbb{N}} M_n = \bigcup_{n \in \mathbb{N}} [n, -n] = \mathbb{Q}$ where $DLO_c$ clearly doesn't hold, and therefore $\mathcal{M} \not \models DLO_c$.


##### Ex. 10
###### a)
*Claim.* given a $n$-type $\tau$ of $\mathcal{M}$ over $A$: $\tau$ is complete $\Leftrightarrow$ $\tau$ isn't properly contained another type of $\mathcal{M}$ over $A$.
*Proof.* "$\Leftarrow$" Assume that $\tau$ is not properly contained in any other type of $\mathcal{M}$ over $A$, then assume for contradiction that $\tau$ is not complete. Since $\tau$ is not complete then there must be a formula $\phi$ of $\mathcal{L}_A$ s.t. $\tau \not \in \phi \land \tau \not \in \lnot \phi$. Then I can define $\tau_1 := \tau \cup \{\phi\}$ and it would be a type properly containing $\tau$. We get then contradiction and have shown that a type not properly contained in any other type is complete.
"$\Rightarrow$" Assume $\tau$ to be complete and assume for contradiction that $\tau$ is properly contained in another type of $\mathcal{M}$ over $A$, name it $\tau_1$. By the second assumption there exists a formula $\phi$ of $\mathcal{L}_A$ s.t. $\phi \in \tau_1 \land \phi \not \in \tau$. By the assumption that $\tau$ is complete I derive that $\tau \models \lnot \phi$, but since $\tau$ is also a proper subset of $\tau_1$ I notice that $\tau_1 \models \lnot \phi$, which is a contradiction. Therefore I proved that any complete type must not be properly contained in another type on the same structure and over the same set.

###### b)
*Claim.* Any $n$-type of $\mathcal{M}$ over $A$ is contained in a complete type.
*Proof.* Consider $\tau$ to be an $n$-type of $\mathcal{M}$ over $A$, if $\tau$ is complete, then it is contained (nor properly) in itself. Assume then $\tau$ to be not complete. Then there is a set of propositions $\Phi_\tau:=\{\phi_1, ...\}$ s.t. $\forall_{\phi \in \Phi}\tau \not \models \phi$. We can then define the sequence of types defined recursively: Given a $\phi \in \Phi_{\tau_{n}}$, then $\tau_{n+1} := \tau_{n} \cup \{\phi\}$. By this process we will get to the complete theory containing $\tau$.

###### c)
As i did previously I assume by contradiction that $tp_A(\overline{m})$ is not complete, so there must be a $\phi$ s.t. $tp_A(\overline{m}) \not \models \phi$ and $tp_A(\overline{m}) \not \models \lnot \phi$, and also $\phi$ must have $n$ or less free variables. In order to get to contradiction I have to check two conditions (i) $FV(\phi) \subseteq \{v_0, ..., v_n\}$ and (ii) $\mathcal{M} \models_{(\frac{v_0, ..., v_n}{m_0, ..., m_n})} \phi$ or similarly for $\lnot \phi$. Since $\phi$ is in $\mathcal{L}_A$ and since it "could" be in the type, then it must have not more than $n$ free variables which are a subset of the variables in $M$, so (i) holds. By definition of type we know that for every finite subset we must be able to elementary extend a structure $\mathcal{N}$ s.t.  $\mathcal{N} \models_{(\frac{v_0, ..., v_n}{m_0, ..., m_n})} \psi$  for all $\psi \in tp_A(m_0, ... , m_n)$ and therefore (ii) must clearly hold too. Therefore $\phi$ or $\lnot \phi$ must be in the type, which, therefore, must be complete.

##### Ex. 11
%%Dovrei provarci ma senza troppe speranze, magari se non lo correggessimo in classe potrei provare a farlo assieme a Pascal come esercizio.%%

##### LaTeX
```LaTeX
\documentclass{article}
\usepackage{amsthm}
\usepackage{csquotes}
\usepackage{amsfonts}
\usepackage{amsmath}
\usepackage{setspace}
\usepackage[greek,english]{babel}
\usepackage[letterpaper,top=2cm,bottom=2cm,left=3cm,right=3cm,marginparwidth=1.75cm]{geometry}
\usepackage{graphicx}
\usepackage[colorlinks=true, allcolors=blue]{hyperref}
\newtheorem{lemma}{Lemma}
\newtheorem{theorem}{Theorem}
\newtheorem{definition}{Definition}

\title{Sheet 3}
\author{Simone Testino}
\date{21st June 2023}
\begin{document}


\maketitle

\subsection*{Ex. 7}
Thanks to the Vaught's Test, I know that: suppose every model of $T$ is infinite, $k \ge max(|\mathcal{L}|, \aleph_0)$ and $T$ is $k$-categorical. Then $T$ is complete. By definition of categoricity: $T$ is $k$-categorical iff any two models of $T$ of cardinality $k$ are isomorphic, then clearly $T$ is $k$-categorical and we also read that the language has cardinality $\aleph_0$ and therefore $k$ must only be an infinite cardinal.

I have left to prove that the Vaught's test holds from the theorems proved in class.
Suppose it doesn't hold. Then $T$ is not complete and therefore we have a $\phi$ an $\mathcal{L}$-sentence s.t. $T \not \models \phi$ and $T \not \models \lnot \phi$. Now define two other theories, $T_0 := T \cup {\phi}$ and $T_1 := {\phi}$. Since, by assumption, $T$ has only infinite models, then each $T_i$ has an infinite model. By the Löwenheim-Skolem theorem we know that there must be an $\mathcal{A}_i \models T_i$ where $\mathcal{A}_i$ has cardinality $k$. Since we know that $T$ is $k$-categorical, $\mathcal{A}_0 \cong \mathcal{A}_1$ and hence $\mathcal{A}_0 \equiv \mathcal{A}_1$ but, by assumption, $\mathcal{A}_0 \models \phi$ and $\mathcal{A}_1 \models \not \phi$, which is a contradiction
%%Guarda un po' che significa quel $\equiv$ %%

\subsection*{Ex. 8}
\textbf{a, c)}
First I notice that $V$ is a model of $T$ if it is $\mathbb{Q}$-vector space, this must hold since we can simply use any torsion free divisible group to form a vector space. This observation will then be particularly useful for proving isomorphism. Now consider $G$ as being a model of $T$, then take an element of $G$ called $g$ and natural number $n$, I can always find an $h \in G$ s.t. $nh = g$ (the two vectors are parallel). Then if, for $k \in G$, $nk = g$, then $n(k-h) =0_G$. Since the group is torsion free then we want there to be no two vectors that multiplied by $n$ give us $g$, then there is a unique $h\in G$ s.t. $nh = g$.

\noindent So I can now describe the theory $T$ as $$T:= \{\forall_{g \in G}\forall_{n \in \mathbb{N}}\exists_{h \in G}(nh = g),\forall_{g \in G}\forall_{n \in \mathbb{N}}\forall_{h \in G}\forall_{k \in G}((nk = g \land nh = g) \rightarrow n(k-h) = 0),$$$$\forall_{g \in G}\forall_{n \in \mathbb{N}} \exists_{h_1 \in G}\lnot \exists_{h_2 \in G}(\lnot(h_1 = h_2) \land (nh_1 = g) \land (nh_2 = g))\}$$
One can define scalar multiplication by a natural number simply as a finite repetition of $+$ and therefore the propositions in $T$ can be written in the language $\langle +, 0 \rangle$.

Now, since I showed those models ti be vector spaces I can use the fact that two vector spaces over the same field are isomorphic if they have the same dimension. I also know that if $G$ has dimension $\lambda$, then $|G| = \lambda + \aleph_0$. Notice $k > \aleph_0$ and $G$ has cardinality $k$, then $G$ has dimension $k$, thus  any two models of cardinality $k$ are isomorphic. From what I showed already in Ex. 7, I can now use the Vaught's test in order to prove the theory to be complete and the only two requirements i need to check are that $T$ is $k$-categorical, which I just proved, and that every model of $T$ is infinite, which clearly emerges from the connection I sketched with the vector spaces since, as I showed, if $G$ has dimension $\lambda$, then $|G| = \lambda + \aleph_0$ and clearly $\lambda \ge 0$. Therefore T is complete.\\

\noindent \textbf{b)}
Recall the way I defined $T$, now what we need more is simply an axiom checking that every group is also totally order. Therefore I can simply define: $$T_<:= T \cup \{\forall_{g,h \in G}(\lnot(g = h)\rightarrow((g < h \lor h < g)\land \lnot(g < h \land h < g))), \forall_{g\in G}\lnot(g<g)\}$$

\noindent \textbf{d)}
I know both $(\mathbb{Q}, +)$ and $(\mathbb{Z}, +)$ are divisible, totally ordered, Abelian groups and have clearly the same cardinality since $|\mathbb{Q}| = |\mathbb{Z}|$. Therefore they are isomorphic (as proved in 8c), though clearly  $(\mathbb{Q}, +, <)$ and $(\mathbb{Z}, +, <)$ are not, since i the first it holds that $\forall_{x, y}\exists_z(x<z<y \lor y<z<x)$but in the second clearly it clearly doesn't.

\subsection*{Ex. 9}
WTS: I start by noticing that the theory of dense linear complete closed intervals $DLO_c$ is complete. Then I define models on growing intervals such that the union on every $n \in \mathbb{N}$ takes the whole $\mathbb{Q}$. In such a model it won't hold anymore that there is a maximal and a minimal element.

Consider the language $\mathcal{L}:= \langle < \rangle$  and define a sequence of closed intervals $[n, -n]$ structures $M_n:=[n,-n]$ and the theory is $DLO_c:= DLO \cup \{\exists_x\forall_y(x<y), \exists_x\forall_y \lnot(x<y)\}$ where $DLO$ is the theory of dense linear ordered intervals which I know to be not complete, though $DLO_c$ is complete (am I supposed to prove it or can I take it as given from external literature?). Clearly $DLO_c$ holds on any closed interval and since $M = \bigcup_{n \in \mathbb{N}} M_n = \bigcup_{n \in \mathbb{N}} [n, -n] = \mathbb{Q}$ where $DLO_c$ clearly doesn't hold (e.g. by any of the two axioms reported), and therefore $\mathcal{M} \not \models DLO_c$.


\subsection*{Ex. 10}
\textbf{a)}
*Claim.* given a $n$-type $\tau$ of $\mathcal{M}$ over $A$: $\tau$ is complete $\Leftrightarrow$ $\tau$ isn't properly contained another type of $\mathcal{M}$ over $A$.

*Proof.* "$\Leftarrow$" Assume that $\tau$ is not properly contained in any other type of $\mathcal{M}$ over $A$, then assume for contradiction that $\tau$ is not complete. Since $\tau$ is not complete then there must be a formula $\phi$ of $\mathcal{L}_A$ s.t. $\tau \not \in \phi \land \tau \not \in \lnot \phi$. Then I can define $\tau_1 := \tau \cup \{\phi\}$ and it would be a type properly containing $\tau$. We get then contradiction and have shown that a type not properly contained in any other type is complete.

"$\Rightarrow$" Assume $\tau$ to be complete and assume for contradiction that $\tau$ is properly contained in another type of $\mathcal{M}$ over $A$, name it $\tau_1$. By the second assumption there exists a formula $\phi$ of $\mathcal{L}_A$ s.t. $\phi \in \tau_1 \land \phi \not \in \tau$. By the assumption that $\tau$ is complete I derive that $\tau \models \lnot \phi$, but since $\tau$ is also a proper subset of $\tau_1$ I notice that $\tau_1 \models \lnot \phi$, which is a contradiction. Therefore I proved that any complete type must not be properly contained in another type on the same structure and over the same set.\\

\noindent \textbf{b)}
*Claim.* Any $n$-type of $\mathcal{M}$ over $A$ is contained in a complete type.

*Proof.* Consider $\tau$ to be an $n$-type of $\mathcal{M}$ over $A$, if $\tau$ is complete, then it is contained (nor properly) in itself. Assume then $\tau$ to be not complete. Then there is a set of propositions $\Phi_\tau:=\{\phi_1, ...\}$ s.t. $\forall_{\phi \in \Phi}\tau \not \models \phi$. We can then define the sequence of types defined recursively: Given a $\phi \in \Phi_{\tau_{n}}$, then $\tau_{n+1} := \tau_{n} \cup \{\phi\}$. By this process we will get to the complete theory containing $\tau$.\\

\noindent \textbf{c)}
As I did previously, I assume by contradiction that $tp_A(\overline{m})$ is not complete, so there must be a $\phi$ s.t. $tp_A(\overline{m}) \not \models \phi$ and $tp_A(\overline{m}) \not \models \lnot \phi$, and also $\phi$ must have $n$ or less free variables. In order to get to contradiction I have to check two conditions (i) $FV(\phi) \subseteq \{v_0, ..., v_n\}$ and (ii) $\mathcal{M} \models_{(\frac{v_0, ..., v_n}{m_0, ..., m_n})} \phi$ or similarly for $\lnot \phi$. Since $\phi$ is in $\mathcal{L}_A$ and since it "could" be in the type, then it must have not more than $n$ free variables which are a subset of the variables in $M$, so (i) holds. By definition of type we know that for every finite subset we must be able to elementary extend a structure $\mathcal{N}$ s.t.  $\mathcal{N} \models_{(\frac{v_0, ..., v_n}{m_0, ..., m_n})} \psi$  for all $\psi \in tp_A(m_0, ... , m_n)$ and therefore (ii) must clearly hold too. Therefore $\phi$ or $\lnot \phi$ must be in the type, which, therefore, must be complete.

\end{document}
```
## Definability
*Definition*: Let $\mathcal{M}$ be an $\mathcal{L}$-structure, let $n \in matb{N}^{>0}$. A subset $X \subset M^n$ is said definable in $\mathcal{M}$ (in dimension $n$) if there is a formula $\phi(v_0, ..., v_n)$ s.t. $X = \phi(\mathcal{M})$, where $\phi(\mathcal{M})$ denotes the set of element satisfying $\phi$, namely: $\{(m_1, ..., m_n)| \mathcal{M} \models_{(\frac{v_0, ..., v_{n-1}}{m_1, ..., m_n})} \phi\}$.
If $A \subseteq M$ is a subset, then a subset $X \subseteq M^n$ is definable in $\mathcal{M}$ with parameters in $A$ if it is definable in $\mathcal{A} = (M, ..., (a)_{a \in A})$, an $\mathcal{L}_A$-structure.
#### Boolean Algebra

## Sheet 4
![[MDT_Sheet_4.pdf]]
#### Ex. 12
a) Consider the formula $\phi_a(x) := \exists_y \lnot y = 0 \land y \cdot y = x$, clearly $\phi_a(\mathcal{N})$ is the required set and $\phi_a$ is a formula in $\mathcal{L}$.
b) Consider the formula $\phi_b(x) := \lnot \exists_y \exists_z y \cdot z = x$. This is the definition of irredicible which is equivalent to the one of prime number in $\mathbb{Z}$, so clearly $\phi_b(\mathcal{N})$ is the required set and $\phi_b$ is a formula in $\mathcal{L}$.
**Corr.** Ripensa ad irreducibility, they can be one. It's fine to use irreducibility.
c) Consider the formula $\phi_c(x) := x = p \cdot ... \cdot p$ repeated for any $m \in \mathbb{N}_0$. Clearly $\phi_c(\mathcal{N})$ is the required set and $\phi_c$ is a formula in $\mathcal{L}$.
**Corr.** Era meglio scrivere $\phi_c\forall_x ((y|x \land \phi_b(y))\rightarrow  y = p)$.

Question 1. Can we use "For $\bar{a} \in M^n$, the type of $\bar{a}$, $tp^{\mathcal{M}}(\bar{a}):= \{\phi(\bar{x})|\mathcal{M} \models \phi(\bar{a})\}$." as definition of a type? Is it equivalent to the one we have? I find it more intuitive, assuming that the interpretation I have of it is correct, namely: "A type of $\bar{a}$ in $\mathcal{M}$ is the set of all proposition satisfied by $\bar{a}$ in $\mathcal{M}$, where $\bar{a}$ is a finite set of variables in $M$."





Question 2. The definition I have of elementary extension is "An extension $\mathcal{M} \subseteq \mathcal{N}$ is elementary if for all $\bar{a} \in \bigcup_{n \in \omega}M^n$, $tp^{\mathcal{M}}(\bar{a}) = tp^{\mathcal{N}}(\bar{a})$."
Is it true that in order to check if the extension is elementary we need to check $n$-types with $n>0$? Otherwise all formulas without free variables would be counted, like "every subset of $\mathbb{N}$ has a minimal element" and ex. 13.a would be wrong.





#### Ex. 13
Claim 1. $N^* = \mathbb{N} \cup \{\omega\} \cup ...$ for $\omega$ defined as satisfying $\phi(x) := \lnot \exists_y y >x$.
Proof. There are four cases for adding a constant $c$ into $\mathbb{N}$
Case 1. $\lnot \exists_y y < c \Rightarrow c < 0$
$\phi_1 \in tp^\mathcal{N}(0)$ where $\phi_1(x) := \lnot \exists_y y < x$, $\phi \not \in tp^\mathcal{N^*}(0)$, then $tp^\mathcal{N}(0) \not = tp^\mathcal{N^*}(0)$, then $\mathcal{N}^*$ is no elementary extension of $\mathcal{N}$.
Case 2. $\exists_x \exists_y x<c<y$
Case 2.1. $\exists_x x < c < x+1$
$\lnot \exists_y x < y < x+1 \in tp^\mathcal{N}(x)$, but $\lnot \exists_y x < y < x+1 \not \in tp^\mathcal{N^*}(x)$ by assumption, then $\mathcal{N}^*$ is no elementary extension of $\mathcal{N}$.
Case 2.2. $\lnot \exists_x x < c < x+1$ and $c$ is no minimal nor maximal element
Then there are two elements $z$ and $x$ s.t. $z + x = c$ in $N^*$ but there is also an $y \in \mathbb{N}$ s.t. $x + z = y$, then in $N^*$ it holds $c =y$ and therefore $c$ is not a new constant since every element in $\mathbb{N}$ is clearly definable in $\mathcal{N}$.
Case 3. $\forall_x x \bot c$
$\phi_2 \in tp^\mathcal{N}(2)$ where $\phi_2(x):= \forall_y x<y \lor y<x$ and $\phi_2 \in tp^\mathcal{N^*}(2)$, then $tp^\mathcal{N}(2) \not = tp^\mathcal{N^*}(2)$, then $\mathcal{N}^*$ is no elementary extension of $\mathcal{N}$.
Case 4. $\lnot \exists_y y > c \Rightarrow c = \omega$
Since we assume in the exercise to be such an $N^*$ it must then be containing such constants.

b) Since any $\mathcal{N}^*$ has the form of a non standard model, then it clearly follows that any subset of $N^*$ has an element $n^*$, s.t. $n^* > n$ for all $n \in \mathbb{N}$.

a) Since $N^*$ is of the form $\mathbb{N}\cup\{\omega\}\cup...$ and since, as we know, there always must be a minimal element in $\mathcal{N}$ since there always must be one in $\mathbb{N}$.
Consider $N^*_1:= \mathbb{N} \cup \Omega$  where $\Omega := \{\omega, \omega - 1, \omega -2, ...\}$. It is easy to notice that $\Omega$ has no minimum.
**Corr.** Let $X \subseteq N^*$ be definable in $\mathcal{N}^*$, let $\phi(x)$ be a formula s.t. $X = \phi(\mathcal{N}^*)=\{n^* \in N^*| \mathcal{N} \models \phi)n^*)\}$ also assume that $X \not = \emptyset$.
Let $y = \phi(\mathcal{N}) \subseteq \mathbb{N}_0$. We claim that $y$ is a non-empty. Indeed $\mathcal{N}^* \models \exists_x(\phi(x))$ so since $\mathcal{N}^* \cong \mathcal{N}$ we have $\mathcal{N} \models \exists_x(\phi(x))$, i.e. $y \not = \emptyset$. So $y$ has a minimum. Therefore $\mathcal{N} \models \exists_x(\phi(x) \land \forall_y(\phi(y) \rightarrow (x = y \lor x < y)))$ so $\mathcal{N}^* \models \exists_x(\phi(x) \land \forall_y(\phi(y) \rightarrow (y = x \land x < y)))$. So $X$ has a minimum.

c) Claim: $tp_1^\mathcal{N}(v_0) := \{1 + ... + 1 < v_0 | n \in \mathbb{N}\} \subseteq tp_2^\mathcal{N}(\emptyset) \land tp_1^\mathcal{N}(v_0) \subseteq tp^\mathcal{N}_3(\emptyset) \land tp^\mathcal{N}_2(\emptyset) \not = tp^\mathcal{N}_3(\emptyset)$.
Proof. I suppose then that $tp_2$ and $tp_3$ are $1$-types or they could not share elements with $tp_1$.
**Corr.** Find an $\mathcal{N}^*$ and two realizations of $p(v_0)$ with distinct complete types. (Realized type? Meaning??). $a, b \in \mathcal{N}^*, \phi(v_0) \in tp^{\mathcal{N}^*}(a) \\ tp^{\mathcal{N}^*}(k)$ where both are subsets of $p$. $a, b \in Z$ (non ho la def). Say $a =$ prime in $N^*$, $b = a +1$. $a$ is even. $\mathcal{N}^* \models \exists_(x + x = a)$, so $b$ is not even, $\mathcal{N}^* \models \exists_(x + x +1 = b)$. Cosa sono i parametri? Credo siano gli elementi che puoi definire solo in metalanguage, tipo prendere i numeri in $\mathbb{Q}$ anche se non sono ez da definire, tipo in un ordering o un gruppo con 0 e 1.

#### Ex. 14
Definition. $\mathcal{M}$ has definable choice over $A$ if for all formulas $\phi$ with FV and parameters in $A$, there is a partial function $f: M^n \rightarrow M$ which is definable over $A$ and s.t. $\mathcal{M} \models \phi (m_0, ..., m_{n-1}, f(m_0, ..., m_{n-1}))$  for all $m_0, ..., m_{n-1} \in M$ and s.t. $\mathcal{M} \models_{(v_i \rightarrow m_i)} \exists_{v_n} \phi (v_0, .., v_{n-1}, v_n)$. 
I interpret it as: $f$ is able to give you the missing variable that makes $\phi$ true (for every $\phi$ on every set of variables), i.e. $f$ is able to define the choice of the last variable in order to satisfy a proposition, clearly $f$ is defined through $\phi$, then I write $f_\phi$.

a) Claim: Let $\mathcal{M}$ have a definable choice over $A$ and $\mathcal{N} = (N, ...)$ be an elem. expansion of $\mathcal{M}$. Show: $\mathcal{N}$ has def. choice over $A$.
Proof. By considering the previous definition i gave of elementary expansion, the claim becomes trivial since: elem. expansion i.e. $\bar{a} \in \bigcup_{n \in \omega}M^n$, $tp^{\mathcal{M}}(\bar{a}) = tp^{\mathcal{N}}(\bar{a})$. Since $A^n \subseteq M^n$ then for every $\bar{a} \in A^*$  we have $tp^{\mathcal{N}}(\bar{a}) = tp^{\mathcal{N^*}}(\bar{a})$, then since there exists one $f_\phi$ forall $\phi \in tp^{\mathcal{N}}(\bar{a})$ it is also a partial function for e very $\psi \in tp^{\mathcal{N^*}}(\bar{a})$, since $\phi = \psi$, so $f_\phi = f_\psi$, so $f_\psi$ exists. It must also hold that $\mathcal{M} \models_{(v_i \rightarrow m_i)} \exists_{v_n} \psi (v_0, .., v_{n-1}, v_n)$ by def. of type.
**Corr.** Let $\phi(v_0, ..., v_n)$ be a formula in $\mathcal{L}_A$. We want an $f: N^n \rightarrow N$ definable over $A \subseteq N$ s.t. $\forall_{m_0, ..., m_{n-1} \in N} \phi(m_0, ..., m_{n-1}, \mathcal{N}) \not = \emptyset$ so $\mathcal{N} \models \phi(m_0, ..., m_{n-1}, f(m_0, ..., m_{n-1}))$. true for $\mathcal{N} = \mathcal{M}$. So there is a $\psi(v_0, ..., v_n) \in \mathcal{L}_A$ which defines a relation $f \subseteq M^{n +1}$ in $\mathcal{M}$, $f = \psi(\mathcal{M})$. Let $g = \psi(\mathcal{N}) \subseteq N^n \times N$. We have that $g$ is a choice function for $\mathcal{N}$.
-  $g$ is a function: $\forall_{a_0, ..., a_{n-1}\in N}(\exists!_{a_n \in N}(\mathcal{N} \models (\psi(a_0, ..., a_{n-1}))))$ si true since it amoints to $\mathcal_{M}, \mathcal{N} \models \forall_{v_0, ..., v_{n-1}}(\exists!_{v_n}(\psi(v_0, ..., v_{n-1})))$.
- .... Tante altre cose che boh non mi sono troppo chiare sto compando a caso, magari faccio uan foto, se guardi la foto fatta il 7.07 alle 9:15 vedi quel che manca e che cmq non ho capito. o

b) Definition. an infinite [structure](https://en.wikipedia.org/wiki/Structure_(mathematical_logic) "Structure (mathematical logic)") (_M_,<,...) that is [totally ordered](https://en.wikipedia.org/wiki/Total_order "Total order") by < is called an o-minimal structure if and only if every [definable](https://en.wikipedia.org/wiki/Definable_set "Definable set") subset _X_ ⊆ _M_ (with parameters taken from _M_) is a finite [union](https://en.wikipedia.org/wiki/Union_(set_theory) "Union (set theory)") of [intervals](https://en.wikipedia.org/wiki/Interval_(mathematics) "Interval (mathematics)") and points.
Method for conducting the proof: I believe a) is suggesting me to find a structure that clearly has definable choice over $M$ and whose elementary extension is $\mathcal{M}$. Though I have basically no example of decidable structures over some sets, and I will therefore try to prove it by induction on complexity of formulae by simply using the definition.

Proof. by induction on complexity of formulae,
"$=$": Consider first all formulae that are equations, so for $x$, $y \in M$, such formulae are of the form $x = y$ where $x$ and $y$ can be any combination of other elements with the $+$ operations, which will always give elements in $M$ by closure under addition of groups. For any such equation we know that if we have an unknown in the formula, we can solve it and get a function giving us its value in function of the remaining variables, so clearly any atomic formula made by "$=$" is have decidable choice, so I can affirm that $\mathcal{M}$ has definable choice on $A_1 := \{\phi \in \mathcal{L}|\exists_x \exists_y \phi = (x=y)\}$.
Note: There might be formulae with more than on solution definable in such a group, in such cases a simple distinction of cases should be enough to chose one specific solution to any equation similarly to what I do next for inequalities.
"$<$": Similarly we can do it for inequalities, any formula of the form $x < y$ is solvable, though we need to choose one value only that makes the formula true (and not giving all of them as we would normally do by solving inequalities, otherwise we would get more than a result and we wouldn't have function). So for any atomic formula of the form $x < y$, when say $y$ is the missing variable, $f: x \mapsto x+1$ and with subtraction if $x$ is the missing one. So I can affirm that $\mathcal{M}$ has definable choice on $A_2 := \{\phi \in \mathcal{L}|\exists_x \exists_y \phi = (x<y)\}$.
"$\land$": For conjunction of these atomic formulae we do nothing but building systems of equations (or disequations) which we know to be solvable for one unknown. Though some systems may give no solution at all, like, for $a, b \in M$: $x = a \land x = b \land \lnot (a =b)$ in such cases there's no value in $M$ to which $f$ should point, in fact, for such formulae, no variable assignment will make them true and then no $f$ is suppose to exist on them. When we hae a solution we can clearly solve the system with one unknown and therefore $\mathcal{M}$ has definable choice on the closure under $\land$ of $A_1$ and $A_2$. 
"$\lnot$": For any negated formula on which $\mathcal{M}$ has decidable choice, we just have to give a value that is not the solution of the equation or inequality. In fact for inequalities just invert the $+1$ and $-1$ from the previously described way. For equations, when they have one solution only, I have to arbitrarily chose one value different form the solution. Therefore $\mathcal{M}$ has definable choice on the closure under $\lnot$ of $A_1$ and $A_2$.
Since "$\lnot$" and "$\land$" are enough for defining "$\lor$" and "$\rightarrow$" I need not to prove anything for those. Left to prove the closure under quantifiers. Though I notice that I have not used at all the o-minimality and therefore I suppose I should apply it somehow in the proof of closure of atomic formulae under quantors. Though I am not sure how to procede. I believe though that the part on "$<$" together with its closures is enough for the exercise c.
**Corr.** Quello che fa lui è prendere tutti gli intervalli e mostrare che da questi intervalli puoi sempre scegliere un numero tra quelli in maniera che la funzione mandi un input ad un solo output. Quindi qua il gioco sarebbe vedere se puoi o non puoi usare i parametri (gli oggettini non definibili) e quando sei quindi dnetro questi intervalli allora devi essere in grado di prendere un elemento che sta dentro quell'elemento. Gli intervalli sono si atra due elemnti definiti ma anche congli infiniti. Ricorda che in un gruppo il neutral element è sempre definibile.

Question 3. How much abstract algebra knowledge (or definitions) are required for the exam? Are we allowed to ask for clarification if such definitions are supposed to be in background knowledge?




Question 4. Is it possible to have a check list of the most fundamental topics for the exam? It would also help if it could have explicit references (like pages or chapters) to the book.



**Corr. b)** Come prima cosa definitamo una \phi(v_0, v_1) che ci dia il consueto ordering in \mathbbb{N}, Sop di che per ogni formula con varie variabili che stia nel linguaggio di N, allora ogni volta che prendi. Controlla che è una partial function. e poi fai tante cos ematte che son troppostanco per seguire, magari faccio una foto

#### Correction:
Incompleteness Theorem sembra avere qualche relazione con l'esercizio 12.
a) 


## Lecture
#### ==Exam Infos==
28.07, 3 problems, 90'.

I) Application of compactness, similar to what
: axiomatise  + show non-axiomatisability
could be ordered groups/archimedean orderd groups, 
show that there is a theory that is exactly
show that there is no theory...

II)=ì L'esercizio più grande, will contain
types, definability, eelementary extensions, (guarda bene la dimostrazione of Łos theorem, ultraproduct theorem)

III) Quantifier eleimination results + o-minimality, di cui vedremo esempi più avanti

Per I e II non hai particolarmente necessita di conoscenza generale di Matematica
ma per il III

III. ordered groups, devi sapere che sono quelli, sii semplicemente familiare con le definizioni
Also:
Delyll And priesst

I. 5
II.2, II.3, II.4
III.4 (quant. elimination)

Non ci sara nulla sulla model completeness ad esempio (peccato perché la avevo capita)

## Exam Parts
### III. Quantifier Elimination
Def. $\mathcal{A}$ first order theory $T$  eliminate quantifiers (or has quantifier elimination/QE) in $\mathcal{L}$ if for all formulae $\phi(v_0, ..., v_n)$ there is a quantifier free formulae $\psi(v_0, ..., v_{n-1})$ s.t. $T \models \forall_{v_0},... \forall_{v_{n-1}}(\phi(v_0, ..., v_{n-1}) \leftrightarrow \psi(v_0, ..., v_n-1))$. 

In particular definable sets in models of $T$ are quantifier free definable.
Proposition. If $T$ is consistent and eliminates quantifiers then $T$ is complete.
Proof. Let $\mathcal{M}, \mathcal{N} \models T$ with $\mathcal{M} \subseteq \mathcal{N}$. Let $\phi(v_0, ..., v_{n-1})$ be a formula, let $h: Vbl \rightarrow M$. Let $\psi(v_0,..., v_{n-1})$ be a quantifier-free with $T \models \forall_{v_0}, ..., \forall_{v_{n-1}}(\phi(v_0, ..., v_{n-1}) \leftrightarrow \psi(v_0, ..., v_{n-1}))$.
We have $\mathcal{M} \models_h \phi \Leftrightarrow \mathcal{M} \models_h \phi \Leftrightarrow \mathcal{N} \models_h \psi \Leftrightarrow \mathcal{N} \models_h \phi$. See $\mathcal{M} \le \mathcal{N}$.
Lemma. Let $T$ be a first order theory. Assime that for alla quantifier-free formulae $\phi(v_0, .., v_{n-1})$, there is a quantifier-rfree formuala $\theta(v_0, ..., v_{n-1})$ s.t. $T \models \forall_{v_0}, ..., \forall_{v_{n-1}}(\theta(v_0, ..., v_{n-1})) \leftrightarrow \exists_{v_n}(\psi(v_0, ..., v_{v-1}))$. Then $T$ eliminates quantifiers.
(If we want to eliminate quandier we just have to eliminate one quantifier and also we jave to look only at one variable and then we can eliminate several varables. Quindi siamo fortunati che ci basta guardare ad un quantifier solo ed un avaribale sola, una volta fatto cosi lo abbiamo per tutti, ottimo risultato.)
Proof. By induction over complexity of $\phi(v_0, ..., v_{n-1})$, you show that there is a $\mu(v_0, ..., v_{n-1})$ quantifier-free, with $T \models \forall_{v_0}, ..., \forall_{v_{n-1}}(\phi(v_0, ..., v_{n-1}) \leftrightarrow \mu)v_0, ...., v_{n-1})$. Now distinguish cases:
- If $\phi$ is quantifier-free than just $\phi = \mu$
- Let $\phi_{0}(v_0, ..., v_{n-1}), \phi_1(v_0, ..., v_{n-1}), \mu_0(v_0, ..., v_{n-1}), \mu_1(v_0, ..., v_{n-1})$, where \mu_0, \mu_1 are quantifier-free and $T \models \forall_{v_0}, ..., \forall (\phi_i(v_0, ..., v_{n-1}) \leftrightarrow \mu_1,(v_0, ..., v_{n-1}))$ i= 0, 1.
- on the notes the rest

## Sheet 5
![[MT_Sheet_5.pdf]]
#### Ex. 15
a) $T$ is the theory that has one function symbol $f$ which is a bijective function. So models of $T$ will have sets and one bijective function between them. In order to prove consistency of a theory I just need to give a model of it, consider for example a model $\mathcal{M}$ where $f$ is interpreted as the identity function on $M$.

Question 1. What I need to show is only that such a bijective $f$ can always be interpreted in it, e.g. as the identity function here, right?

b) Since $T$ must not be infinite, I cannot directly apply the Vaught's Test.
Since we have no other symbol in $\mathcal{L}$, then $f$ can only be defined as $f(v_0)=v_0$ or $\lnot f(v_0) = v_0$ . There clearly are models of the theory where one or the other are true e.g. consider the NOT operator and the identity in boolean algebra. Therefore $T \not \models f(v_0)=v_0$, $T \not \models \lnot f(v_0)=v_0$ so $T$ is not complete.

**Corrections**:
Che minchia ho scritto, dio boia, son puttanate. Offiviamente il not operator non è definito cosi. Say integers with the function $n + 1$, È un modello di $T$ in cui $f$ chiaramente non è l'identità. Comunque va bene, obv hai capito ma attento a che minchia scrivi.

c) Since $T$ is not model complete then it can't have quantifier elimination, as we proved in class.
**Corrections**: 
Forse si ma considera 
#### Ex. 16
Let $\mathbb{K}$ be an algebraically closed field, then $\mathbb{K}_n := \mathbb{K}[X_1, ..., X_n]$ a ring and $I$ a prime ideal in $\mathbb{K}_n$.
Claim: There is an $\bar{a} \in \mathbb{K}^n$ s.t. for all $Q \in I$, $Q(\bar{a})=0$.
Proof. Since $I$ is a prime ideal I know by def. that $\forall_{a, b \in \mathbb{K}_n \setminus \mathbb{K}^\times} a \cdot b \in I \rightarrow a \in I \lor b \in I$. Therefore I know that if there is a polynomial $a \cdot b$ in $I$ then there must be a second polynomial, $a$ or $b$ that has degree less than $a \cdot b$. Since we are in an algebraically closed ring, the only irreducible elements (and hence prime elements, since $\mathbb{K}_n$ is a factorial domain) are the normed first degree polynomials. Therefore I know that if, say, $x_1^3  + 4x_2 - 3 \in I$, then $x_1 + \lambda \in I \lor x_2 + \lambda \in I$. I notice therefore that $\mathbb{K}_n$ is a PID (principal ideal domain) and therefore notice that since $I$ is prime then it must be a principle ideal of the form $(\lambda_0 \cdot (a_1\cdot x_1 + \lambda_1)\cdot ...\cdot (a_n\cdot x_n + \lambda_n))$  for $(a_i)_{i \in [1, n]}$ where $a_i \in \{0,1\}$ and  $(\lambda_i)_{i \in [0, n]} \subseteq \mathbb{K}$. Clearly I can now define the root of this polynomial (name it $p$) that generates the ideal as a $\bar{b} \in \mathbb{K}^n$ s.t. for any $i \in [1, n]$ I have $a_i = 1 \rightarrow b_i = - \lambda_i$ clearly $p(\bar{b})=0$ and since it is a principle ideal any other element of it will be of the form $p \cdot q$ and therefore clearly $\bar{b}$ will be a root of that polynomial too.

Question 2. Is this an model theoretic enough proof? Which non-algebraic tools was I supposed to use?

#### Ex. 17
$T_{rc}$ is the theory of ordered fields $\mathbb{K}$ where every monic irreducible polynomial (in $\mathbb{K}[X]$) of degree $> 1$ is of the form $X^2 + b X + c$ where $b^2 + 4c < 0$.

a) $T_{rc}$ is consistent since I can define a model $\mathcal{M}$ s.t. $\mathcal{M} \models T_{rc}$. Let $\mathcal{M} := (\mathbb{R}, +, \cdot, 0, 1)$ where we know that irreducible polinomials of degree $\ge 2$ have the named form. One could analogously name $\mathbb{Q}$.

b) $T_{rc} \models \lnot \exists_x (x^2 + bx + c =0) \leftrightarrow b^2 - 4c < 0$. So left to prove is that the theory of ordered fields has quantifier elimination, we know that real closed fields have quantifier elimination on their usual language and that the same holds for the reals as an ordered additive group, so $T_{rc}$ has QE on $\mathcal{L}_{or}$.

d) We cannot say the same for $\mathcal{L}_r$ since $\phi(b, c) : =b^2 - 4c < 0 \not \in \mathcal{L}_r$. And since $\mathcal{L}_r \subset \mathcal{L}_{or}$ then there is no $\psi \in \mathcal{L}_r$ s.t. $T_{rc} \models \psi(b,c) \leftrightarrow \phi(b,c)$ where $\psi(b,c)$ can syntactically use no other symbol than the one in $\phi(b,c)$ but without "$<$".

Question 3. Are such more syntactical proofs also fine in general?

c) Since I have shown the theory to have quntifier elimination on $\mathcal{L}_{or}$ then it must also be complete. I then need to show that one structure only of $T_{rc}$ is o-minimal in order to show that $T_{rc}$ is o-minimal. This clearly is the case since every subset of $\mathbb{R}$ is made up by points or intervals.

#### Ex. 18
$T_0$ is the theory of algebraic closed fields of characteristic 0. Let $\mathcal{U}$ be a free ultrafilter on $\mathbb{P}$ and the corresponding ultraproduct (and not an ultrapower, right?) $\prod_\mathcal{U}(\tilde{\mathbb{F}}_p)_{p\in \mathbb{P}}$. 

a) Now we know that the characteristic function, which takes fields as inputs, gives $Ch(\tilde{\mathbb{F}}_p) = p$ but since the ultraproduct is running over $p \in \mathbb{P}$ then the characteristic of $\prod_\mathcal{U} (\tilde{\mathbb{F}}_p)_{p\in \mathbb{P}}$ cannot be any $p$ for any $p > 0$, since the formula $1 + ... +1 = 0$ $p$-times is true in one field only ($\mathbb{F}_p$) and not in all the (infinite) others. Therefore $\prod_\mathcal{U} (\tilde{\mathbb{F}}_p)_{p\in \mathbb{P}}$ is a field of characteristic $0$. I know that it is also algebraically closed since any $\tilde{\mathbb{F}}_p$ is algebraically closed by def.

b) iii) Once i) and ii) are proved just notice that the set of $p$ s.t. i) and ii) hold, are a subset of $\mathbb{P}$ and are finite, then it does not hold for almost all models of the ultraproduct.
ii) Just prove that it is the closure of F_p https://math.stackexchange.com/questions/3967894/algebraic-closure-of-mathbb-f-p.

i) Consider the polymial function $f: (\tilde{\mathbb{F_p}})^n \rightarrow (\tilde{\mathbb{F}_p})^n,  (a_1, . . . , a_n) \mapsto (P_1(a_1, . . . , a_n), . . . , P_n(a_1, . . . , a_n))$ ... say I have found sucha. function that is injective and not surjective

ii) Here I need to simply claim that $(\tilde{\mathbb{F}_p})^n = (\mathbb{F}_{p^k})^n$ for some $k \in \mathbb{N}$. Take a polynomial $p(x)\in \mathbb{F}_p[x]$. Then, $p(x)\in \mathbb{F}_{p^k}[x]$ for some $k$. The splitting field is a finite extension of characteristic $p$, so it is isomorphic to $\mathbb{F}_{p^l}$ for some $l$ (by characterisation of finite fields). Hence, $p(x)$ must split over $\mathbb{F}_p$.
..?

iii) Since we see that the definition of $f$ must depend on $p$ then clearly such an $f$ exists for finitely many fields in the sequence (namely only $\mathbb{F}_{p^k}$) and therefore in the ultraprodut there cannot be such a function. From what I have proved in a) I can now conclude that there cannot be such a function in any model of $T_0$.

## Quantifier Elimination
Notes from youtube Math 557 Quantifier Elimination
**Def.** For any $\phi \in \mathcal{L}$ there is a quantifier free $\psi$ s.t. $T \models \phi \leftrightarrow \psi$, then $T$ has quantifier elimination.
**Example**: $DLO$ without endpoints has QE.
*Proof.* $\sigma(x_1, ..., x_n)$ is a variable constellation, those are formulae of the form $x_1 > x_3 \land x_2 = x_4 \land x_4 < x_3$ and those are possibly inconsistent. Let $\phi$ be an $\mathcal{L}_<$ formula, $\phi$ is satisfieable in $\mathbb{Q}$ via $\bar{a}$ $\Rightarrow$ $\bar{a}$ satisfies some var. constellations $\sigma(\bar{a})$. Define now $\psi_\phi(\bar{x}) = \bigvee$ var. const. arising this way (as some $\sigma(\bar{a})$). Then clearly $\mathbb{Q} \models \phi(\bar{a}) \rightarrow \psi_\phi(\bar{a})$ but you can also show the converse which is harder. Since $T$ is complete, it is enough to show it for $\mathbb{Q}$ only.
Completeness of the theory is not enough for quantifier elimination.
$\mathbb{N}$ has NOT QE.
$(\mathbb{Q, <})$ element. embedds into any model of $DLO$ since it is model complete.
the following hold:
- $\mathcal{M} \subseteq \mathcal{N}$, $\bar{a} \in M$: $\phi$ is q.f. then $\mathcal{M} \models \phi[a] \Leftrightarrow \mathcal{N} \models \phi [\bar{a}]$.
- If $M \subseteq N$, then $\mathcal{M} \subseteq \mathcal{N} \Leftrightarrow \mathcal{N}_M \models \Delta \mathcal{M}$ remember that
	- the quantifier free diagram is $\Delta(\mathcal{M}) := \{\phi| \mathcal{M} \models \phi \land \phi$ is q.f. $\}$
	- and $\mathcal{N}_M$ is a str. in the extended language, where all $m \in M$ are now constants.
**1. Criterion for QE**: $T$ has QE $\Leftrightarrow$ If $\mathcal{M}, \mathcal{N} \models T$, $\mathcal{A} \subseteq \mathcal{M}, \mathcal{N}$: for any $\bar{a} \in A$, $\mathcal{M} \models \phi(\bar{a}) \Leftrightarrow \mathcal{N} \models \phi(\bar{a})$.
In particular notice that if you set $\mathcal{A} = \mathcal{M}$ then you get *model completeness*. What is required here is more though. Model completeness is different form completeness, e.g. $ACF$ (alg. closed fields) has QE but is not complete ($ch(\tilde{\mathbb{F}}_3) \not = ch(\mathbb{C})$).
So, to prove that $T$ doesn't have QE, just find two models of $T$ s.t. $\mathcal{N} \subseteq \mathcal{M}$ but not elementary.
**2. Criterion for QE**: Just prove you can eliminate $\exists$.
**1 + 2. Criterion for QE**: For $\mathcal{M}, \mathcal{N} \models T$, for any $\mathcal{A} \subseteq \mathcal{M}, \mathcal{N}$ for any q.f. $\phi(x_0, x_1, ..., x_n)$ if there is a $\bar{a} \in A^n$ and $b_0 \in M$ s.t. $\mathcal{M} \models \phi [b_0, \bar{a}]$ then there is a $c_0 \in N$ s.t. $\mathcal{N} \models \phi [c_0, \bar{a}]$, then $\exists_{x_0} \phi$. Then $T$ has QE.
# Briefly, Theorems and Defs.
**Def. Filter**: (i) $\emptyset \not \in \mathcal{F}, I \in \mathcal{F}$, (ii) Closed under $\cap$ (iii) Closed under supersets in $I$
	**Principal Filter**: If $x \in I$ then $\mathcal{F}$ is generated by $x$, if $x$ is a singleton, then $\mathcal{F}$ is ultra
	**Fréchet Filter**: $F = \{A \subseteq I | I \setminus A \text{ is finite}\}$ 
	**Free Filter**: Contains a Fréchet filter
	**Ultrafilter**: (i) $\forall_{A,C \subseteq I} A \cup B \in \mathcal{F} \Rightarrow A \in \mathcal{F}$ or $B \in \mathcal{F}$ (prime filter on $\cup$) or (ii) is a maximal filer
	**FIP**: If the intersection over any finite subcollection of $I$ is non empty
	**Creation of a Filter**:  If $\mathcal{A} \subset \mathcal{P}(I)$ has the FIP, then there is a filter $\mathcal{F}$ on $I$ with $\mathcal{A} \subseteq \mathcal{F}$
	**Extension of a Filter**:  $\mathcal{F} \cup \{A\}$ is contained is a filter on $I$.
	**Ultraproducts**: $\prod_{i \in I} \mathcal{M}_i / \mathcal{U}$
		**Łos Theorem**: $\prod_{i \in I} \mathcal{M}_i / \mathcal{U} \models \phi (m_1,…,m_n) \Leftrightarrow  \{i \in I:M_i \models \phi (m_{1,i},…,m_{n,i})\} \in \mathcal{U}$.
	**Ultrapower**:  $\prod_{i \in I} \mathcal{M} / \mathcal{U}$
**Embedding**:(i) constants (ii) functions (iii) relations but *only injective for the variables*
	**I. Type**: $p$ is a $n$-type of $Th(\mathcal{M})$ $\Leftrightarrow$ e.ext. $\mathcal{N}$ of $\mathcal{M}$ s.t. $\exists_{b \in N} \mathcal{N} \models p(b)$ $\Leftrightarrow$ $\forall_{p_0 \subset p} \exists_{b \in M} \mathcal{M} \models p_0(b)$.
	**II. Type**: $tp^\mathcal{M}(a)$ is the complete type of $a$ in $\mathcal{M}$
	**Elementary Embedding**: $\mathcal{M} \models_h \phi \Leftrightarrow \mathcal{N} \models_{\tau \circ h} \phi$
	**Elementary Equivalence**, $\equiv$**: $\mathcal{M} \models \phi \Leftrightarrow \mathcal{N} \models \phi$
	Elementary Extension**: $\mathcal{M} \subseteq \mathcal{N}$ s.t. for all $\bar{a} \in \bigcup_{n \in \omega}M^n$, $tp^{\mathcal{M}}(\bar{a}) = tp^{\mathcal{N}}(\bar{a})$.
	**Substructure**: $N \subseteq M$, $\mathcal{N}$ closed and same outputs on everything $\mathcal{M}$ has.
	**Elementary Substructure**: $\mathcal{M} \models \phi \Leftrightarrow \mathcal{N} \models \phi$ and $\mathcal{N}$ substr. of $\mathcal{M}$
		**E. Emb $\Rightarrow$ E. Eq** p. 72
	**Compactness Theorem**: Any finite subset of $T$ is consistent $\Leftrightarrow$ $T$ is consistent.
	**Corr. to Comp.** If $\Gamma \models \phi$ then there is a finite $\Gamma_0$ s.t. $\Gamma_0 \models \phi$.
	**Löwenheim-Skolem Theorem**: Inf. $\mathcal{M}$, inf. $k$, then there is an E. Ex. or E. Sub. $|\mathcal{N}| = k$.
	**Definable Choice**: $\mathcal{M}$ has def. choice over $A$ if for every form. with param. in $A$ $\phi(v_0, ..., v_n)$ there is a *partial func.* (not def on all $M^n$) $f: M^n \rightarrow M$, $\mathcal{M} \models \phi(m_0, ..., m_{n - 1}, f(m_0, ..., m_{n- 1}))$
**Quantifier Elimination**: For $\phi \in \mathcal{L}$ there is $\psi \in \mathcal{L}$ w.q., s.t. $T \models \psi \leftrightarrow \phi$ and with $FV(\phi) = FV(\psi)$
	**QE $\Rightarrow$ Model Completeness**: For every str. s.t. $\mathcal{M}, \mathcal{N} \models T$: $\mathcal{M} \subseteq \mathcal{N}\Rightarrow \mathcal{M} \preceq \mathcal{N}$.
	**T.-V. test**: $\mathcal{N} \preceq \mathcal{M} \Leftrightarrow \forall_{\phi(c, y_1, ..., y_n)}\forall_{b_1, ..., b_n \in N}\mathcal{M} \models \exists_x \phi(x, b_1, ..., b_n) \rightarrow \exists_{a \in N} \mathcal{M} \models \phi(a, b_1, ..., b_n)$.
	**QE $\Rightarrow$ Def. Sets without Quantifiers are all Def. Sets.**
	**1. Criterion for QE**, $T$ has QE $\Leftrightarrow$ If $\mathcal{M}, \mathcal{N} \models T$, $\mathcal{A} \subseteq \mathcal{M}, \mathcal{N}$: for $\bar{a} \in A^n$, $\mathcal{M} \models \phi(\bar{a}) \Leftrightarrow \mathcal{N} \models \phi(\bar{a})$.
	**2. Criterion for QE**: Just prove you can eliminate $\exists$.
	**O-minimality on $\mathcal{M}$**: Every definable subset $X \subseteq M$ is a finite union of intervals and points.
	**O-min** $\Leftrightarrow \mathcal{M} \models \phi(v_0) \leftrightarrow \psi(v_0)$ where $\psi(v_0) \in \mathcal{L}_<$... true?
	**O- min on $T$**: Every model of $T$ has O-min
	**$T$ complete** $\Rightarrow$ just one O-min str. needed
	**Use QE for O-min**: QE $\land$ Sets def. by atomic $\phi(v_0)$ are finite unions of intervals $\Rightarrow$ O-min.
	We [know](https://en.wikipedia.org/wiki/Quantifier_elimination): [abelian groups](https://mathoverflow.net/questions/402099/quantifier-elimination-for-abelian-groups#:~:text=Abelian%20groups%20are%20the%20same,called%20Baur%E2%80%93Monk%20invariants), [DLO](https://math.stackexchange.com/questions/3229235/questions-regarding-the-proof-of-quantifier-elimination-of-dlo), algebraically closed fields, real closed fields are **QE**
	We [know](https://en.wikipedia.org/wiki/O-minimal_theory): DLO in $\mathcal{L}_>$, real closed fields are **o-min**
	**RCF**: $\mathbb{F}[i]$ is ACF $\Leftrightarrow$ $\mathbb{F} \equiv \mathbb{R}$
**Categoricity**: $T$ is $k$-cat. iff any two models of $T$ of card, $k$ are isomorphic.
**Vaught's test**: if all $\mathcal{M} \models T \Rightarrow |\mathcal{M}|  \ge \aleph_0$, $k \ge max(|\mathcal{L}|,\aleph_0)$ and $T$ is $k$-cat. then $T$ is complete.


#### Probable Exercise:
From [here](https://math.stackexchange.com/questions/3427247/no-single-axiom-stating-non-archimedeanity), checked also [this](https://math.stackexchange.com/questions/193826/do-ordered-fields-and-archimedian-ordered-fields-have-the-same-first-order-theor?rq=1).
*Claim*: There is no first order theory of Archimedean Ordered Groups:
*Proof*. Let $T_g$ be the first order theory of ordered groups (see below) and now define $T_g' := T_g \cup \{\phi_n | n \in \mathbb{N}\}$ where $\phi_n:= \exists_x(x>0 \land  c>x + ... + x)$. Now notice that any finite subset $T_g'$ has an Archimedean model. So, assume for contradiction that there is a first order axiom defining Archimedean groups, call it $T_A$, then define $T_g'' := T_g' \cup T_A$. Clearly any finite subset of $T_g''$ has a model (which is Archimedean), thus, by compactness $T_g''$ has a model too, but since "$c = \omega$" such a model cannot be Archimedean and is therefore not existent. Then we get contradiction and such a $T_A$ cannot exist, thus there is no first order theory of Archimedean Ordered Groups.

The theory of ordered groups, named above $T_g$:
- $\forall_x \exists_y (x + y = 0)$
- $\forall_x (x + 0 =x)$
- $\forall_{x, y} \exists_z (x + y = z)$
- $\forall_x \lnot( x < x)$
- $\forall_x \forall_y \lnot(x < y \land y<x)$
- $\forall_{x, y, z} (x < y \land y < z \rightarrow x<z)$
- $\forall_{x, y} (x<y \lor y<x)$
Archimidean Property: $\forall_x \forall_y \exists_{n \in \mathbb{N}} x<ny$
##### Quantifier Elimination Technique
1. I need first to show that for the given theory $\exists_ x\bigwedge^n_{i = 1}L_i$ is equivalent to a quantifier free formula. Such formulae are, in groups, simple systems of polynomials which can always be solved.
2. Then notice that any quantifier free formula $F$ can be written as $\bigvee^m_{i = 1} \bigwedge^n_{i = 1}L_{ij}$ and use that $\exists \bigvee^m_{i = 1} \bigwedge^n_{i = 1}L_{ij} \Leftrightarrow \bigvee^m_{i = 1} \exists_x\bigwedge^n_{i = 1}L_{ij}$. Then you get that Those formuale are also quantifier free.
3. Notice that showing it for $\exists$ is enough, simply show that since $L$ can have a negation then it must hold for $\forall$ too.
# Questions To Vincent
```LaTeX
\documentclass{article}
\usepackage{amsthm}
\usepackage{csquotes}
\usepackage{amsfonts}
\usepackage{amsmath}
\usepackage{setspace}
\usepackage[greek,english]{babel}
\usepackage[letterpaper,top=2cm,bottom=2cm,left=3cm,right=3cm,marginparwidth=1.75cm]{geometry}
\newtheorem{Question}{Question}
\usepackage{graphicx}
\usepackage[colorlinks=true, allcolors=blue]{hyperref}


\title{Questions To Vincent}
\author{simone.testino }
\date{July 2023}

\begin{document}

\maketitle

\subsection*{On Corrections of Sheet 3}
\textbf{Question 1.} On Ex. 8 you corrected my definition of $T$ by showing that it cannot be a theory of formulae in the language since I used natural numbers. Though just below the theory I wrote: "One can define scalar multiplication by a natural number simply as a finite repetition of $+$ and therefore the propositions in $T$ can be written in the language $\langle +, 0 \rangle$" is it not enough to write a justification like that s.t. every use of the natural numbers can be translated in the language? How should i have written it otherwise?\\
\\
\\
\\
\\
\textbf{Question 2.} In Ex. 10, would the folowing definition of $\Psi_\tau$ make tegh exercise fully right? \[\Phi_\tau := \{\phi_1, ...\}\textit{ s.t. }\forall{\phi \in \Phi} \tau \not \models \phi \land \tau \not \models \lnot \phi\]Since I imagined it as a recursive process, this set gets redifined on every cycle when $\tau$ changes, therefore only those fromulae that are \emph{independent} from $\tau$ will be added. Should I also prove something on the cardinality of $\Phi_\tau$ (e.g. that it is countable since I suppose the language also is countable)?
\\
\\
\\
\\
\subsection{On Theory}
\text{Question 3.} In the lecture we talked about types and complete types but I believe we didn't use the notation $tp^\mathcal{M}(\bar{a})$, is it right to define it as the set of all formulae with $|\bar{a}|$ many free variables s.t. evaluated at $\bar{a}$ they hold in $\mathcal{M}$?
\\
\\
\\
\\
\textbf{Question 4.} Did we see in the lectures a theorem that relates Quantifier Elimination and O-minimality? Is there one? I found that QE $\Rightarrow$ O-minimality, can we use this in the exam?
\\
\\
\\
\\
I may have some question on decidable functions but I want to first wait for the corrections of sheet 4 and see if I menage to get a more concrete understanding by myself.
\end{document}



```

# Exam Program
The exam will have three exercises:
1. Applications of the **Compactness Theorem**: axiomatize theory or show their non-axiomatisability. Consider theories of groups in general, in particular *archimedean ordered groups*. **Ch. I. 5**
2. **Types, Definability, Elementary Extensions**, but also **Ultrafilters and Ultraproducts**. Consider in particular the **Łos Theorem** and its proof. **Ch. II. 2-4**
3. **Quantifier Elimination**, its results and **o-minimality**. **Ch. III. 4**
Model completeness and other not mentioned things will *not* be in the exam.
### 1. Compactness Theorem
#### Theory
#### Compactness Theorem
**Theorem**: Let $T$ be a theory such that any finite subset of $T$ is consistent, then $T$ is consistent.
	*Proof.* Let $I$ denote the set of finite subsets of $T$. Each $i \in I$ we write $i^* =\{j \in I| i \subseteq j\}$, and we let $I^* =\{i^* | i \in I\}$. We claim that $I^*$ has the finite intersection property (note that $\emptyset \not = i^* for all i \in I^*$) For $i_1, i_2 \in I, i_1^* \cap i_2^* = (i_1 \cup i_2)^*$ where $i_1 \cup i_2 \in I$ are $i_1^* \cap i_2^* \in I^*$. So there is an ultrafilter $\mathcal{U}$ on I which contains $I^*$. For each $i \in I$, since $i$ is consistent, there is a model $\mathcal{M}_i$ of $i$. We set $\mathcal{M}:=\prod_{\mathcal{U}}(\mathcal{M}'_i )_{i \in I}$, and we claim that $\mathcal{M}$ is a model of $T$. Let $\phi \in T$, so $\{\phi\} \in I$ where $\{\phi\}^* =\{i \in I | \phi \in i\} \subseteq \{i \in I| \mathcal{M_i}\models \phi\}$. So, by Łos' theorem, we see that $\mathcal{M} \models \phi \Leftrightarrow \{i \in I| \mathcal{M}_i \models \phi\} \in \mathcal{U}$, but the latter relation holds since $\{\phi^*\} \in \mathcal{U}$ and $\mathcal{U}$ is a filter. So $\mathcal{M} \models \phi$. Since this holds for any $\phi \in T$, we gave $\mathcal{M} \models T$, so $T$ is consistent, $QED$.
**Example**: There is no first-order theory in the language $\langle < \rangle$ of strict orderings, where models are exactly *linearly ordered sets with the least upper bound propery for bounded sets* (the LUB for bounded subsets is defined as: if $A \subseteq M$ is bounded ($\exists_{m_1, m_2 \in M} m_1 \le a \le m_2 \text{ for all } a \in A$) then $A$ has a least upper bound in $M$... basically, it means that the set has a supremum.)
*Proof.* Assume for contradiciton that such a theory $T$ exists. Consider the expanded language $\langle <, c, +\rangle$ where $c$ is a constant symbol and $+$ is a binary function symbol. Let $T'$ be the union of $T$ with the following list of sentences:
- sentences that insure a structure is a abelian group in $\langle + \rangle$
- $\forall_{v_0}\forall_{v_1}\forall_{v_2}((v_0 < v_1) \rightarrow (v_0 + v_2 < v_1 + v_2))$
- $(0 < c_0 \land 0 < c_1)$
- $\exists_{v_0} (\forall_{v_1}(v_0 è v_1 = v_1) \land v_0 < c_0 )$ (?)
- $c_0 + c_0 + ... + c_0 < 1$ (n-times) for all $n \in \mathbb{N}$
*Claim.* $T'$ is consistent. Indeed, if $T_0 \le T'$ is finite, then there is an $n \in \mathbb{N}$ such that $c_0 + ... + c_0 < c_1 \not \in T_0$ ($h$-times) for any $h \ge n$. Now we can see $\mathbb{R}$ as an $\langle <, c_0, c_1, + \rangle$-*structure* by interpreting $<, +$ as the classical realtion and sum and we can interpret $c_0$ as $1$ and $c_1$ to be $n \in \mathbb{R}$. Then, since $(\mathbb{R}, <)$ has the LUB for bounded sets, $(\mathbb{R}, +, <, 1, n) \models T_0$. So $T'$ is finitely consistent, hence consistent by compactness. Now if $\mathcal{M} = (\delta, +, <, m_0, m_1)$ is a model of $T'$, then we claim that $A=\{h \cdot c_0 |h \in \mathbb{N} \} is bounded but does not have a least upper bound. Indeed $\mathcal{M} \models c_0 + ... + c_0 < c_1$ ($n$-times) for all $n \in \mathbb{N}$, so $c_1 \ge A \ge 0: A$ is bounded. Let $\alpha \in M$ be an upper bound of $A$, then for $k \in \mathbb{N}$, we have $(k +1) m_0 < \alpha$, so $(h + 1)m_0-m_1 < \alpha - m_0$. So $\alpha - m_0$ is a strictly smaller upper bound of $A$. This constradicts the fact that $\mathcal{M} \models T$ (because $T \subseteq T'$), $QED$.
**Remark** By a theorem of Antin-Scheier, given a field $h$ and an algebraic closure $h (tildato)$ of $h$, we have $0 < [h: h(tildato)]< \infty$ iff. $h$ is a filed a model of $Th(\mathbb{R},+,\cdot)$. This seems to be not first order axiomatisable, though it is.
**Application** in to the Lö-Sk theorem If $T$ has an infinite model $\mathcal{A}$ then it can have a larger structure.
*Proof.*
	let $\mathcal{A}$ be an infinite $\tau$-structure and $max(|A|, |\tau|) \le k$ then $\mathcal{A}$ has an elementary extension of cardinality $k$. I divide it in two steps:
	Step 1.
		Construct an elementary extension $\mathcal{A}'$ of cardinality $\ge k$, we choose a set $p$ of new constant symbols, $|p| = k$. Then consider $T := Th(\mathcal{A}_A) \cup \{\lnot c = d | c, d, \in p, c \not =d\}$, I claim that any finite subset of this new theory $T$ is satisfiable. Since $A$ is infinite, all finite subsets of $T$ are satisfiable. But the compactness theorem implies that $T$ has a model $\mathcal{A}''$. %%mancano due righe ma comuque non mi è chiarissima%%
#### Similar Exercises
##### Show that there is a theory
**Method 1.** Simply find it. Find a set of axioms that describe the theory.
##### Show that there is no such theory (first order)
*Show that there is no first order theory whose models exactly are connected graphs*:
*Proof*. Define the formula: $$\psi_n(v_1, v_2):= \lnot (\exists_{v_3},..., \exists_{v_{n+2}}(v_3 \rightarrow v_4)\land ...\land (v_{n+1} \rightarrow v_{n+2}) \land (v_3 = v_1) \land (v_{n+2}=v_{2}))$$Now define $T' =T \cup \{\psi_n(v_1, v_2)| n\in \mathbb{N}\}$. Every finite subset $T_0 \subseteq T$ is consistent, define $T_0$ s.t. there is a $n_0$ s.t. for $k \ge n_0$, $\psi_k(v_1, v_2) \not \in T_0$. Consider then for example the loop that has a way from $v_1$ to $v_2$ with infinite knots between and one straigh passage in the other way around. This graph is model of $T_0$. So the compactness theorem says that then $T'$ is consistent so let $\mathcal{M}$ be a model of $T'$, ad this gives us the graph $G=(V, E)$ and two vertices $x, y$. They must be connected and must be not connected, $QED$.
Second attempt:
\emph{Claim}: there is no first order theory whose models exactly are connected graphs:\\
\emph{Proof}. Define the formula: $$\psi_n(v_1, v_2):= \lnot (\exists_{v_3},..., \exists_{v_{n+2}}(v_3 \rightarrow v_4)\land ...\land (v_{n+1} \rightarrow v_{n+2}) \land (v_3 = v_1) \land (v_{n+2}=v_{2}))$$Now define $T' =T \cup \{\psi_n(v_1, v_2)| n\in \mathbb{N}\}$. Every finite subset $T_0 \subseteq T$ is consistent by compactness and consistence of $T$, define $T'_0$ s.t. there is a $n_0$ s.t. for any $k \ge n_0$, $\psi_k(v_1, v_2) \not \in T_0$. For intance consider the loop that has a way from $v_1$ to $v_2$ with infinite knots between and one straigh passage in the other way around. This graph is model of $T'_0$. By compactness we know that if $T'$ were consistent then let $\mathcal{M}$ be a model of $T'$, ad this gives us the graph $G=(V, E)$ and two vertices $x, y$. They must be connected and must be not connected, $QED$.
### 2. Types, Elementary Things and Ultrathings
#### Theory
##### Filters and Ultrafilters
###### Def. of Filter
We define an infinite set $I$.
*Def.* A **filter** on $I$ is a set $\mathcal{F}$, such that $\mathcal{F} \subset \mathcal{P}(I)$, non-empty with:
1. $\emptyset \not \in \mathcal{F}$
2. $\forall_{A,B \in \mathcal{F}} A \cap B \in \mathcal{F}$
3. $\forall_{A,B \subseteq I}(A \in F \land A \subseteq B) \Rightarrow B \in \mathcal{F}$
Conditions 2. and 3. can be summerised in: $M \cap N \in \mathcal{F} \leftrightarrow M, N \in \mathcal{F}$.
*Def.* For a fixed $K \subseteq I$, a **principal filter** generated by $K$ is the family of all supersets.
- [ ] Superset
- [ ] Family
Excurus: Try to think at filters as ideals of the ring $(\mathcal{P}(I), \cap, \subseteq)$, closed under $\cap$ and checking all elements of $\mathcal{P}(I)$ for $\subseteq$.
**Lemma**: Every set with the FIP (finite intersection property) generates a filter (by closure under sueprsets). Also remember that any filter is contained in a ultrafilter, then a set with FIP is enough to build all up to an ultraproduct. This is used in the proof of the compactness theorem.
###### Examples
*Def.* $A$ is said **cofinite** iff. $\bar{A}$ is finite. Remember $\bar{A} := I \setminus A$ for a set $I$ s.t. $A \subset I$, $\bar{A}$ is called the **complement**.
- Given $i \in I$, we have a filter $\mathcal{F}_i = \{A\subseteq I: i \in A\}$.
- **Féchet Filter**, is the filter of the cofinite subsets of $I$: $\{A \subseteq I: I \setminus A \textit{ is finite}\}$.
- If $(I, <)$ is totally ordered, then the set supersets of non-empty final segments of $I$ is a filter. A final segment is a subset $A \subseteq B$ with $\forall_{i,j \in I}(i \in A \land j \ge i) \Rightarrow j\in A$
Given a subset $\mathcal{A} \subseteq T(I)$, we write: $FI(\mathcal{A}) = \{A_1 \cap ... \cap A_n n >0, A_1, ..., A_n \in \mathcal{A}\}$. and we say that $\mathcal{A}$ has the finite intersection property if $\emptyset \not \in FI(\mathcal{A})$.
- [ ] Understand filters on ordered sets
- [ ] Understand what the Féschet Filter is
- [ ] Understand the finite intersection property
- [ ] Summerise in these notes
###### Two Lemmas
**Lemma 1.** If $\mathcal{A} \subset \mathcal{P}(I)$ has the finite intersection property, then there is a filter $\mathcal{F}$ on $I$ with $\mathcal{A} \subseteq \mathcal{F}$
*Proof.* Define $\mathcal{F} := \{C\subseteq I : \exists_{B \in FI(\mathcal{A})} B\subseteq C\} \subseteq \mathcal{A}$.
*Claim.* $\mathcal{F}$ is a filter. I know $\emptyset \not \in \mathcal{F}$ by the finite interesection property, so the first point is done. If $c_1 c_2 \in \mathcal{F}$, $B_1, B_2 \in FI(\mathcal)$ with $B_1 \subseteq C_1$ and $B_2 \subseteq C_2$ then $B_1 \cap B_2 \in FI(\mathcal{A})$ is containted in $C_1 \cap C_2$, so $C_1 \cap C_2 \in \mathcal{F}$. Finally, if $C \in \mathcal{F}$, $B \in FI(\mathcal{A})$ such that $V \subseteq C$, and $C' \subseteq I$ is such that $C \subseteq C'$, then $B \subseteq C$ is $C' \in \mathcal{F}$.
**Lemma 2.** Let $\mathcal{F}$ be a filter and let $A \subseteq I$ with $\bar{A} \not \in \mathcal{F}$. Then $\mathcal{F}_A: \mathcal{F} \cup \{A \cap B \land B \subseteq I\}$ is a filter containing $\mathcal{F} \cup \{A\}$.
*Corollary:* $\mathcal{F} \cup \{A\}$ is contained is a finlter on $I$.
*Proof.* Assume for contradiction that $\emptyset \in \mathcal{F}_A$, so $\emptyset = A \cap B$ for some $B$. This means that  $B \subseteq \bar{A}$, but then $\bar{A} \in \mathcal{F}$ contradiction so $\emptyset \not \in \mathcal{F}_A$.
Given $C_1, C_2 \in \mathcal{A}$, let's examine the cases:
(i) $C_1, C_2 \in \mathcal{F}$, then $C_1 \cap C_2 \in \mathcal{F} \subseteq \mathcal{F}_A$
(ii) $C_1 \in \mathcal{F}, C_2 = A \cap B_2$, $B_2 \in \mathcal{F}$
(iii) $C_2 \in \mathcal{F}$
(iv) $C_1 \mathcal{A} B_1$, $C_2 = A \cap B$,   $B_0, B_2 \in \mathcal{F}$ then
$C_1 \cap C_2 = A \cap (B_1 \cap (B_2 \in \mathcal{F}_A$))
- [ ] Try to understand what sould the case iv be
###### Def. Ultrafilters & Ultraproducts
**Lemma (& Def.)**: A filter \mathcal{F} on $I$ following are equivalent
1. $\mathcal{F}$ is an ultrafilter
2. $\forall_{A,C \subseteq I} A \cup B \in \mathcal{F} \Rightarrow A \in \mathcal{F}$ or $B \in \mathcal{F}$ 
3. $\mathcal{F}$ is maximal among filters on $I$, i.e. it is not poperly contained in a filter on $I$
*Proof.* Assume that $\mathcal{F}$ is an ultrafilter, and let $A, B \subseteq I$ with $A \cup B \in \mathcal{F}$. Then $A \not \in \mathcal{F}$ , then $\bar{A} \in \mathcal{F}$. Let $\bar{A} \cap (A \cup B)=(\bar{A} \cap A) \cup (\bar{A}\cap B)$ is in $\mathcal{F}$. So $\bar{A} \cup B \subseteq B$ is in $\mathcal{F}$. So $1. \Rightarrow 2.$
Now assume that $\mathcal{F}$  satisfies 2., and let $\mathcal{F} \subseteq \mathcal{U}$ be a filter. Let $A \in \mathcal{U}$. We have $A \cup \bar{A} \in \mathcal{F}$ indeed $\mathcal{F}$ is non-empty by asssumption and given $B \in \mathcal{F}$, $A \cup \bar{A} \supseteq B$. So $A \in \mathcal{F}$ or $\bar{A} \in \mathcal{F}$, but the later option would imply that $\bar{A} \in \mathcal{U}$, so $A \cap \bar{A} = \emptyset \in \mathcal{U}$. Thus $A \in \mathcal{F}$. So $\mathcal{F} = \mathcal{U}$, hence $\mathcal{F}$ is minimal, so $2. \Rightarrow 3.$ Assume that $\mathcal{F}$ is minimal among ultrafilters on $I$. In particular for $A \subseteq I$ with $\bar{A} \not \in \mathcal{F}$ given a filter $\mathcal{F}_A$  on conianing $\mathcal{F} \cup \{A\}$, we have $\mathcal{F} = \mathcal{F}_A$, so $A \in \mathcal{F}$ this $\mathcal{F}$ is an ultrafilter. $QED.$
**Def**. form [Wikipedia](https://en.wikipedia.org/wiki/Ultrafilter?wprov=sfti1)
Every ultrafilter falls into exactly one of two categories: principal or free. A **principal** (or **fixed**, or **trivial**) ultrafilter is a filter containing a [least element](https://en.wikipedia.org/api/rest_v1/page/mobile-html/Least_element "Least element"). Consequently, principal ultrafilters are of the form ![{\displaystyle F_{a}=\{x:a\leq x\}}](https://wikimedia.org/api/rest_v1/media/math/render/svg/babc93072005c41ddc68ac2b7c5067e3f945dc1d) for some (but not all) elements ![a](https://wikimedia.org/api/rest_v1/media/math/render/svg/ffd2487510aa438433a2579450ab2b3d557e5edc) of the given poset. In this case ![a](https://wikimedia.org/api/rest_v1/media/math/render/svg/ffd2487510aa438433a2579450ab2b3d557e5edc) is called the _principal element_ of the ultrafilter. Any ultrafilter that is not principal is called a **free** (or **non-principal**) ultrafilter.

**Ex.** Given an $i \in I$, the filter $\mathcal{F}_i =\{A \subseteq I| i \in A\}$ is an ultrafilter on $I$, and we say that $\mathcal{F}_i$ is principal. An ultrafilter on $I$ is said free if it is not principal.
**Lemma**: A filter on $I$ is **free** iff it contains the Féchet Filter $\{A \subseteq I | \bar{A} \text{ is finite }\}$.
*Proof.* Say $\mathcal{F}$ contains the Fréchet filter, then for any distinct $i, j \in I$, we have $\{\bar{i}\}$ we have $\mathcal{F}_i \not = \mathcal{F}_j$, so $\mathcal{F}$ is free. Now assume that $\mathcal{F}$ is free. Let $A \subseteq I$ be cofinite, i.e. $\bar{A}$ is finite and we write $\bar{A}= \{i_1,..., i_n\}$ for $n \in \mathbb{N}$ and $i_1, ..., i_n \in I$. We want to show that $A \in \mathcal{F}$. Assume for contradiction that $A \not \in \mathcal{F}$. So $\bar{A} \in \mathcal{F}$. By the second characterisation of ultrafilters, we have: $\bar{A}= \{i_i\} \cup ... \cup \{i_n\} \in \mathcal{F} \Rightarrow \exists_{k \in \{i_1, ..., i_n\}}$ with $\{i_k\} \in \mathcal{F}$ (by induction). But then $\mathcal{F}_{i_k} \subseteq \mathcal{F}$ since $\mathcal{F}$ is a filter. We conclude since $\mathcal{F}_{i_k}$ is minimal that $\mathcal{F}_{i_k} = \mathcal{F}$. We get then contradiction. $QED.$
Let $\mathcal{L} = \langle (f_k)_{k \in K}, (R_j)_{j \in J}, C \rangle$ be a first order language. Let $(\mathcal{M}_i)_{i \in I}$ be a family of $\mathcal{L}$-*structures* and write $\mathcal{M}_i =(M_i,  (f_k)_{k \in K}, (R_j)_{j \in J}, (\lambda_{i,c})_{c \in C})$. We will define an equivalence relation on the Cartesian product $\prod_{i \in I} M_i = \{g: I \rightarrow \bigcup_{i \in I} n_i: g(i) \in M_i \text{ for each } i \in I\}$. Let $\mathcal{U}$ be an ultrafilter on $I$. We say that $(m_i)_{i \in I}$ and $(m'_i)_{i \in I}$ in $\prod_{i \in I}M_i$ are *equivalent modulo* $\mathcal{U}$ and we write $(m_i)_{i \in I} =_\mathcal{U} (m_i')_{i \in I}$ if the set $\{i \in I | m_i = m_i'\}$ lies in $\mathcal{U}$.
**Lemma**: This is an equivalence relation on $\prod_{i \in I} M_i$
*Proof.* Reflexivity: this is because $I \in \mathcal{U}$ (true for all filters). Simmetry: by symmetry of $=$. Transitivity: let $(m_i)_{i \in I} =_{\mathcal{U}} (m_i')_{i \in I}$ and $(m'_i)_{i \in I} =_{\mathcal{U}} (m_i'')_{i \in I}$. And let $A, B \in \mathcal{U}$ be witnesses, i.e. $\{i \in I: m_i = m_i'\}=A$ and $\{i \in I: m_i' = m_i''\}=B$. Then by transitivity of $=$ we have $m_i = m_i''$ for all $i \in A \cap B$, but $A \cap B \in \mathcal{F}$, since $(m_i)_{i \in I} =_{\mathcal{U}} (m_i'')_{i\in I}$. $QED.$
We write $\prod_{\mathcal{U}}$ with interpretation of symbols in the signature. We proceed as follows: For $k \in K$ and $m_1, ..., m_{\alpha k} \in \prod_{i \in I}M_i$, we define:$\underline{f_k}([m_1]_\mathcal{U},..., [m_{\alpha k}]_\mathcal{U}) := [(f_{i,k} (m_1(i),...,m_{\alpha k}(i))_{i \in I}]_\mathcal{U}.$ if $m_1', ..., m_{\alpha k}' are s.t. $([m_1']_\mathcal{U}, ..., [m_{\alpha k}'']_\mathcal{U})= ([m_1]_\mathcal{U}, ..., [m_{\alpha k}]_\mathcal{U})$, then for sets $A_1, ..., A_{\alpha k} \in \mathcal{U}$ witnessing each equivalence $m_1 =_\mathcal{U} m_1', ..., m_{\alpha k} =_\mathcal{U} m_{\alpha k}'$ we have that $A:= A_1 \cap ... \cap A_{\alpha k} \in \mathcal{U}$, and for each $i \in A$, $f_{i,k}(m_1(i), ..., m_{\alpha k}(i)) = f_{i,k}(m_1'(i), ..., m_{\alpha k}'(i))$ which means that $[(f_{i,k}(m_1(i), ..., m_{\alpha k}(i))_{i \in I}]_\mathcal{U} = f_{i, k}([m_1], ... [m_{\alpha k}])$.

###### Def. Ultrapowers
It basically just is an ultraproducts where all factors are the same structure $\mathcal{A}$. A corollary of the Łos theorem states that a the theory of an ultrapower of $\mathcal{A}$ is equal to the theory of $\mathcal{A}$. Every sentence that holds in $\mathcal{A}$ clearly holds also in every factor and therefore holds in the ultrapower too (this is what I tried to show to Pascal in the las week). This is trivial if the ultrafilter is principal.
##### Types, Elementary, Sk-Lö
**Definition**: Let $\mathcal{M}$ be an $\mathcal{L}$-structure, $A \subseteq M$ and $n \in \mathbb{N}$. An $n$-type of $\mathcal{M}$ over $A$ is a set $p(v_0, ..., v_n)$ of formulae in $\mathcal{L}_A$ with free variables among $v_0, ... , v_n$ s.t. for every finite subset $X$ of $p(v_0, ..., v_n)$, there is an elementary extension from $\mathcal{N}$ to $\mathcal{M}$ in $\mathcal{L}_A$ and a tuple $x_0, ..., x_n \in N$, s.t. $\mathcal{N} \models_{(\frac{v_0, ..., v_n}{x_0, ..., x_n})} \phi$ for all $\phi \in p(v_0, ... , v_n)$.
*Interpretazione*: Un type quindi è un insieme di formule che usano meno variabili di quelle che potrebbero inoltre esiste, dato un subset finito del type, una struttura in grado di soddisfarlo finitamente. Si tratta quindi di una nozione molto legata a quella di substructure. Lo si può anche definire come:
**Definition**: For $\bar{a} \in M^n$, the type of $\bar{a}$, $tp^{\mathcal{M}}(\bar{a}):= \{\phi(\bar{x})|\mathcal{M} \models \phi(\bar{a})\}$.
Those are then the set of all proposition that are satisfied by a constant $a$ in a given model $\mathcal{M}$.
**Definition**: An extension $\mathcal{M} \subseteq \mathcal{N}$ is **elementary** if for all $\bar{a} \in \bigcup_{n \in \omega}M^n$, $tp^{\mathcal{M}}(\bar{a}) = tp^{\mathcal{N}}(\bar{a})$. %%In particular remember that it is not true that $\mathcal{M} \models \phi \not \Rightarrow \mathcal{N} \models \phi$, but only the types on elements of $\mathcal{M}$ must remain the same.%%
**Ex**. Let $\mathcal{M} = (\omega, <)$ and $\mathcal{N} = (\{-1\}\cup \omega, <)$. Then the extension $\mathcal{M} \subseteq \mathcal{N}$ is not elementary since: $tp^{\mathcal{M}}(0) \not = tp^{\mathcal{N}}(0)$, for example we see $\phi(x) := \exists_y y < x$, we notice $\phi(x) \not \in tp^{\mathcal{M}}(0)$ and $\phi(x) \in tp^{\mathcal{N}}(0)$.
**Theorem**: Every infinite model has a proper elementary extension.
*Proof.* Let M be infinite, and let $T = Th(M,a)_{a\in M}$. Let c be a new constant, and let $T' =T\cup \{c \not=a |a\in M\}$. By the compactness theorem $T'$ has a model $\mathcal{N}$. Since $\mathcal{N} \models T, \mathcal{N}$ is an elementary extension of $\mathcal{M}$.
**Cor**: Every infinite model $\mathcal{M}$ has elementary extensions of arbitrary large cardinalities $> |M|$.
**Löwenheim-Skolem Theorem**: Let $\mathcal{N}$ be a model with at most countably many functions and constants. Then $\mathcal{N}$ has an elementary countable submodel.
**Ex**. $(\mathbb{R}, +, \times, 0, 1)$ has $2^{\aleph_0}$ countable real closed subfields. %%I'm unsure on this point%%
None of these extensions are elementary: $$(\mathbb{N},+,\times,0,1) \subseteq^1 (\mathbb{Z},+,\times,0,1) \subseteq^2 (\mathbb{Q},+,\times,0,1) \subseteq^3 (\mathbb{R},+,\times,0,1) \subseteq^4 (\mathbb{C},+,\times,0,1)$$We see that $1$ is not elementary since "there are elements before $0$" $2$ because of closure under inverse of $\times$, $3$ because of $\phi(x):= \exists_y y \times y= x$ and $4$ again because of $\phi(x)$.
**Theorem**: $\mathbb{N}$ , $\mathbb{Z}$  and $\mathbb{Q}$ have $2^{\aleph_0}$ countable elementary extensions. %%I suppose that these should be all those extensions with \omega with alle elements added and then \omega^\omega. they seem to be 2^{\aleph_0}. Obviously \omega_2 should not be one of those because it would then be uncountable.%%
%%I could continue with these kind of theorems from the slides on Elementary Extensions by Kossak, I stopped at slide 15/25.%%
**Definition**: A **nonstandard model of arithmetic** is a proper [elementary extension](https://ncatlab.org/nlab/show/elementary+extension) of the _standard model_ $(\mathbb{N},0,1,+,\times,S)$ of first-order [Peano arithmetic](https://ncatlab.org/nlab/show/Peano+arithmetic).
#### Similar Exercises
### 3. Quantifier Elimination and O-Minimality
#### Theory
##### Quantifier Elimination
Def. $\mathcal{A}$ first order theory $T$  eliminate quantifiers (or has quantifier elimination/QE) in $\mathcal{L}$ if for all formulae $\phi(v_0, ..., v_n)$ there is a quantifier free formulae $\psi(v_0, ..., v_{n-1})$ s.t. $T \models \forall_{v_0},... \forall_{v_{n-1}}(\phi(v_0, ..., v_{n-1}) \leftrightarrow \psi(v_0, ..., v_{n-1}))$ . 
In particular definable sets in models of $T$ are quantifier free definable.
Proposition. If $T$ is consistent and eliminates quantifiers then $T$ is complete.
Proof. Let $\mathcal{M}, \mathcal{N} \models T$ with $\mathcal{M} \subseteq \mathcal{N}$. Let $\phi(v_0, ..., v_{n-1})$ be a formula, let $h: Vbl \rightarrow M$. Let $\psi(v_0,..., v_{n-1})$ be a quantifier-free with $T \models \forall_{v_0}, ..., \forall_{v_{n-1}}(\phi(v_0, ..., v_{n-1}) \leftrightarrow \psi(v_0, ..., v_{n-1}))$.
We have $\mathcal{M} \models_h \phi \Leftrightarrow \mathcal{M} \models_h \phi \Leftrightarrow \mathcal{N} \models_h \psi \Leftrightarrow \mathcal{N} \models_h \phi$. See $\mathcal{M} \le \mathcal{N}$.
Lemma. Let $T$ be a first order theory. Assime that for alla quantifier-free formulae $\phi(v_0, .., v_{n-1})$, there is a quantifier-rfree formuala $\theta(v_0, ..., v_{n-1})$ s.t. $T \models \forall_{v_0}, ..., \forall_{v_{n-1}}(\theta(v_0, ..., v_{n-1})) \leftrightarrow \exists_{v_n}(\psi(v_0, ..., v_{v-1}))$. Then $T$ eliminates quantifiers.
(If we want to eliminate quandier we just have to eliminate one quantifier and also we jave to look only at one variable and then we can eliminate several varables. Quindi siamo fortunati che ci basta guardare ad un quantifier solo ed un avaribale sola, una volta fatto cosi lo abbiamo per tutti, ottimo risultato.)
Proof. By induction over complexity of $\phi(v_0, ..., v_{n-1})$, you show that there is a $\mu(v_0, ..., v_{n-1})$ quantifier-free, with $T \models \forall_{v_0}, ..., \forall_{v_{n-1}}(\phi(v_0, ..., v_{n-1}) \leftrightarrow \mu)v_0, ...., v_{n-1})$. Now distinguish cases:
- If $\phi$ is quantifier-free than just $\phi = \mu$
- Let $\phi_{0}(v_0, ..., v_{n-1}), \phi_1(v_0, ..., v_{n-1}), \mu_0(v_0, ..., v_{n-1}), \mu_1(v_0, ..., v_{n-1})$, where \mu_0, \mu_1 are quantifier-free and $T \models \forall_{v_0}, ..., \forall (\phi_i(v_0, ..., v_{n-1}) \leftrightarrow \mu_1,(v_0, ..., v_{n-1}))$ i= 0, 1.
- on the notes the rest
- [ ] Copy other notes from Notability
#### Similar Exercises



