I sent this LaTeX to [[L. Horsten]] in response to some quoted remarks he made in the course of [[KK2]] at the beginning of the [[Second Semester]] at the [[University of Constance]].
In response I got the following:
"Dear Simone,
\[...\]
Later on in the course we’ll see that there may be cases of a person who, even though she knows $p$, would answer No if she were asked “do you know p”? It is related to the question whether the principles "Kp -> KKp" and not" K p -> K not K p” are logical laws governing the concept of knowledge.
(Certanly bring up your proposal in the tutorial!)
with best wishes,
Leon"

``` latex
\documentclass{article}
\usepackage{amsthm}
\usepackage{csquotes}
\usepackage{setspace}
\usepackage[greek,english]{babel}
\usepackage[letterpaper,top=2cm,bottom=2cm,left=3cm,right=3cm,marginparwidth=1.75cm]{geometry}
\usepackage{graphicx}
\usepackage[colorlinks=true, allcolors=blue]{hyperref}

\title{A Brief Attempt to Define Knwoledge}
\author{Simone Testino}
\date{April 2023}
\begin{document}
\maketitle

\section{The Unappreciated Methodology}
The methodology expressed in class used to formalise the conception we commonly have on knowledge is the same, as exposed in the lecture, used by Newton while using the idea of force in his axioms without ever defining it. Similar is the case of Euclidean Geometry, where the concept of point has no definition even though it plays a crucial role in every axiom. Similar to these are also some conceptions of cause and effect which are present in various axioms, though without ever giving a definition of them.\\
Generally, I have an antipathy towards this procedure for formalising concepts we have in our head and which cannot be better conceived (yet?). I also think that many would share the opinion that deciding to avoid giving any express definition of knowledge, point, force or cause doesn’t particularly enrich the discourse and instead should be considered as the very last option. Even when such definitions are commonly avoided and one manages to get the desired results by axiomatic systems which don’t include any definition of such concepts, then it should always be welcomed any attempt to define the yet undefined term.\\

\section{The Attempt}
If you ask a yes/no question to somebody you might always also get a third answer “I don’t know”, I define knowledge as being the only predicate for which it holds that if I ask “K($\phi$)?” the answer can only be \enquote{yes} or \enquote{no}, \emph{tertium non datur}. When I claim that every question that is not of the form \enquote{Do you know $\phi$?} must have a third answer, I am not claiming more than what cartesian scepticism does: every time I ask you a different question, you might think about a certain devil deceiving all your perception; then you might be convinced that, no matter how simple the question is, you don’t anymore know if it’s true or false. But then, if I happen to ask you if \emph{you know or not} the answer, you’ll surely respond to me clearly, either \enquote{yes} or \enquote{no}.\\

\section{Problems}
\subsection{On Clear Sentences}
I just made two important assumptions when considering the question \enquote{Do you know $\phi$} : (i) the subject has clear what \enquote{do you know} means and (ii) the subject has clear what \enquote{$\phi$} means. One might argue that if both the predicate and the argument mustn’t be in any sense vague or ambiguous, then on every predicate the subject should give a binary answer. Though, such an answer, the subject might realise, could be deceived by the famous devil, and therefore drive the subject unto uncertainty. This surely holds if our source of knowledge is experience but it clearly holds also if we’re talking about logical truths, since many and many of those are doubted in modern debates (statements like $\lnot(A \land \lnot A)$ might be some puntual exceptions, though it doesn’t constitute a problem, since such statements are surely very finitely countable and shall be excluded from our definition of $K$, this is the topic of the next subsection).

\subsection{On Other such Predicates}
One might also argue that some other predicates like \enquote{I want $x$} might also never give us an “I don’t know” as an answer, or similarly \enquote{I perceive $\phi$}. I guess though that between the predicate of knowledge and of will one might simply draw a simple distinction on the domain, I know sentences, I want events. On perception, it is not that absurd to consider the predicate of \enquote{I perceive $\phi$} as being a subset of \enquote{I know $\phi$}.

\end{document}
````