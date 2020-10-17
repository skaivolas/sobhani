---
title: Grammar Construction in the Minimalist Program — Conclusion
layout: page
---

[Back](jherring-5) — [Forth](jherring-7)

# <span id="anchor-111"></span>Conclusion

## <span id="anchor-112"></span><span id="anchor-113"></span><span id="anchor-114"></span>Contributions

The primary contribution of this study has been the development of an
LKB-style grammar development environment for researchers working in the
Minimalist Program. To the best of the author’s knowledge, it is the
first such attempt within the GB/Minimalist tradition. This is somewhat
surprising, given that the speculative nature of Minimalist research
provides a number of opportunities for such a tool to be of assistance.
In particular, because Minimalist research is directly concerned with
the cognitive devices that are involved in sentence produc- tion — it
goes beyond lexical specification of the component parts for a
particular language, as is more the emphasis of competitor theories that
tend to be either monostratal (HPSG, CCG, Dependency Grammar) or at
least non-derivational (LFG) — the danger that new theories will break
prior analyses in unexpected ways is particularly high in this
tradition. A tool that can help either verify that a new analysis
preserves the insights of prior analyses, or else point out where the
points of conflict are, is potentially quite useful.

As it is not, however, the first attempt to make a grammar development
environment for research purposes, nor is it the first attempt to
capture minimalist insights in a software tool, it is worth taking some
space to clarify the points of departure with similar efforts.

### <span id="anchor-115"></span>The LKB

The system that inspired this work, the *Linguistic Knowledge Builder
(LKB) *of (Copestake 2002), is the most obviously similar in purpose.
Like this system, the LKB aims to provide researchers a tool that
verifies speculative theoretical results primarily by (a) guaranteeing
that results neither over- nor under-generate sentences relative to the
researcher’s claims and (b) pointing out any points of tension with
earlier analyses — specifically areas where assumptions specific to the
new analysis conflict with assumptions of previous ones. The only real
difference is in the target: where the LKB implements unification
grammars — preferably, though not exclusively, in the HPSG paradigm —
this system is focused on the derivational approach of the Minimalist
Program.

The difference is not trivial. While it is popular in formal circles to
speculate that explicit transformation offers no generative power over
and above what slash features<sup>\[65\] </sup>offer, the
implementational details at least are quite different. Researchers used
to thinking in transfor- mational terms — indeed, who find
transformations to be the correct abstraction for capturing human
linguistic knowledge — find themselves in an alien environment working
in the LKB. Since the transformational tradition remains prominent and
productive, it is good to have a tool that speaks its language.

In addition to their significant implementational differences,
Minimalism and Unification Grammars also differ sharply in focus.
Unification Grammars are typically more practical- minded in purpose.
They make weaker cognitive claims than Minimalism. The concern is less
with getting the mechanisms of the mind exactly right than with modeling
the output. For this reason, there is usually more concern with
consistency and coverage in Unification Grammars. What percentage of
observed sentences for a language<sup>\[66\] </sup>does a particular
implementational lexicon generate? How does changing the feature
specification of a particular lexical item’s entry affect this coverage?
These are the kinds of questions that feature prominently among
researchers using the LKB. In the Minimalist tradition, by contrast, the
focus is on the spadework of uncovering generative mechanisms. In a
sense, Minimalist researchers are more focused on exotica, because these
are the phenomena that are most likely to help define the boundaries of
human linguistic competence. Concerns about coverage are typically
secondary, and this ordering of priorities is reflected in the fact that
there are, to the author’s knowledge, no freely-available text corpora
annotated for Minimalist research. One of the purposes of this project,
indeed, is to bring coverage concerns to prominence within Minimalism.
But even to the extent that it is successful, coverage will always take
a back seat to spadework in Minimalism given the nature of the program.
For this reason, there is in a real sense no possibility of an “LKB for
Minimalism.” This system serves a subtly different purpose for a subtly
different research program.

### <span id="anchor-116"></span>Minimalist Grammars

The *Minimalist Grammars *of (Stabler 1997) and subsequent work operate
in the same paradigm targeting the same research papers as source
material, but again with an important difference in focus. While both
systems are, to a degree, interested in *verification *of research
results, *Minimalist Grammars *mean this in a purely formal sense. The
idea is to identify the kernel of the Minimalist Program and establish
it on a firm, formal footing to study the model, provide a template for
implementation, and verify results. The emphasis on proveability and
formal correctness is indispensible to the continued relevance of
Minimalism, but it is also confining in three ways. First, because the
formal devices used are somewhat unfamiliar to most minimalist
researchers, there is a bit of a barrier to entry. Second, while the
Minimalist Program can and undoubtedly will benefit from the more
disciplined approach *Minimalist Grammars *take, it is nevertheless a
fact that Minimalism as practiced simply doesn’t work this way. Indeed,
its founding principles — the repeated insistence that it is a program
and not a theory — are arguably designed to *avoid *formal
specification. Third, *Minimalist Grammars *tend to be more
representational than derivational. Like with the LKB, the focus isn’t
really on allowing language implemenators to tweak the derviational
algorithm; rather, it is up to the researcher to conform to the
specifiation. In a *Minimalist Grammar*, the researcher doesn’t, for
example, have the opportunity to attach a side-effect to a particular
feature match. In this sense, *Minimalist Grammars *are perhaps at odds
with the way minimalist researchers think about language.

