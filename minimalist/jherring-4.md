---
title: Grammar Construction in the Minimalist Program — Chapter 4 — Implementation
layout: page
---


[Back](jherring-3) — [Forth](jherring-5)

# <span id="anchor-50"></span>Chapter 4 — Implementation

## <span id="anchor-51"></span><span id="anchor-52"></span><span id="anchor-53"></span>Purpose

As noted in the introductory chapter, the Minimalist Program lives in a
kind of purgatory between theory and program. In principle, it is
nothing more than a set of research guidelines for a particular domain
of study we might term “Cognitive Linguistics.” In practice, for reasons
both conceptual and historical, it is somewhat more than that.

Conceptually, its foundational texts (Chomsky 1993; Chomsky 1995)
present a rationale for its approach that is grounded in a particular
(architectural) model about the position language occupies in the human
cognitive system. However abstract, and no matter that it demurs from
making concrete predictions about how language is *actually *situated in
the brain, it is a model notwithstanding and as such constrains the
range of objects and mechanisms that researchers working in the
Minimalist Program are likely to propose in their theories.
Historically, it is grounded in, and largely a rethinking of, previous
work in *Government and Binding Theory*. This likewise strongly informs
the range of topics that Minimalist researchers concern themselves with.

If Minimalism is not strictly a theory, calling it a “program” can
sometimes feel like a technicality. It seems to actually be somewhere in
between: too specific to be a program, but not constrained enough to be
a theory. It would be more accurate to say that it is *aiming *at a
particular theory that cannot yet be tested, given the nature of the
domain it studies and the current level of technology available for
observing objects in that domain. All that can be done for now is to try
to imagine what the Human Language Faculty would look like if the theory
were true, and then try to fit the lingusitic phenomena we observe to
that hypothetical set of machinery. It is believed that successes and
failures are equally informative in this enterprise: successes in
advancing understanding of what it would mean for the theory to be true,
and failures in learning where reality is likely to deviate from the
theory. “Is likely” is used advisedly: in the strange paradigm
Minimalism operates under, where conjectures can be lent credence by
data but never properly verified, a failure to fit data to the target
theory can as easily mean an *actual *deviation from a “perfectly
designed” language faculty as a misconception on the part of the
researcher about what “perfect” would mean in this domain.

In an important sense, what Minimalism is doing is reverse engineering
the brain. It looks at “output” (at least, a certain domain of “output”)
and tries to imagine how the machine that produced it would have to be
constituted to get just this range of data. “How the machine is
constituted” can be almost arbitrarily abstract. The Minimalist
researcher need not concern himself with the actual neural mechanisms of
human language — indeed, it would be misleading to do
so<sup>\[29\]</sup>. It’s more a question of high-level understanding.
Even so, there is no better proof of understanding than the ability to
make it concrete, and there would be no better test of Minimalist
success than the ability to build a machine that produces exactly the
same output, if not necessarily in exactly the same way. The purpose of
this project is to take the first steps toward building a toolkit that
allows researchers to do exactly that.

## <span id="anchor-54"></span><span id="anchor-55"></span><span id="anchor-56"></span>Introduction

The previous two chapters gave a necessarily cursory survey of
conceptual/explanatory machinery that is in popular use in the
Minimalist program and would be available in any<sup>
</sup>grammar-building toolkit if it is to be useful to researchers. As
this project develops, more mechanisms may be added. The ones
represented for now are chosen to achieve maximal coverage of theories
currently popular in the literature. The following sections give a
survey of how they are represented in the system and how researchers
would go about assembling testing environments for their individual
theories out of them.

## <span id="anchor-57"></span><span id="anchor-58"></span><span id="anchor-59"></span>Alternate Systems

Before getting into that, however, it would be remiss not to mention
alternate approaches to this problem. Broadly speaking, there seem to be
two.

### <span id="anchor-60"></span>**Minimalist Program Grammar Implementation**

The *Minimalist Program Grammar Implementation *of (Fong and Ginsburg in
preparation) is the closest in spirit to this project. Like this one, it
is primarily concerned with building a publicly-available system that
people can actually use in their research. Like this one, it considers
computational implementation the “proof in the pudding” — a (minimalist)
theory is on the right track to the extent that it *verifiably *produces
linguistic output consistent with people’s actual intuitions. Like this
one, it is a perpetual work in progress, starting by implementing the
core mechanisms that underly most or all minimalist theories and
expanding from there. And like this one, it seems to have identified
**Agree **and its implementations as the prime computational engine and
locus of difference between various minimalist theories. The most recent
work by researchers associated with this project seeks to provide a full
accounting for and implementation of **Probe**-**Goal **agree systems.

It departs from this system in being focused on efficiency and parsing.
Where this project aims to be a grammar-building toolkit that
researchers can use to test their theories against a common database of
example sentences, Fong and Ginsburg’s system seems more focused on
building an industry-applicable parser. For this reason, the focus is
more on efficiency than range of coverage. The system is grounded in
Minimalist research out of a concern for cognitive linguistic accuracy
(over and above mere machine usability), but it still wants its accurate
results in a manner that is maximally efficient for silicon processors.
As a consequence, there is a different principle guiding the choice of
implementational mechanisms, and it is aimed at a different class of
users with a different class of concerns. Practically speaking, this
means it offers a more limited range of implementational mechanisms.
Where this system aims to offer an API\[30\]<sup> </sup>of known
grammatical mechanisms, the *Minimalist Program  Grammar Implementation
*settles on a more specific version of Minimalism that it believes to be
correct, at least in terms of parsing efficiency.

### <span id="anchor-61"></span>Minimalist Grammars

The *Minimalist Grammars *approach of (Stabler 2001) and (Harkema 2001)
is somewhat more removed from this project. Whereas this project and the
*Minimalist Program Grammar Implementation *are concerned with tool
building, the *Minimalist Grammars *project is a research program in its
own right.

