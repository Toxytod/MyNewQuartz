## Talk with Pascal
After a chat with [[P. Wagner]] on the [[Continuum Hypothesis]] as in his Master Thesis at the [[University of Constance]] I wrote this short list of questions in order to understand more and ask him a question that might need to come before any answer to his central question. This clearly is connected with [[Advanced Set Theory (Lecture)]], the idea, Pascal told me, is originally by [[L. Horsten]]. I wrote and sent it in the evening after we talked, on [[13.07.2023]] just after I finished that exercise
### To Pascal
If I understood correctly, your aim is to calculate the amount of countable models of ZFC where CH is true so that you can divide this number with the full amount of countable models of ZFC and get how probable it is that CH is true. For simplicity, say what you are computing is a function in respect to a theory of a certain formula, so $f_{ZFC}(CH)$. Say that the codomain of $f_{ZFC}$ is the real interval $[0,1]$ where $f_T(\phi) = 1 \Leftrightarrow T \models \phi$ and $f_T(\phi) = 0 \Leftrightarrow T \models \lnot \phi$
_Question. 1_ 
  If I remember correctly you told me that there are $\aleph_1$ many countable models of ZFC, is it true even if you are considering only those models that satisfy either CH or $\lnot$CH? I suppose that, in order to tell how probable it is that CH is true you want to consider only those models where CH is either satisfied or its negation is.
  
Now when thinking about this the first difficulty I encounter is how to interpret a result like in "70% of the models CH is true and in the rest it’s false". Therefore, before thinking of how to compute such a probability I would first try to imagine which results can I expect from my computations, the claim that comes most intuitive to me is the following:
**Claim 1**. Given a theory $T$ and an _atomic_ formula $\phi$ s.t. $T \not \models \phi$ and $T \not \models \lnot \phi$, then 
$$\text{lim}_{\epsilon \rightarrow 0}f_T(\phi) \in \{0, \epsilon,0.5, 0.5\pm \epsilon, 1-\epsilon, 1\}$$
I decided to choose $\phi$ to be atomic, otherwise it is clear to me how for $\phi = \phi_1 \land \phi_2$ you could quickly get results that are out of the presented set by, e.g. I see it as an easy application of multi valued logic with truth values in the real interval $[0,1]$.
I also decided to include the limits with $\epsilon$ since I can imagine cases where you have a couple of models where $\phi$ is false but it is true in infinitely many others (or you have a infinities of different sizes compared); I can also imagine cases, as we talked about CH, where you get 50% probability.
*Question 2.*
	Do you share my intuition? Do you know a proof or a disproof of this claim?

In order to understand what would actually be the case if I were wrong, I tried to be creative and make an analogy. Say our theory $T$ are the ten commandments and our $\phi$ is "I can't harm an animal for no purpose", and we say, hoping that no theologist will contradict me, that $T \not \models \phi$. In this case it is very clear to me that $f_T(\phi)$ may well be around 80%, not infinitesimally less than 100% but also not strictly 50%. The argument here would be that clearly the ten commandments should be _less modified_ in order to get them to prove $\phi$ than to prove $\lnot \phi$.
*Question 3.*
	Do you follow my reasoning? Do you believe that that percentage should similarly show how much we need to modify a theory in order to get it to prove $\phi$?

### Answer