It is expected, however, that this project will eventually converge
completely with the research being done by Stabler and colleagues. The
approaches diverge due to difference in emphasis, but the end goal is
the same.

### <span id="anchor-117"></span>Minimalist Program Grammar Implementation

As with *Minimalist Grammars*, the point of departure with the
*Minimalist Program Grammar Implementation *of (Fong and Ginsburg in
preparation) is mainly one of emphasis. Where this project provides a
platform for experimenting with different approaches to Minimalism, the
MPGI distills the most plausible candidate implementation from current
research and implements it for industrial use. Important practical
differences include a focus on parsing and a somewhat frozen
implementational system. This system, by contrast, is concerned with
generation and verification of research results. While it is possible
that this system will eventually incorporate the results obtained for
minimalist parsing by the *Minimalist Program Grammar Implementation*,
the functionality of the two systems is currently aimed at very
different purposes, and there is consequently not much overlap.

### <span id="anchor-118"></span>Specific Contributions

A secondary purpose of this project has been to emphasize the importance
of implementation in uncovering hidden assumptions and resolving
theoretical disputes. Indeed, several were noticed in the course of
program development.

The most important of these has been recognizing the ways in which
underspecification of the derivational algorithm can lead to confusing
results. Implementing a derivational system in software forces attention
to details that can be glossed over in text-based explanations. For
example, when **select**ed, how does that process unfold *precisely*? A
typical text-basd explanation will simply note the fact that **select
**occurred, but an implementor has to actually make it happen. For the
present project, this meant, in the case of an item **select**ed from
the active ***lexical subarray***, deleting it from the ***lexical
subarray ***and copying it into an array of active items, with the
assumption that it would subsequently **merge**. This was a step
necessitated by the need to eliminate a certain kind of **lookahead
**from the system that is probably not obvious to the
non-implementational researcher: what if the system **select**s items
from the ***lexical subarray ***in the “wrong” order? There must, after
all, be an *unmotivated *initial selection. Ideally, this initial
selection is precisely the item that will, in turn, **select **the next
appropriate item from the subarray. But no system can know, without
arguably illegitimate guidance, which picks are the “right” ones, and no
system that uses generation as a tool to verify that the extent of
grammar coverage is exactly what is claimed *should *provide such
guidance. The system has to be free to **select **items in any order,
which means something has to be done with previously-**select**ed items
that are either unable to **select **items themselves, or will **select
**items that do not necessarily follow the order of selection a typical
research paper would report. Many options are available, of course. One
could simply return an unsuccessful **select **back to the ***lexical
array***. One could provide the system with heuristics to guarantee that
the *phase *head (or at least the item with the most immediate
selectional feature) is always first **select**ed (this is the approach
taken by this system). The point is that once one has determined that
**select **actually means (something like) “identify and copy to an
array of active items,” it highlights the idea that there is no *a
priori *reason why **merge **must immediately follow **select**, even if
this is the general case. The two operations are computationally
distinct<sup>\[67\]</sup>. Once this is understood, the EPP seems a
shade less arbitrary. After all, any system that starts with ***lexical
array***s needs an in-principle-unmotivated operation to start the
process moving in any case; this recognized, the idea of a diacritic
feature that requires an object to undergo **select **and then **merge
**on lexical items is nothing more than triggering a function we know
the system already has. For this reason more than any, it is useful to
have an *explicit *derivational algorithm, and this system has provided
that.

Perhaps the next most important is the recognition that Minimalist
grammar development has three core components: feature specification,
algorithm specification, and triggered side effects. As far as the
survey of the literature done here indicates, every tool at a minimalist
researcher’s disposal falls into one of these three categories. Thus,
what seemed impossible in principle — building a system that allows
researchers to implement *arbitrary *new minimalist theories — is
probably tractable in practice, even if there is no way to guarantee
coverage of every future development. What any conceivable minimalist
grammar development environment, including future competitors to this
project, must provide, then, are (1) a way for users to create lexical
items composed of feature sets, (2) a way for users to reorder the steps
the system takes, and (3) an API that allows for the addition of
user-scripted “hooks” that operate on the system’s object in response to
system events. It is this last point that arguably separates Minimalism
most sharply from more representational systems like HPSG and LFG,
that<sup> </sup>shows that Minimalism, at its core, retains the
derivational character of its ancestors. Certain (combinations of)
features trigger certain reactions, and users of any conceivable
minimalist grammar development environment must have the power to script
those reactions.

