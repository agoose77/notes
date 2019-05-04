Load this document in the Markdown viewer to enable macros.
$$
\gdef\dd{\mathop{}\!\mathrm{d}}
\gdef\em#1{\boldsymbol{#1}}
\gdef\quantity#1{{\left\{ #1 \right\}}}
\gdef\qty#1{{\left\{ #1 \right\}}}
\gdef\pqty#1{{\left( #1 \right)}}
\gdef\bqty#1{{\left[ #1 \right]}}
\gdef\vqty#1{{\left\vert #1 \right\vert}}
\gdef\Bqty#1{{\left\{ #1 \right\}}}
\gdef\absolutevalue#1{{\left\vert #1 \right\vert}}
\gdef\abs#1{{\left\vert #1 \right\vert}}
\gdef\norm#1{{\left\Vert #1 \right\Vert}}
\gdef\evaluated#1{{#1 \vert}}
\gdef\eval#1{{#1 \vert}}
\gdef\order#1{{\mathcal{O} \left( #1 \right)}}
\gdef\vb#1{{\boldsymbol{ #1 }}}
\gdef\vectorarrow#1{{\vec{\boldsymbol{ #1 }}}}
\gdef\va#1{{\vec{\boldsymbol{ #1 }}}}
\gdef\vectorunit#1{{{\boldsymbol{\hat{ #1 }}}}}
\gdef\vu#1{{{\boldsymbol{\hat{ #1 }}}}}
\gdef\Re#1{{\operatorname{Re} \left\{ #1 \right\}}}
\gdef\Im#1{{\operatorname{Im} \left\{ #1 \right\}}}
\gdef\qqtext#1{{\quad\text{ #1 }\quad}}
\gdef\qq#1{{\quad\text{ #1 }\quad}}
\gdef\ket#1{{\left\vert { #1 } \right\rangle}}
\gdef\bra#1{{\left\langle { #1} \right\vert}}
\gdef\expectationvalue#1{{\left\langle {#1 } \right\rangle}}
\gdef\expval#1{{\left\langle {#1 } \right\rangle}}
\gdef\ev#1{{\left\langle {#1 } \right\rangle}}
\gdef\commutator#1#2{{\left[ #1 , #2 \right]}}
\gdef\comm#1#2{{\left[ #1 , #2 \right]}}
\gdef\anticommutator#1#2{{\left\{ #1 , #2 \right\}}}
\gdef\acomm#1#2{{\left\{ #1 , #2 \right\}}}
\gdef\poissonbracket#1#2{{\left\{ #1 , #2 \right\}}}
\gdef\pb#1#2{{\left\{ #1 , #2 \right\}}}
\gdef\derivative#1#2{{\frac{\text{d}{ #1 }}{\text{d}{ #2 }}}}
\gdef\dv#1#2{{\frac{\dd {#1}}{\dd{ #2 }}}}
\gdef\partialderivative#1#2{{\frac{\partial{ #1 }}{\partial{ #2 }}}}
\gdef\pdv#1#2{{\frac{\partial{ #1 }}{\partial{ #2 }}}}
\gdef\functionalderivative#1#2{{\frac{\delta{ #1 }}{\delta{ #2 }}}}
\gdef\fdv#1#2{{\frac{\delta{ #1 }}{\delta{ #2 }}}}
\gdef\innerproduct#1#2{{\left\langle {#1},{ #2} \right\rangle}}
\gdef\ip#1#2{\innerproduct{#1}{#2}}
\gdef\braket#1#2{{\left\langle {#1} \mid { #2} \right\rangle}}
\gdef\outerproduct#1#2{{\left\vert { #1 } \right\rangle\left\langle { #2} \right\vert}}
\gdef\dyad#1#2{{\left\vert { #1 } \right\rangle\left\langle { #2} \right\vert}}
\gdef\ketbra#1#2{{\left\vert { #1 } \right\rangle\left\langle { #2} \right\vert}}
\gdef\op#1#2{{\left\vert { #1 } \right\rangle\left\langle { #2} \right\vert}}
\gdef\dotproduct{{\boldsymbol\cdot}}
\gdef\vdot{{\boldsymbol\cdot}}
\gdef\crossproduct{{\boldsymbol\times}}
\gdef\cross{{\boldsymbol\times}}
\gdef\cp{{\boldsymbol\times}}
\gdef\gradient{{\boldsymbol\nabla}}
\gdef\grad{{\boldsymbol\nabla}}
\gdef\divergence{{\grad\vdot}}
\gdef\div{{\grad\vdot}}
\gdef\curl{{\grad\cross}}
\gdef\laplacian{{\nabla^2}}
\gdef\tr{{\operatorname{tr}}}
\gdef\Tr{{\operatorname{Tr}}}
\gdef\rank{{\operatorname{rank}}}
\gdef\erf{{\operatorname{erf}}}
\gdef\Res{{\operatorname{Res}}}
\gdef\principalvalue{{\mathcal{P}}}
\gdef\pv{{\mathcal{P}}}
\gdef\PV{{\operatorname{P.V.}}}
\gdef\qcomma{{\text{,}\quad}}
\gdef\qc{{\text{,}\quad}}
\gdef\qcc{{\quad\text{c.c.}\quad}}
\gdef\qif{{\quad\text{if}\quad}}
\gdef\qthen{{\quad\text{then}\quad}}
\gdef\qelse{{\quad\text{else}\quad}}
\gdef\qotherwise{{\quad\text{otherwise}\quad}}
\gdef\qunless{{\quad\text{unless}\quad}}
\gdef\qgiven{{\quad\text{given}\quad}}
\gdef\qusing{{\quad\text{using}\quad}}
\gdef\qassume{{\quad\text{assume}\quad}}
\gdef\qsince{{\quad\text{since}\quad}}
\gdef\qlet{{\quad\text{let}\quad}}
\gdef\qfor{{\quad\text{for}\quad}}
\gdef\qall{{\quad\text{all}\quad}}
\gdef\qeven{{\quad\text{even}\quad}}
\gdef\qodd{{\quad\text{odd}\quad}}
\gdef\qinteger{{\quad\text{integer}\quad}}
\gdef\qand{{\quad\text{and}\quad}}
\gdef\qor{{\quad\text{or}\quad}}
\gdef\qas{{\quad\text{as}\quad}}
\gdef\qin{{\quad\text{in}\quad}}
\gdef\variation{{\delta}}
\gdef\var{{\delta}}
\gdef\matrixelement#1#2#3{{\left\langle{ #1 }\right\vert{ #2 }\left\vert{#3}\right\rangle}}
\gdef\matrixel#1#2#3{{\left\langle{ #1 }\right\vert{ #2 }\left\vert{#3}\right\rangle}}
\gdef\mel#1#2#3{{\left\langle{ #1 }\right\vert{ #2 }\left\vert{#3}\right\rangle}}
$$
<!-- Custom Macros-->
$$
\gdef\mleftright#1#2#3{\mathopen{}\mathclose{\left#1#2\right#3}}
\gdef\set#1{\left\{\,#1\,\right\}}
\gdef\qed{\blacksquare}
\gdef\atom#1#2{{}^{#1}\text{#2}}
\gdef\nucleus#1#2#3{{}_{#1}^{#2}\text{#3}}
\gdef\barn{b}
\gdef\unit#1{\operatorname{#1}}
\gdef\amu{u}
\gdef\MeV{\operatorname{MeV}}
\gdef\keV{\operatorname{MeV}}
\gdef\eV{\operatorname{eV}}
$$
<!-- QM -->
$$
\gdef\y{\hat{y}}
\gdef\x{\hat{x}}
\gdef\z{\hat{z}}
\gdef\p{\hat{p}}
\gdef\L{\hat{L}}
\gdef\J{\hat{J}}
\gdef\S{\hat{S}}
$$
<!-- algebra -->
$$
\gdef\comp#1#2{#1\circ#2}
$$

<!-- Style notes
\colon should be used for linear maps
: should be used for "where", e.g. $x : x \in V$
-->