*Minimalist Grammars *are rigorous formalizations of a subset of the
theoretical mechanisms<sup> </sup>proposed under the Minimalist rubric.
No attempt is made to formalize the entire field — rather, those
mechanisms are chosen which lend themselves to formalization (and which
are in common enough use to plausibly be called “core” operations), and
they are given formal grounding. This is done in the hope that it makes
the Minimalist Program easier to reason about. To the extent that such
formalizations aid the creation of Minimalist tools, this is of course
viewed as a success, but it is also not the main point. The main point
is to give Minimalist conjecture theoretical footing so that it can be
reasoned about like a theory. One might say that this approach is more
concerned with depth than breadth.

## <span id="anchor-62"></span><span id="anchor-63"></span><span id="anchor-64"></span>Object and Mechanisms

This project takes as its inspiration the LKB (Linguistic Knowledge
Builder) system of (Copestake 2002) and its associated English Resource
Grammar (Copestake and Flickinger 2000; Flickinger, Bender, and Oepen
2014). Its aim is to build an analogous system for Minimalism. In an
important sense, this goal is unattainable — for where “unification
grammars” are a formalism, Minimalism is merely a research program.
Unlike with *Head-Driven Phrase Structure Grammar (HPSG) — *the research
paradigm targeted by the LKB — there is no authoritative Minimalist
guidebook one can look to for the core mechanisms. The best one can do
is to read the prominent papers in the field and mimic their systems
computationally. In what follows, these core objects and mechanisms are
distilled from those presented in the overview given by the previous two
chapters.

### <span id="anchor-65"></span>Lexical Features

(Chomsky 1995), and nearly all subsequent work, conceives of Lexical
Items — the atoms of a derivation — as bundles of linguistic features.
Any grammar implementation in Minimalism must therefore begin by laying
out the inventory of features that will be used. In an important sense,
Lexical Features are the primitives of any minimalist grammar.

This implementation represents lexical features with a class
***feature***. ***feature***s are defined by:

**Category **The class to which a feature belongs. This governs to a
large degree what features it can interact with.

**Polarity **Features in Minimalism come in paired oppositions. For each
category, there are two classes of instantiation.<sup>\[31\]</sup>

**Value **Features have values (or don’t). It will be assumed here that
all features are *potentially *valued in the sense that all features
come with a place to store a value. Whether or not a value can be
transmitted or received for a given feature is a degree of freedom in
the system.

In the current implementation, this is associated with a paricular
machine-readable notation that is standard in the literature:

*polarityCATEGORY *\[*value*\]

*Polarity *is a lower-case letter — usually *u *or
*i*<sup>*\[32\]*</sup>.

*Category *is string of letters at least the initial of which is
upper-case.

*Value *is a string and is enclosed in brackets. An *unvalued *feature
marks its status by having the empty string between the brackets.

Examples of possible representations include:

**A valued (accusative) case feature**: *uK*\[*ACC*\]

**An unvalued ***φ ***feature**: *uφ*\[\]

**An (inherently-)valued ***φ ***feature**: *iφ*\[3*sg*\]

### <span id="anchor-66"></span>Lexical Feature Specification File

The range of features allowed for a given grammar is laid out in a
user-defined ***feature specification file***.

To capture the insights in (Preminger 2014), (Nevins 2007) and (McGinnis
2005), among others, this file is arranged in a *feature geometry*. The
file should be in JSON (Bray 2014) format and should be represented as a
single root object. Categories are arranged hierarchically as the keys
of objects both at the root level and of objects nested inside other
objects. The value associated with a category key is either itself an
object keyed by category, or it is a ***specification object***. A
***specification object ***is an object with a single key: ***value***.
***value ***is typically a list of ***string***s. A category definition
embedded in another category definition is a *specification *for the
purposes of standard feature unification algorithms such as those used
in HPSG (see that have largely been replaced by *valued *and *unvalued*.

(Sag, Wasow, and Bender 2003)). The format of ***feature specification
file***s is best thought of as a tree that represents a *feature
geometry *(a la (Clements 1985)), with ***value ***arrays as a shorthand
method for spelling out the leaves/terminals.

An example ***feature specification file ***is shown below:

***\{***

***"Syn": \{***

***"Phi": \{***

***"Person": \{***

***"value": \["1", "2", "3"\]***

***\},***

***"Number": \{***

***"value": \["sg", "pl"\]***

***\}***

***\},***

***"Case": \{***

***"values": \["ACC", "NOM", "DAT", ...\]***

***\},***

***"Selection": \{***

***...***

***\}***

***\}***

***\}***

One thing that might stand out about this example file is that ***Person
***and ***Number ***are separate features, begging the question of how
one implements the *φ *probes popular in the literature. This is done
for compatibility with analyses like (Preminger 2014) and (Béjar and
Rezac 2003) in which these features are treated separately, but of
course it is up to the researcher-user to make these kinds of decisions
in the space the system allows. It is of course possible to collapse
them into a single *φ *category by replacing the implementation object
for “Phi” in the file above with a ***specification object ***that is
the concatenated powerset of the two ***value ***arrays, like so:

***\{ ... ,***

***"Phi": \{***

***"value": \["1sg", "2sg", "3sg", "1pl", ...\]***

***\}***

***\}***

Shortcut Values

