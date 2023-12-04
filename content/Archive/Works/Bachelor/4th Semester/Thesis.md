The following project will be the core of both my thesis in both the BSc in Mathematics and BA in Philosophy. The main claim is philosophical though most of the argument has a mathematical nature using concepts mostly of Model Theory and Set Theory.
For further details on the project read [[Thesis#Appendix]].
###### Abstract
I begin giving arguments for two ground assumptions: first that possible worlds, to some extent, are real and second, that possible worlds share the same structure as mathematical models. One must then conclude that mathematical constructions, like ultraproducts, on possible worlds must be real to the same extent as possible worlds are. I then analyse the structure of some ultraproducts and conclude with the existence of bizarre possible worlds. The choice whether this argument shall be considered as a proof ad absurdum against the two assumptions or some concrete results on the nature of possible worlds remains to the reader.
#### Mathematical Grounding
In this section I expose results on ultraproducts of various sorts which will be essential in the philosophical argument. For each of these structures I first expose the intuition and then analyse them in detail in the respective documents. Before reading the constructions of the ultraproducts or if some notation is unclear, please give a look to [[Notation.pdf]].
I expect to edit and delete some of the present construction, and add new ones as times goes on and intuition come, therefore the following are to be considered as the very first constructions
##### Colour Ultraproduct
The colouring ultraproduct has two main features: its ultrafilter is non-principal and any two models in the sequence differ only in the mapping of a function of the form $f: \{c\} \rightarrow D$ for $c$ a constant and $D$ an infinite set. The name derives from the easy-to-picture example where $f$ is the function mapping an object to its colour. The question begging for a mathematical proof is what is the colour of that object in the ultraproduct of that sequence of models?
On one hand $c$ must have a colour (since it has one in every model of the sequence), on the other hand  it cannot have a specific colour, since that would be true for one model in the sequence only (by non-principality of the ultrafilter and Łos Theorem, that cannot be the case).
Here I first analyse the mathematical structure of the ultraproduct and then point to philosophical consequences of considering such an ultraproduct on possible worlds.
This ultraproduct has a similar structure to $\prod_{p \in \mathbb{P}} \overline{\mathbb{F}_p}/\mathcal{U}$, where the colour function is the characteristic of the field (see more [here](https://grossack.site/2021/12/05/ultraproducts-howto.html)).

![[Colour_Ultraproducts.pdf]]

##### Mirror Ultraproduct

What do a mathematician at work and a kid playing a videogame have in common? Perhaps the fact that both are creating some worlds *inside* the actual one. Consider the notion of a subworld as being a set of complete and consistent sentences listed inside another world. One might see the actual world as being a proper metaphysical world and the videogame as a linguistic construction, a mathematical model. Though, since we are considering possible worlds as being nothing formalised into mathematical models (see: [[Thesis#Possible Worlds as Mathematical Models]]), the video game and the actual world are of the same sort. Furthermore since we are assuming modal realism (see [[Thesis#Modal Realism]]) the video game is in no way less real than the actual world. We might then ask, is it possible to have a videogame just like the actual world? Better said, is it possible to have a possible world that contains itself?
Directly defining a model that contains itself clearly ends in circularity issues hence, to give a positive answer to the question, ultraproducts might help.

![[Mirror_Ultraproduct.pdf]]
##### Co-Ultraproduct
Couldn't we define a world where all the opposite of what it is holds? Clearly, this would give rise to some internal contradictions (see [Impossible Worlds](https://plato.stanford.edu/entries/impossible-worlds/)), we could in fact not call a world possible where tautologies are negated. On the other hand, there certainly are some propositions that can be negated, I want therefore to construct an ultraproduct that negates all that can be negated of another ultraproduct, in a word: its opposite.

![[Co_Ultraproduct.pdf]]
#### Philosophical Grounding
There are two main assumptions that are required for my argument, here I give a more precise statement of both and show the content that will be part of the thesis.
##### Possible Worlds as Mathematical Models
I follow from the Tarskian definition of truth the necessity of considering possible worlds as mathematical models. This argument will be expanded in [[On Models and Worlds]], the essay for the course on Philosophy of Logic, and a revisited version will be added below.
###### Abstract
The Tarskian definition of logical consequence requires us to consider models within the same formal system of any proposition that we want to prove true. I then expose how the Tarskian Truth definition applied to any sort of empirical sentence requires an analysis of the formal system of possible worlds, considered as models. I then state the question asking which formal language should be regarded as the right one to talk about worlds, and then show the connection with the literature on logical pluralism.
##### On Models and Worlds

![[PDF]]
##### Modal Realism
For this I will mainly refer to [SEP](https://plato.stanford.edu/entries/david-lewis/#6) Section 6, I plan to only expose the Lewis' argument and show compatibility with [[Thesis#Possible Worlds as Mathematical Models]], in order to show that I use the same definition of possible worlds in these two arguments.
### Appendix
In the appendix I upload details of any sort regarding the thesis, divided in those regarding the actual content and the relevant bureaucratic informations.
##### Appendix Index
- Bureaucracy 
	- [[Thesis#Official Submission Form]]: actual submission form for BSc. and BA
	- [[Thesis#Time Table]]: detailed time table, tasks list and what will be uploaded
- Content
	- [[Thesis#Material]]: possible future references of the thesis
#### Official Submission Form
Since I want to submit the thesis for both the BSc. Mathematics and the BA Philosophy, I need to split it into two different documents which will be connected by many references. The version uploaded under [[Thesis#Thesis]] is therefore **not** the one that will be officially submitted, the content will be the same but split into two disjoint documents which will share no more than references. The documents I will submit can be found here:
#### Material
Here I list some of the material I plan to use to write the thesis.
##### Books
- Models and Ultraproducts, J. L. Bell, A. B. 
- Philosophy and Model Theory, T. Button, S. Walsh
##### Articles
###### On Interpretation of the World
- Horsten, L. (2021). _Having an Interpretation_ [PDF](https://www.philosophie.uni-konstanz.de/securedl/sdl-eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJpYXQiOjE3MDE0NDA2MTksImV4cCI6MTcwMjEzMTgxOSwidXNlciI6MCwiZ3JvdXBzIjpbMCwtMV0sImZpbGUiOiJmaWxlYWRtaW4vcGhpbG9zb3BoaWUvYWctaG9yc3Rlbi9QdWJsaWNhdGlvbnNfTGVvbi9Ib3JzdGVuMjAxMF9IYXZpbmdhbkludGVycHJldGF0aW9uLnBkZiIsInBhZ2UiOjEwODcwNX0.dqyhYTONNT2-jgZ8CFCOhLIqDWKySxOWtNKdWcnFAsM/Horsten2010_HavinganInterpretation.pdf)
- van Fraassen, B. (2008). Scientific representation: Paradoxes of perspective. Oxford: Oxford University Press.
###### On Semantic View
- Kokoszyńska, M. (1977). On the difference between deductive and non-deductive science. In Przełęcki, M. and Wójcicki, R., editors, _Twenty-Five Years of Logical Methodology in Poland_, pages 201–231. 
- Putnam, H. (1980). Models and reality. _The Journal of Symbolic Logic_, 45(3):464–482.
- Van Fraassen, B. C. (1980). To save the phenomena. In _The Scientific Image_, pages 41–69. Clarendon Press.- Da Costa, N. C. A. and Chuaqui, R. (1988). On Suppes’ set theoretical predicates. _Erkenntnis_, 29(1):95–112.
- Ruetsche, L. (2011). Exegesis saves. In _Interpreting Quantum Theories_, pages 1–18. Oxford University Press.
- Winther, R. G. (2020). The Structure of Scientific Theories. In Zalta. E. N., editor, _The Stanford Encyclopedia of Philosophy_, [SEP](https://plato.stanford.edu/archives/spr2021/entries/structure-scientific-theories/).
- Halvorson, H. (2013). The semantic view, if plausible, is syntactic. _Philosophy of Science_, 80(3), 475-478.
#### Time Table
The time dividing now (December 2023) from the submission date (August 2024) can be divided into three areas:
##### Third Semester
The high amount of courses (see [[3rd Semester]]) prevents me to work at any intensity at the thesis even, therefore, instead of doing the more time-consuming tasks like consulting the material (see [[Thesis#Material]]), I focus on finding the two right supervisors (see [[Thesis#Supervisors]]). That means that I am focusing on finding the right topic for my thesis and writing questions which I discuss with professors in the field.
##### Break
During the break I will have more time though I will not be able to discuss the material and ideas with the supervisors, therefore I want to have as many technical (hence mathematical) details cleared as possible. In this way I will spend the break on the more philosophical part of the material (see [[Thesis#Material]]) and want to write the introduction.
###### Tasks List
- Write the introduction
- Formalise the previously stated claims
- Begin to prove those formally, collect questions
##### Fourth Semester
During the fourth semester I foresee having fewer courses than in the third semester (see [[4th Semester]]) and will therefore spend most of it working on the thesis.