Some such reactions that featured prominently in Chapter 5 were **head
movement **and **head incorporation**, and there was the related queston
of whether these were substantively different. The chapter offered the
tentative concluson that they are the same process, that they are *not
*substantively different, and that in fact the persistent question of
whether **head movement **is a cyclic or post-cyclic (PF-only)
phenomenon is actually a bit of a distraction. Again, an implementor
must decide exactly *when ***head movement **happens, and also *how *it
happens in somewhat more detail than simply showing a head attached to
another head. In the present system, it was decided that, without user
involvement, **head movement **happens immediately on **merge**.
Moreover, **head movement **means that the *entire *feature array of a
“moving” head is prepended on the front of the feature array of the
receiving head. In effect, they become a single lexical item. This is a
process already anticipated by (Chomsky 2008)’s addition of **feature
inheritance **to the inventory of operations: **head movement **is
nothing more than complete feature transfer (including phonetic
features). Since features are *prepended*, there is no change in the
order in which arguments are **select**ed relative to treating the
merged heads as kernels of separate phrases. This allowed the system to
follow the obvious heuristic (alluded to above) of having the *phase
head *always be the first-**select**ed item from any ***lexical subarray
***that contains one without undesired ordering side effects. *v *is
first-**select**ed, and it, in turn, **select**s V, and the *v*-V
complex **select**s V’s complement, its external argument, and then
*v*’s external argument in the usual order. People who prefer to see
head movement as a PF effect can point to the fact that the ultimate
sequential ordering must still reflect the underlying architecture —
***spec***-*v *preceeds *v*-V preceeds ***spec***-V preceeds
***comp***-V. This is presumably a PF decision. People who prefer to see
head movement as syntactic can point to the feature transfer as an
undeniably syntactic implementation. Both parties are correct in their
way, and the debate was probably never worth having. But this is the
sort of thing that isn’t necessarily noticed until an implementation is
pursued — whether with software or on paper — to an appropriate level of
detail.

A similar contribution that “falls out” of the implementation is the
realization that *phases *are not an architectural innovation in need of
special enforcement by the system. They are perfectly implementable with
chapter 4’s *barrier feature*. All that is actually required is that the
appropriate phase heads be endowed with one, guaranteeing that all
**probe**s halt at the phase boundary. Notice also that a fact about
*phases *that seemed synthetic to many researchers is actually quite
natural: the idea that the periphery (i.e. the ***spec ***of the **phase
**head) is accessible in a way that the ***comp ***is not. This is
simply a consequence of the fact that the *barrier *feature is
represented on the *phase *head, as is natural if it is the head that
defines the *phase*. In a normal in-order tree traversal, a **probe
**will his any ***spec***s *before *it hits the head, and it is only on
hitting the head that it encounters the *barrier *feature and halts.
Phases are not so mysterious after all. Like so much else, they are a
factor of lexicon design.

## <span id="anchor-119"></span><span id="anchor-120"></span><span id="anchor-121"></span>Future directions

Though the core of the system is in place and available for use, the
project is far from complete. In broad terms, the work that remains is
as follows.

Foremost, it is necessary to do what amounts to a second version of this
project dealing with PF processes. The current system simply uses
in-order tree traversal string concatenation, augmented by deletion, to
yield the surface order. This is useful for little more than demon-
strating that the syntactic component is working correctly. The number
of hypothesized PF effects has exploded in recent years, so it will be
necessary to do a separate comprehensive survey of what has been
proposed and to implement a new API exposing them to users. This is the
next step for this project.

Secondarily, semantic hooks will need to be exposed. The distinction
between Transfer — which sends information to LF — and SpellOut — which
sends output to PF — is not much maintained in recent work, but in the
original concept it was typical to treat SpellOut as cyclic (“multiple
spellout”) and Transfer as a single reading from an assembled tree. This
project takes that approach: it is possible even now to add semantic
“features” to ***lexical item***s in the ***lexicon — ***in the ***sem
***field reserved for that purpose. A semantic module would need to then
traverse the tree, reading these features and assembling them
appropriately. Since no particular semantic theory is favored in
Minimalism (though (Heim and Kratzer 1998) is a go-to resource for
non-specialists), it is best to leave the implementation up to outside
module writers. Once the PF implementation is satisfactory, the next
step will therefore be to collaborate with semantics module writers to
make sure that the system API exposes everything that they need to do
their work.

Finally, though this system is focused on sentence generation as a means
of verifying research claims, there is no reason why it shouldn’t
eventually be expanded to include parsing. It is at this point that the
system will seek to merge with work done in the *Minimalist Grammars
*tradition — specifically on foundations laid in (Harkema 2001) — to run
all the devices “in reverse.”

[Back](jherring-5) — [Forth](jherring-7)