To save space and tedium in ***feature specification file***s, the
system provides two shortcut values that stand in for a range of things
that could have been added to the feature geometry to acheive certain
effects. These are **wildcard **(\*) and **sink **(\#). **wildcard
**automatically matches any value, including **category
**specifications. **sink **automatically *fails *to match (is
automatically *distinct from *any match, technically). These are meant
to cover situations where achieving certain effects requires a large
number of single-use entries at every point in the hierarchy. So, for
example, implementing a *barrier feature *to block any probe is normally
a lot of work, because it requires entering a special-use “stop value” —
a value that represents no linguistic specification — as a leaf of every
category branch in the hierarchy. Repurposing

the earlier ***feature specification file ***example, to implement a
head that blocks all Case and *φ *probes, one might do something like
this:

***\{***

***"Syn": \{***

***"Phi": \{***

***"Person": \{***

***"value": \["1", "2", "3", "\#"\]***

***\},***

***"Number": \{***

***"value": \["sg", "pl", "\#"\]***

***\}***

***\},***

***"Case": \{***

***"values": \["ACC", "NOM", "DAT", "\#"\]***

***\}***

***\}***

***\}***

And then, on the head in question, there would have to be “sink”
features — like so: *iCase*\[\#\]*, iP erson*\[\#\]*, iNumber*\[\#\].
This guarantees that any probe of these categories will match and meet
with failure, since the sink feature is meaningless, but the probe is
technically now valued and thus inactive. Suppose instead one wanted to
block *all *probes (as is true at phase boundaries, for example — see
chapter 2). In that case the shortcuts save a lot of typing. The
“barrier feature,” to coin a term, is just *i*\[\#\]. It matches any
category and transmits a useless value.<sup>\[33\]</sup>

As a sidenote, any applicability of the *barrier *feature to systems
like (Chomsky 1986a) is not a mere coincidence. It has been widely noted
that Minimalist *phases *capture a lot of the same intuitions, and the
shortcuts were added to the system precisely to make *phases *easier to
implement without having to build them in as primitives. The name
reflects this heritage.

### <span id="anchor-67"></span>Lexical Item

A ***lexical item ***is nothing more than a selection of features
(Chomsky 1995). Ideally, then, ***lexical item***s in this system would
just be arrays of features. For implementational convenience, they are a
bit more articulated than that in the present system. ***lexical items
***consist of:

**Tag **a string that uniquely identifies the item<sup>\[34\]</sup>. No
two items in a lexicon may have the same ***tag***.

**Phon **a string representation of phonological features

**Syn **a set of syntactic ***lexical features***

**Sem **a string representing a semantic denotation (if any)

***Syn ***consists of features in the sense of ***lexical features
***defined above. At the time of writing, ***Phon ***and ***Sem ***are
not fleshed out. **SpellOut **in the present system is just string<sup>
</sup>concatenation, so ***Phon ***for lexical items is its surface
string. It remains for future work to articulate this further (see
(Herring 2009) for a preview). ***Sem ***is also not articulated at the
time of writing, but the intention is to leave this largely to user
implementation. More details are given in later sections, but the system
includes “attachment points” at which a user-defined semantic
implementation can be “plugged in.” To delegate maximal responsibility
to the external semantic system, semantic features are currently
expected to be strings. These strings can represent whatever objects the
semantic plugin understands, and it is the responsibility of the plugin
to parse and assemble them. It is anticipated that in the general case
these will be semantic *denotations *to be combined in a manner
determined by the algorithm that reads them from the output tree
structure (see (Heim and Kratzer 1998) for a compatible system that is
popular among Minimalists).

### <span id="anchor-68"></span>Lexical Item Token

A ***lexical item token ***is a syntactically independent copy of a
***lexical item ***that partici- pates in a derivation. It differs from
a ***lexical item ***only in terms of having an ***index — ***an
***integer ***that is incremented each time a uniquely-identified
***lexical item ***is **Select**ed from the **Lexicon **into a
**Derivation**. This roughly mirrors the *numeration *of (Chomsky 1995).
The indices serve to keep instances of ***lexical item***s
distinct<sup>\[35\]</sup>.

Lexicon

A ***lexicon ***is a set of ***lexical item***s. Ideally, it represents
an entire language. In practice,

it will typically be just as many items as needed to test the
implementation of a particular<sup> </sup>theory.

*****l******exicon***s are represented by ***lexicon files***. Like
***feature specification file***s, ***lexicon file***s consist of a
single JSON object. In this case, the object has a single key —
***lexicon — ***the value of which is an array of JSON objects
representing lexical items. The system will check to make sure there are
no duplicates and that all items are correctly specified. Items loaded
into memory via a ***lexicon ***are available to the system for use in
**Derivation**s.

A sample lexicon file for a highly simple grammar that generates a
single sentence<sup>\[36\]</sup>:

***\{***

***"lexicon": \[***

***\{***

***"tag": "nuts\_1",***

***"phon": "nuts",***

***"sem": "",***

***"syn": \["cN\[nom\]", "iH\[3pl\]"\]***

***\},***

***\{***

***"tag": "parrots\_1",***

***"phon": "parrots",***

***"sem": "",***

***"syn": \["cN\[nom\]", "iH\[3pl\]"\]***

***\},***

***\{***

***"tag": "det\_indef\_pl", "phon": "",***

***"sem": "",***

***"syn": \["cD\[indef\]", "=N\[\]", "uC\[\]"\]***

***\},***

***\{***

***"tag": "like\_1",***

***"phon": "like",***

***"sem": "",***

***"syn": \["cV\[like\]", "=D\[\]"\]***

***\},***

***\{***

***"tag": "v\_trans",***

***"phon": "",***

***"sem": "",***

***"syn": \["cv\[trans\]", "=V\[\]", "uH\[\]", "iC\[acc\]"\]***

***\},***

***\{***

***"tag": "T\_pres",***

***"phon": "",***

***"sem": "",***

***"syn": \["cT\[pres\]", "=v\[\]", "=D\[\]", "iC\[nom\]"\]***

***\},***

***\{***

***"tag": "C",***

***"phon": "",***

***"sem": "",***

***"syn": \["cC\[decl\]", "=T\[\]"\]***

***\}***

***\]***

***\}***

### <span id="anchor-69"></span>Lexical Array

A ***lexical array ***is an object that holds only those items that will
participate in a given **Derivation — **i.e. is an array in sense of
(Chomsky 2001). Items selected from the Lexicon into a ***lexical array
***are instantiated as ***lexical item token***s.

Syntactic Object

*****s******yntactic object ***is a type that subsumes ***lexical item
token***s and combinations of ***lexical item token***s — i.e.
***lexical item token***s that have been **Merge**d (in a process to be
defined below). ***lexical item token***s which are selected from the
***lexical array ***of a ***derivation ***are automatically converted to
a ***syntactic object ***type.

The salient difference between ***syntactic object***s and ***lexical
item token***s is that ***syntactic object***s are recursion-enabled.
They contain, as part of their data structure, a ***constituent list
***of other ***syntactic object***s, which in the case of a head
obviously contains its **Comp **as well as any **Spec**s.

In the interest of keeping the system maximally general, **Spec **and
**Comp **are not explicitly distinguished in this system the way they
are in, say, the LKB, or more recent versions of HPSG. Rather, the
system relies on the insight that in any pairwise **Merge **system it
will always be the case that there is a sequence to the list of items
that have been **Merged **with a particular ***lexical item token
***head. In principle, individual grammar implementations are free to
ignore this, disregarding the ordering for any user-scripted functions.
In this way, shallow-tree systems (of the kind detailed in (Culicover
and Jackendoff 2005), for example) are implementable in the system — one
need only ignore the ordering of the constituents associated with a
phrase. But since the system is intended for use by researchers working
in the Minimalist Program/GB tradition, it is expected that the
overwhelming majority of use cases will choose to write rules that treat
the first item in the internal constituent list — the **Comp —
**considerably differently from the remaining items.

*****s******yntactic object ***also encapsulates — in defined interface
methods — much of the functionality involved in combining with other
***syntactic object***s. This list includes:

**Immediately Contains **an interface function that inspects the
***constituent list ***to de- termine whether the queried item is a
member.

**Contains **the recursive extension of ***immediately contains***: an
item ***contains ***another item if it ***immediately contains ***it or
a member of its ***constituent list ***does. C- command is implemented
by restricting ***contains ***queries to the first item in the
***constituent list — ***the **Comp**.

**Merge **takes another ***syntactic object ***as an argument and
returns a new ***syntactic object ***built from the one on which the
method was called, and the argument<sup>\[37\]</sup>.

**Project **determines the side-effects of **Merge**. Technically this
is a system “hook” — a point where a user-scripted function can be
inserted to specify the next action the system should take. But the
obvious candidates are provided out of the box. These are ***append
***(put the argument on the end of the calling object’s ***constituents
list***), and ***donate ***(a convenience implementation of feature
inheritance per (Chomsky 2008) — see below for more details).

### <span id="anchor-70"></span>Workspace

This concept is adapted from (Collins and Stabler 2016) by taking the
representational idea from that system and embellishing it with
functionality.

A ***workspace ***in this system is an implementational primitive and
should not be confused with the **Workspace**s of (Nunes 2004) or
(Hornstein, Nunes, and Grohman 2005), though they can be leveraged for
the same purposes<sup>\[38\]</sup>. At their core, though,
***workspace***s provide a way of marking items as *active*<sup>*\[39\]*
</sup>in a derivation as well as an interface for executing derviational
actions.

A ***workspace ***in this sense consists of a list of ***syntactic
object***s and a system of interface functions related to their
derivational status. In the general case, a ***workspace***’s list will
consist of either one or two objects. If two, then one that is the
output of previous derivational<sup> </sup>steps and one that is
recently-**Select**ed — whether from the relevant ***lexical array ***or
as a result of a **Probe **on the other object. If one, then either the
initial **Select**ion from the ***lexical array ***or the (possibly
convergent) output of previous derivational steps.

However, this assumes a fairly constrained algorithm for **Select**ing
items from the ***lexical array — ***one that is informed by the
features on the previously-derived or previously-**Select**ed member of
the ***workspace***, perhaps — and this need not be true of all
implementations. Thorough checking for overgeneration in a grammar may
wish to allow for random selection from the ***lexical array***, just to
see what the result is. In this case, it can happen that two
in-principle-uncombinable items end up in the ***workspace ***at the
same time, and it is necessary to **Select **again to proceed. In such
cases, there will be more than two (perhaps many more than two) items in
the ***workspace***. It is really only true for convergent ***lexical
array***s that the “general case” involves ***workspace***s of one or
two items.

*****w******orkspace***s are not mere containers. They also implement a
number of useful interface representations and functions.

Representationally, because ***workspace***s are *ordered *arrays of
items — that is, since **Select**ed ***syntactic object***s are always
appended to the end of the array, the first item in the array has a
special status, which we’ll call *active*. This means merely that
whatever operation is attempted will start by calling the relevant
interface function on the *active *(leftmost, 0-positioned) ***syntactic
object ***and only proceed to the next if it fails on the first. The
utility of this will become easier to understand after reading the
derivational example section (Appendix A), but in simple terms, the
current active head of a derivation should always be first-selected into
the ***workspace***. It is not that the derviation will fail if this is
not the case, it is just that the system will waste a step determining
that the left-most item in a given ***workspace ***can’t actually select
the item to its right, that this must be retried the other way around,
etc.

Functionally, ***workspace***s provide interfaces for the derviational
algorithms to use. Some which are exposed include:

**is\_root **which determines whether a given item in the ***workspace
***is a root in the workspace (i.e. it is there because it is expressly
in the list of contained ***syntactic item***s) or is contained within a
root in the workspace (i.e. is a candidate for **Move**)

**is\_simplex **which determines whether a ***workspace ***has a single
member or multiple members **merge **instructs the ***workspace ***to
implement whatever **Merge **algorithm is defined on it. In the general
case the most active item (the leftmost in the ***workspace***’s array)
goes through each of the other items in the array in turn (in the
general case, there is of  course only one) until it finds (or fails to
find) something that it can **Merge **with. This

returns an updated version of the workspace.

**probe **instructs the ***workspace ***to try to establish a
relationship with another item. This amounts to passing a message on to
the leftmost item in its own array to **probe**. In systems that adhere
to the **merge-over-move **constraint, items should first **probe **in
the relevant ***lexical array ***before attempting to look into their
own arrays of items. **probe **passes a reference to the ***probe***ing
feature into each ***syntactic object ***considered’s own ***probe
***method, and this method, in turn, allows for recursive ***probe
***(in the case where the target ***syntactic object ***is not simplex).
As detailed in chapters 2-3, this is largely the way the system enforces
locality constraints.

The reader may notice that **move **(**re-merge**) and **value **are not
on the list of interface functions. That is because they are expected to
occur only as side-effects of **probe **and so are not directly callable
on a ***workspace***.

### <span id="anchor-71"></span>Stage

A ***stage ***is another implementational primitive adapted from
(Collins and Stabler 2016) and is essentially a “state manager” for
derivations. Like with ***workspace***s, where the Collins and Stabler
version is mostly representational, ***stage***s in this system also
incorporate functionality.

*****s******tage***s contain the ***lexical array ***for a particular
section of a derivation\[40\]<sup> </sup>and at least one
***workspace***. This could just as well be “at most one
***workspace***” but for proposals by (Nunes 2004), (Bobaljik and
Brown 1997) and others that movement of objects between “simultaneous”
derivations — originally called “interarboreal movement,” now more
commonly refered to as “sideward movement” — is possible under certain
circumstances. Additionally, it is convenient to assemble adjuncts in
this way (as they are typically assumed to be fully-formed by a separate
process before attachment to the main “trunk” of — and subsequent
involvement in — the derivation).

A ***stage ***can be thought of as a single (automata-theoretic) “state”
in a derivation, and final convergence depends upon a ***derivation
***object consisting of a single active convergent ***state***.

A given ***stage ***represents the *start state *when

1.  1.  It has a non-empty ***lexical array ***and
    2.  It has no non-empty ***workspace***s

A given ***stage ***represents a *convergent *state when

1.  It has an empty ***lexical array***
2.  It has a single, non-empty, *simplex **workspace ***in which all
    unvalued features on member *****s******yntactic object***s have
    been valued

In the case where a probe had failed to find a match, indicating
divergence, one of two things would have occurred. An inadequate target
might have been found — an intervention effect — in which case the
target would have been added to the ***workspace***’s working array but
never **Merge**d or **Value**d, and so never reintegrated into the
active object. Alternately, *no *target may have been found, in which
case there are un-**Select**ed items in the ***lexical array ***(because
the derivation will be unable to proceed after no suitable connection is
made by the **Probe — **it “crashes”). The requirement that a
***workspace ***be *simplex *for *convergence *arises from the need to
detect a crash in the first case, and the requirement that the
***lexical array ***be empty for the second. Otherwise, the state
*diverges*. Note that it is in keeping with Minimalist principles to
regard all intermediate states in a derivation as *divergent*.
Minimalist conjecture is that the purpose of *C*<sub>HL </sub>is to
establish interface-readable assemblages of lexical items, and Narrow
Syntax is the engine that does this. By assumption, no work-in-progress
is (yet) readable by the interfaces and so is *divergent *by definition.
Therefore, ***stage***s — including the *start state *stage — are either
*divergent *or *convergent *and never anything else.

*****s******tage***s function as “state managers” for derivations in the
sense that they accept and execute instructions and report back on the
effects, in part by deciding on a ***string ***from a list of acceptable
state labels to associate themselves with. The decision function itself
— called a ***strategy ***in the system — reads the new state off of
the stage and creates the next stage from it, at which point the cycle
may repeat itelf by calling interface functions on this new ***stage
***and so on. There is, of course, a default fallback implementation, to
be detailed and demonstrated below, but in principle the usefulness of
the system comes primarily from allowing user lexicon and feature
specification, and secondarily by allowing user modification of the
cycle algorithm by supplying a user-defined ***strategy ***function.

### <span id="anchor-72"></span>The Cycle

*The Cycle *is the process that a derivation goes through at each stage
to edge closer to convergence. Recall that Narrow Syntax is tasked with
assembling items in a ***lexical array ***into a single-rooted object
that the interfaces can “read.” It goes through a series of steps to
achieve this goal. At each step, it finds itself in a state that is
either *divergent *or *convergent*. As explained, the vast majority of
these are *divergent*. Some of them are *irreparably divergent*, in
which case the derivation fails — is said to “crash” in the jargon. If a
derivation finds itself in a state that is *irreparably divergent*, it
is in a failed state and should halt. If it finds itself in a
*convergent *state, it is in a success state and should also halt
(though it can form part of the input to further derivations).
Otherwise, it carries out an implementation of the cycle to determine
what action to take next and then to take that action.

The default cycle is simple:

1.  Activate

2.  Perform
    
    1.  Designate
    2.  Probe
    3.  React

3.  Evaluate

**Activate **decides on a ***syntactic object ***as the actor in the
next cycle. This is user-scriptable, but in the default case it is
simply the leftmost object in the active ***workspace***s array followed
by, if nothing can be done with the leftmost, the next one and so on
down the list until there are none left. This will suffice for almost
all implementations. But more complex implementations — for example,
those that involve multiple workspaces — may exercise more control over
this process.

**Perform **is a loop that repeats three steps until nothing more can be
done. **Designate **decides on a **Probe **on the active item to try. In
the general case, this is the first *active *(in the sense of (Chomsky
2001)) probe in the active ***syntactic object***’s lexically specified
list of features. **Probe **implements the process of looking for a
match for the probe’s features. In **merge-over-move **honoring systems,
this means it will first look for matches in the ***lexical array ***and
only then, when none are found, attempt to probe its **Comp**. In the
default algorithm, the **Comp — **i.e. the *first *item in the active
***syntactic object***’s constituent list — is the only item tried
outside of the ***lexical array***. In more sophisticated systems, other
things are possible. For example, a probe could search in another
workspace, if one is present (implementing what is sometimes called
interarboreal or, more colloquially, “sideward” movement), or it could
proceed down its own constituent list (effectively **Probe**-ing its
specifiers). After **probe **has completed, the system moves on to
**React**, which implements any side-effects of probe match. If the
probe is unsuccessful, in a standard (Chomsky 2008) system **React
**should throw an error, aborting the derivation.<sup>\[41\]
</sup>Otherwise, the item is copied into the active objects array in the
***workspace ***to mark that a relationship has been established between
the **Probe**-ing item and this target. From there, the system will
**value **any items in the ***workspace ***array according to their
array of features — as membership in the array marks that they are in a
relationship with the active ***syntactic object***. **value **itself
will have side-effects, which in the general case means removing the
item from the array.<sup>\[42\] </sup>But this will not always be the
result. In the case where the item came out of the ***lexical array***,
chances are it was as the result of a **Select **feature, in which case
**value **will instruct the system to **merge **as a side effect. This
is also the point where EPP features come into play.

EPP, in this system, is effectively an override instruction to **merge
**where the system would normally **return**<sup>**\[43\]**</sup>.

**Perform **iterates until all active probes have been tried.

**Evaluate **fires after the **Perform **loop exits. It is tasked solely
with deciding on what state the stage ends in, and what to do about it.
If errors were thrown in the **Perform **loop, it “handles” them,
generally by aborting the derviation with a printed explanation of why
it failed. Otherwise, it checks the state conditions outlined above and
decides which applies. It then returns a copy of itself<sup>\[44\]
</sup>which will be the input to the next cycle.

The apparent simplicity of this process of course conceals a lot of
implementational details. For example, on **probe**, it conceals the
order in which to attempt each of the active ***syntactic object***’s
potentially numerous **Probe**s. There are plans in the future to allow
users to intervene in this process (by, e.g., allowing conditional rules
on probe ordering, or access to workspace selection, etc.). For now, it
is assumed that probes are tried in the order in which they are
specified on the ***lexical item***. Additionally, determining which
**probes **match what is a bit complex. This, again, is user-scriptable.
In the default case, it is much the same as HPSG in the sense that it
obeys the ***feature geometry ***outlined in the ***feature
specification file ***according to standard unification algorithms. A
probe **match**es a goal of opposite polarity if the goal has a category
that is identical to its own or else rooted lower in the hierarchy. So,
“Feature,” the top level, matches any category, and a highly-specific
one, like “Author” (see (Preminger 2014)) pretty much only matches other
“Author” features. Another wrinkle is that some systems wish to
intervene on **match **and prevent **value **in some way. For example,
for the purposes of clitic doubling in a number of systems, it’s assumed
that **Dative **nominals can’t value a probe, but they can copy full
sets of *φ *features, which show up as a clitic. No attempt is made to
try to implement such a complex system here, it is merely noted as
justification for treating **value **as a system “hook” where
user-defined functions can be inserted.

## <span id="anchor-73"></span><span id="anchor-74"></span><span id="anchor-75"></span>Feature Inheritance

Before moving on to the ***derivation ***class, it is probably worth
taking a detour into the **feature inheritance **of (Chomsky 2008). Of
all the mechanisms surveyed in previous chapters, this one is perhaps
the biggest puzzle.

To start with what is clear — whatever **feature inheritance **is, it
must be a side-effect    of **merge **and not **value**. We know this is
so because the whole point of it is to give **T **countercyclic **probe
**features. “Countercyclic” means giving **T **an opportunity to **probe
**after the point in the cycle where it should have been allowed to —
which is really just a fancy way of saying that **T **should be allowed
to participate in **C**’s **probe **cycle using **C**’s feature. But
putting it just that way begs the question of why this can’t just stay
**C**’s cycle. Presumably, the answer is one or both of that
*wh*-objects need to be **Probe**d first (to obviate the intervention
effect and make the subject visible to **T**) — and **C **probes go
first since it’s “**C**’s turn” — or that the subject needs to end up in
**T **for various other reasons (articulatory or scopal). Either way, we
need more control over the implementation than comes with the default
algorithm. To solve the probe-ordering issue, there would need to be
some mechanism that relegates the (now-)**T**-associated **probes **to
the end of the list. To solve the positioning issue, the probes would
have to be marked in some way to indicate that any (re-)**merge **that
takes place would have to adjoin to **T **rather than **C**. The problem
with this, of course, is that **T**, having already **merge**d with
**C**, is not in the array of ***workspace***-active ***syntactic
object***s, breaking the standard way of achieving this goal in this
system. Now, there’s nothing in principle wrong with having a
side-effect of **merge **that leaves the target “active” in the sense
that it sits in the array of active ***syntactic object***s even after
having been **merge**d. But in practice keeping **T **separate breaks
the **probe **path, since **C **doesn’t yet have an explicit **Comp
**(since **merge **wouldn’t have completed, as the pair of involved
items is still represented separately in the **workspace**). It’s like
**C **needs to have **T **in its **Comp **at the same time that **T **is
in the active array.

The solution is just to do that literally. **Feature inheritance **is
implemented as a kind of *incomplete merge*. Since the ***syntactic
object***s that are in the active array are pointers, there is no
problem with adding **T **to **C**’s constituent array (in the first
position, as a **Comp**) while also leaving it in the active array. It
is both *active *and **merge**d all at once.

The question of how to implement the actual sharing part is not
difficult to answer: just do that literally as well. There is plenty of
evidence from the literature to justify including such an operation (as
a side-effect of **merge**) in the system. This includes things like
pronouncing multiple intermediate copies of simplex *wh*-items in some
Germanic languages (Felser 2004) — a fact that (Herring 2009) interprets
as pronunciation of intermediate landing sites which have “borrowed”
their phonetic features from the moving item. It also includes many
analyses of clitic doubling (e.g. (Béjar and Rezac 2003; Preminger
2014)). And, there is also some evidence directly to do with feature
inheritance. (Ouali 2008), for example, argues from agreement patterns
in Berber — in which subject agreement sometimes appears on **C — **that
**feature inheritance **can actually take one of three forms:

1.  **Donate — **in which **C **simply gives its *φ*-features to **T**.
2.  **Share — **in which the features are active on both **C **and **T
    **(presumably through a (Pesetsky and Torrego 2007) type of
    arrangement)
3.  **Keep — **in which **C **doesn’t transmit anything.

These situations correspond to varying agreement patterns.

If there are plenty of accounts in the literature that depend on the
ability of a head to transmit features to another as a side-effect of
**merge**, then clearly the system has to make this available as a
mechanism to researchers. So, it is provided in the default cycle
algorithm for **C **and **T — **to cover the (Chomsky 2008) argument —
in the present version of the system, and later iterations of the system
will make it modifiable by users.

The problematic bit that remains is “cleanup.” After this
implementation, **T **remains in the “active” array at the end of the
phase, which means the ***stage ***will incorrectly think it’s failed
and return in an error state. There doesn’t seem to be a good solution
to this problem in the present system, so for now a stipulative
“cleanup” phase is added to **Evaluate **that detects this
situation. In techical terms, **cleanup **checks to see whether the
following situation obtains:

1.  There are only two items in the active ***workspace***’s active
    items array
2.  One of these items is contained in the other
3.  Neither of the items have active probes

If these conditions obtain, remove the contained item from the active
array, and retry

**Evaluate**.

## <span id="anchor-76"></span><span id="anchor-77"></span><span id="anchor-78"></span>Head Movement

Head movement is equally problematic to implement, not so much because
the necessary primitives are not independently available in the system
as that it isn’t entirely clear from the literature what head movement
is. Through most of the GB period and into early Minimalism, it was
taken to be some kind of incorporation: one head raised to the next
highest head<sup>\[45\] </sup>and in some important (if vague) sense
*fused *with it. It wasn’t clear whether the moved head left behind any
kind of trace, but if it did it certainly didn’t *c-command *it, making
this kind of movement technically “improper” (see (Müller and Sternefeld
1993) for a detailed discussion of what counts as “improper movement,”
including examples that go beyond the *c-command *requirement, and
(Fukui 1993) for an early Minimalist reworking of GB conditions on
proper movement).

(Chomsky 2001) lists a number of characteristics of head movement that
make it problematic *as a syntactic phenomenon:*

1.  It never seems to affect interpretation (though see (Matthew 2015)
    and (Funakoshi 2013) and (Roberts 2011) for recent arguments that it
    sometimes does).
2.  It is not clear what the trigger is. Relegating it to features would
    require the feature system to be able to distinguish between heads
    and phrases, which Bare Phrase Structure arguably tries to avoid
3.  It is countercyclic and violates the Extension Condition.
4.  It is improper movement as the moved head does not *c-command *its
    trace (at least, not without complications of the definition of
    *c-command*).
5.  It is not successive-cyclic, but rather always “rolls up” (each
    subsequent movement always form a successively more complex head; it
    is not the case that a single head can move to one head position and
    then continue on to the next without taking the head at the
    preceding landing site along with it).

These form the motivation for rethinking head movement as an entirely PF
process.

Since feature transmission in the sense of (Ouali 2008)‘s **Donate **is
available in this system, the suggestion is to use that. “Head movement”
means that the lower head of the pair **Donate**s all of its features to
the higher one. This is essentially “reverse feature inheritance.” And
since inheritance happens on **merge **using the same mechanisms that
underly C-T feature inheritance, there is no need to complicate
*c-command *to get the desired result: there is no question that the
lower head is “visible” for feature sharing/donation/inheritance at the
point the target head **merge**s with it. The operation is simple: *all
*the features of the lower head, including ***phonetic ***and
***semantic ***features (if any) are “unshifted” onto to the front of
their counterparts’ values in the higher head (and deleted from the
lower head). The lower head ceases to exist as anything other than a
position in the hierarchy; all relevant information about it is realized
at the analogous position one higher up.

This should accurately capture all of the empirical facts. It captures
the pronunciation shift (including — thanks to the fact that these
features “unshift” onto the front of the target head’s array rather than
concatenating on to the end of it — all observations underlying the
“mirror principle” of (Baker 1988)), and captures the “rolling up”
effect/lack of successive cyclicity. It does not capture any
interpretive effects that may need to be accounted for, but this can
always be remedied by specifying **Share **rather than **Donate **(so
that syntactic features are represented in both associated places in the
hierarchy, effectively collapsing them in syntactic terms, but semantic
denotations continue to occupy separate nodes), or else distributing the
relevant features between **Donate **and **Keep **(i.e. selectively
deciding which go where).

## <span id="anchor-79"></span><span id="anchor-80"></span><span id="anchor-81"></span>Select

Nothing much has been said up to this point about **Select — **another
mildly problematic category. The question with **Select **in any system
is whether to treat it as a system primitive or to leverage features in
its implementation. Like with **head movement**, there is no real
consensus in the literature about how to answer this, nor is there much
in the way of detailed treatments of the topic. Researchers tend to take
**Select **as a given and gloss over its mechanics.

As has been hinted at in earlier sections, this system takes the view
that **Select **is a part of the feature system — effectively a
side-effect of **probe**.

The main wrinkle comes in trying to capture its optionality. While
**Select**ion of arguments is (usually) required, adjunction is free and
(apparently/often) also unconstrained with regard to number. And yet,
it’s clear that **Select **plays a role even in adjunction, since it
is not typically possible to adjoin *just any *category to a given
projection. The head has some say in what participates in its phrase,
even outside of its internal argument. This mirrors one of the puzzles
of the EPP, alluded to earlier, whereby it seems to be highly
specialized for the category it attracts, suggesting a featural
implementation, and yet it does not seem to pair with other features
(does not participate in the interpretable/uninterpretable polarity
system).

Call it the No Platypus Principle, but unlike natural systems,
computational implementations have to decide on an interpretation in
situations like this, and this system chooses the feature route.
Selectional features are features like any other, meaning they have
polarity and come in pairs. In the case of optional selection, the
**selector **is *uninterpretable — *since it acts as the **probe — **and
the **selectee ***interpretable*.

It is at this point that the distinction between *uninterpretable *and
*unvalued *pays dividends. If the interfaces are only concerned with
feature *values*, and not with feature *polarity*, as seems reasonable,
then we can leverage feature geometry to implement optionality. Optional
**Select **is implemented with an *uninterpretable *but *valued
*feature, where the value is present but underspecified. For situations
like sequences of adjective phrases, where multiple are allowed, but
there are nevertheless some constraints on in what order they adjoin,
the implementor can simply define a feature hierarchy that takes care of
this. The category values of the “closest” adjective types would need to
be “highest” in the feature geometry tree, so that at each stage of
selection, unification could take place and the value on the **selector
**N head could get “more specific” (i.e. successively replaced with
lower values in the hierarchy). However, since the N head comes already
valued out of the lexicon for its adjectival modifier feature, the
interfaces will not complain if it doesn’t combine with any.

*θ*-selection would be handled more traditionally. An argument-seeking
**selector **head would have an uninterpretable/unvalued selection
feature, enforcing the obligatory nature of argument selection. The
target **selectee **argument would have an interpretable but unvalued *θ
*feature, and an interpretable and valued selection feature — a value it
transmits to its **selector **to mark that the **selector **has picked
an argument. Getting *θ*-marked means having its *θ *feature valued by
the corresponding version on the **selector**.

Any implementation that treats *θ*-marking as feature-driven is probably
obligated to say something about the Movement Theory of Control
(Hornstein 2000), since the idea that *θ*-marking is feature-driven is a
hallmark of that theory, and the idea that allowing items to accumulate
*θ*-roles overgenerates (without baroque prevention mechanisms) is the
main argument against it (Landau 2003). In reality, there’s no need to
take a position on this here since the debate doesn’t hinge on the
mechanism of *θ*-role transmission so much as whether multiple *θ*-roles
are allowed. Any system in which a valued feature can’t be
re-valued<sup>\[46\]</sup>, or where accumulation of values is not
allowed, will get the “standard” theory of control of (Landau 2003) even
if *θ *roles are implemented with features.

## <span id="anchor-82"></span><span id="anchor-83"></span><span id="anchor-84"></span>Phases

Surprisingly, given how much has been written about *phases *in recent
years, little need be said about them here. A system such as this one is
successful to the extent that seemingly radical departures from the
basic system turn out *not *to need *ad hoc *solutions — meaning
solutions that have to be implemented directly<sup>\[47\]</sup>. Phases
in the (Chomsky 2008) and (Gallego 2010) sense, indeed in almost every
sense, can be relegated to the lexicon.

The two salient points about *phases *for these systems are:

1.  Phase heads are the sole locus of uninterpretable features AND
    
    Phases are *impenetrable*

The first point is the responsibility of the lexicon writer, so any
researcher who buys this analyses need only take responsibility for
seeing that the lexicon he feeds the system contains no non-phase heads
with uninterpretable features. In practice this will be impossible,
since this system treats selectional features like any other. So, at
least uninterpretable selectional features will have to exist on
non-phase head. But this is not really a problem since it doesn’t seem
to violate the spirit of the proposal in any way<sup>\[48\]</sup>.

The second point is a bit more complex, since there are several versions
of the **phase impenetrability condition **that would need to be
covered. In the basic case, any phrase in this system can be made
“impenetrable” by including the “barrier” feature on the relevant
head. Wherever the head **merge**d in **is **the barrier in question,
the matter is as simple as including the “barrier” feature in the item’s
lexical entry. In more complex cases, where merger of the phase head
causes the (complement of the . . . but see (Fox and Pesetsky 2005))
*next lower *phase to be **spell**ed **out**, it is implementable via
**feature inheritance — **transmission of the “barrier” feature can
simply be included in the **merge **side-effects. So, phases turn out to
be a derivative notion, and not really an implementational primitive.

## <span id="anchor-85"></span>Derivation

*****d******erivation ***is the driver class of the system. It is
responsible for setting things in motion and evaluating the result. It
takes as input a ***lexical array***, which can be an array of arrays.
An initial ***stage ***is created for each subarray; if there are no
subarrays, only a single stage is created. ***derivation ***then decides
on which of the subarrays to start with and takes responsibility for
selecting the initial item. Having done so, it places the active stage
in a ***history ***array (that represents the derivation as a whole),
sends a ***probe ***signal to it, and receives the result. As indicated,
the result of sending a signal to a ***stage ***is always a new ***stage
***which is a copy of the original ***stage ***with all changes that
occurred during its cycle applied. At a minimum, this means its state
indication will have changed (because if no other changes occurred it is
either convergent or there was an error). The ***derviation ***places
the new ***stage ***on the ***history ***stack, inspects its state and
decides what to do from there. It continues this process until there is
a convergent state on top of the stack and no more ***lexical array***s
to account for, in which case it returns a *converge *message, or until
it exits with an *error*.

## <span id="anchor-86"></span><span id="anchor-87"></span><span id="anchor-88"></span>Derivation Examples

A sample derivation of “Parrots like nuts” (from (Citko 2014)) is given
in Appendix B along with some pointers for implementing other example
sentences. Additionally, the following chapter demonstrates some ways in
which the need to carefully implement a theory can expose unintended
side-effects of its assumptions. A complete derivation of one critical
example sentence from this chapter is available in Appendix A.

[Back](jherring-3) — [Forth](jherring-5)
