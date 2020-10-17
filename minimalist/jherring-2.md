---
title: Grammar Construction in the Minimalist Program  — Chapter 2 — An Overview of Phases
layout: page
---

[Back](jherring-1) — [Forth](jherring-3)

# <span id="anchor-12"></span>Chapter 2 — An Overview of Phases

## <span id="anchor-13"></span><span id="anchor-14"></span><span id="anchor-15"></span>Motivation

One of the side-effects of Minimalism’s reimagining of syntactic
derivation as a pair-wise, bottom-up process was the introduction of a
“timing” problem: certain independently licit operations had to be
constrained from applying at certain points in the derivation to prevent
ungrammatical results. The canonical example (modified slightly from
(Citko 2014), citing (Chomsky 2000)) involves **Merge **of an expletive
with an expression involving a small clause:

16) 1.  1.  Many people are likely to be at the party.
        2.  There are likely to be many people at the party.

Both expressions are grammatical and express the same idea. They differ
only in the presence of the expletive *there*.

Introducing the expletive has some interesting consequences. These
include (a) that the expletive intervenes in any attempt to move *many
people *over it (in (2)) to the left edge of the expression and
apparently also (b) that it must be **Merge**d in the **Spec **of *to
*(**T**).

Motivation for (a) comes from examples like (3):

16) 1.  1.  \*Many people are likely there to be at the party.

Although licit at the left edge of the clause in (1), *many people *is
barred from this position when the expletive is present.

More interesting is that *many people *seems to be barred from moving at
all under these circumstances. That is, even to the right of *there*,
moving *many people *seems to violate some constraint of the system:

16) 1.  1.  \*There are likely many people<sub>i </sub>to be *t*<sub>i
            </sub>at the party.

It is a bit surprising that this should be the case. By assumption,
*many people *lands in **Spec**-**T — **that is, just to the left of *to
— *on its way to the left edge of the clause in (1). Furthermore, this
cannot be intrinsically motivated (such as for case checking), or *many
people *would never be licit in its original small clause position, as
it is in (2). *many people*, it seems, either makes it “all the way to
the top,” or it doesn’t move at all. But if the intermediate movement is
not motivated by anything intrinsic to the phrase — i.e. is in some
sense “optional” — something must prevent it from happening in cases
like (2) where the expletive is present.

The addition of *phase*s to the Minimalist toolkit begins with (Chomsky
2000)’s solution to this problem.

If the intermediate movement step is real in (1), then the most
straightfoward way to rule it out in (2) (thus avoiding the
ungrammatical (3)) is to somehow require *there *to enter the derivation
at that point, blocking it at the source. This is the approach (Chomsky
2000) takes, proposing a **Merge over Move **principle that, all else
equal, requires the derivation to proceed with a **Merge **operation at
junctures where both **Merge **and **Move **are available and motivated.
The tree diagram below shows such a juncture:

After the **Merge **of **T ***to *and **VP ***be many people at the
party*, assume there is an *EPP\[5\]*<sup> </sup>feature on **T **that
must be checked. This can be done either by **Move**-ing *many people
*there, or by **Merge**-ing in *there*. **Merge over Move **requires the
derivation to prefer the latter. Each is schematized below:

**MOVE ***many people*

**MERGE ***there*

![](Pictures/1004640500001D9C00000E0318AB00E01E44B8DE.svgPictures/10000201000000D700000066130596939E78ADBB.png)

By **Merge over Move**, the derivation schematized by the first tree is
licit only if there is no available expletive to **Merge**, as in (1).
If one is available, moving *many people *is ruled out, and only the
derivation schematized by the second tree is allowed.

That solves the immediate problem, but at the cost of introducing
others. Computationally,<sup> </sup>**Merge over Move **has the
potential to massively complicate the grammar by requiring the
comparison of parallel derivations; it requires **Lookahead**. At the
point in the derivation where **Merge over Move **must come into play,
it is not yet known if **Merge**-ing *there *will be required. *There*,
for all the derivation knows, could end up put to some other use later,
one where it doesn’t block *many people*’s path to the left edge,
obviating the problem that the principle is enlisted to solve. For
example:

16) 1.  1.  There is reason to believe that many people will be at the
            party.

Having **Merge**d in *there *at the first **Merge over Move **point
would have yielded\[6\]<sup> </sup>the ungrammatical:

16) 1.  1.  \*There is reason to believe that will be many people at the
            party.

In (5) and (6), the facts are reversed from (1) — (4): **Move **seems
*required *here.

There are, in essence, two ways to solve the problem without giving up
the principle: either **Merge over Move **admits of exceptions, or there
is some reason why *there *is not available at the relevant point in
this derivation.

(Chomsky 2000) opts for the latter. The **lexical array **that limits
access to the **Lexicon **for the purposes of a given derivation is
given more articulation. It is subdivided into **Lexical Subarray**s,
operations on each of which must complete *independently *of the others
as far as possible before being **Merge**d together. Access to elements
in (structures formed from) one subarray by (structures formed from)
elements of another is not completely ruled out, but it is sharply
limited in a manner to be detailed. The solution to the immediate
problem is that

**Merge over Move **holds *only for elements of the same subarray*.

Lexical Array = \{\{C, T\},

\{v, be, reason, there, to, believe\},

\{that, will\},

\{many, people, v, be, at, the, party\}\}

The composition of the various subarrays given here will not be entirely
uncontroversial, but they serve to illustrate the proposed mechanism,
which is that at the juncture in the derviation when **Merge over Move
**could force **Merge **of *there *in place of **Move**-ing *many
people*, the derivation does not have access to *there*.

Of course, nothing *prevents *inclusion of *there *in the relevant
subarray:

16) 1.  1.  There is reason to believe that there will be many people at
            the party.

Lexical Array = \{\{C, T\},

\{v, be, reason, there, to, believe\},

\{that, will\},

\{there, many, people, v, be, at, the, party\}\}

But it is telling that including it doesn’t obviate the requirement for
the second, independent *there *in the higher clause. The higher and
lower clauses are in an important sense syntactically independent of
each other — constructed separately from independent pools of lexical
resources. Contentful lexical items which contribute to the meaning of
the expression may be shared between segments, but items introduced for
purely grammatical functions — such as expletives are included only to
satisfy the needs of their domain. Defining such domains precisely is
the aim of phase theory.

## <span id="anchor-16"></span>Transfer

Phases were introduced to explain an ordering constraint, but that is
not the only work that they do. They additionally serve to limit access
by later operations to portions of the syntactic object already
assembled, and in this capacity they can be leveraged to explain
otherwise stipulative reconstruction effects.

It is well-known that anaphoric binding interacts with displacement in
expressions like the following (examples from (Boeckx and Grohmann
2007)):

16) 1.  1.  \*John<sub>1 </sub>said that Sue likes pictures of
            himself<sub>1</sub>.
        2.  Which pictures of himself<sub>1 </sub>did John<sub>1
            </sub>say that Sue likes?

Example (8) is straightforward: *himself *should refer to *John*, but it
cannot because *Sue *intervenes as a “closer” potential binder. The
*φ*-feature mismatch between *Sue *and *himself *(*Sue *is a feminine
binder, but *himself *must be bound by a masculine antecedent) renders
the binding impossible, and the derivation crashes.

(9), by contrast, is a bit of a puzzle. By assumption, an antecedent
must stand in some kind of superiority relation to its bindee —
c-command, dominance, or something of the sort. However, the bindee
*himself *would seem to be in the superior position with regard to *all
*its potential binders. The only way to save the assumption would be to
allow binding to resolve at some point in the derivation before *Which
pictures of himself *has moved to the left edge of the expression (or
else allow binding to resolve after movement — perhaps at the interfaces
but over traces/unpronounced copies of the moved item). But at first
blush, this kind of approach merely reintroduces the problem in (8) as
the best-motivated “trace” position for *Which pictures of himself *is
as the **complement **of *likes*.

16) 1.  1.  Which pictures of himself<sub>1 </sub>did John<sub>1
            </sub>say that Sue likes which pictures of
            himself<sub>1</sub>?

*Sue *will again be the closest potential binder, and the binding will
fail as before.

What seems to be required is for *which pictures of himself *to also
exist in some intermediate position in the derivation — somewhere lower
than *John *but higher, in some sense, than *Sue*. And indeed, this
seems intuitively correct. The central puzzle here is, after all, what
it is about *displacing *the *wh*-phrase that permits a binding
resolution that was otherwise impossible; the explanation should involve
movement.

10\. Which pictures of himself<sub>1 </sub>did John<sub>1 </sub>say
which pictures of himself<sub>1 </sub>that Sue likes which pictures of
himself<sub>1</sub>?

The trouble is motivating such movement. However well-aligned with the
empirical facts, it isn’t very conceptually satisfying to simply note
that intermediate landing sites exist. Minimalism is founded on the
notion that the computational system shouldn’t do anything it doesn’t
strictly have to, and intermediate landing sites would seem to fall into
that category.

“Would seem to” but for the fact that there is already some independent
motivation for phases. The system needs some mechanism to account for
**Merge over Move **facts; if that same mechanism also helps explain
intermediate landing sites, all the more reason to adopt it.

(Chomsky 2000) does just that, motivating phases in part by appeal to
notions of economy. If phases are the transfer points — points where
assembled material is “shipped” to the interfaces — then they serve to
restrict the domain of syntactic operations. A given operation need not
consider the entire derivational tree, as the parts of it that are
“known” to be complete can be removed from the workspace. This
hypothesis is made concrete in the **Phase**

**Impenetrability Condition **(as defined in (Chomsky 2001)):

**Phase Impenetrability Condition**: The domain of H is not accessible
to operations at ZP; only H and its *edge *are accessible to such
operations.

ZP, in this context, is meant to be the \[next\] smallest strong phase —
that is, the next phase head that c-commands H in the course of the
derivation. So, the assumption is that anything that is **complement
**to a phase head is inaccessible to further syntactic operations after
a higher phase head has been merged in. If there are unvalued
uninterpretable features in this domain at this point, the derivation
crashes. This has the effect of keeping the derivation immediate: by
narrowing the search space, and thus the range of options, the
computational system can more quickly determine whether a derivation is
worth proceding with or should be terminated than would be the case if
it had to consider the full range of already-**Merge**d lexical items.

The relevant point for the present discussion is that it is the *domain
*of the phase head that is transfered to the interfaces. The “edge” and
the head itself remain available. If this view of the system can be
maintained, the need for intermediate landing sites is clear: without
them, movement to the operator position at the left edge of the
expression would be impossible. Put differently, it is a requirement of
the system that syntactically “active” items remain in narrow focus, and
short-move displacement to intermediate landing sites along the edge of
the phase to escape transfer are the mechanism by which they are kept
visible.

Of course, it remains to be explained why the system should be
constructed this way. It seems correct to say that the otherwise
mysterious existence of intermediate landing sites gains some cachet
once there is independent reason to believe in (something like)
*phases*, but this does nothing to explain why *phases *operate the way
they do — permitting access to their left edge, but not their
complements — or why they should exist at all.

## <span id="anchor-17"></span>The Left Periphery

Broadly speaking, researchers have come to terms with the special active
status of items in the left periphery of a *phase *in three ways:
denial, acceptance and reanalysis.

The **denial **approach argues that the special status of the left
periphery is an epiphenomenon: items **Merge**d to the left will be
structurally higher than items in the **Complement**, and as such are
naturally more visible to outside operations anyway. It’s not that
access to the **Complement **is completely ruled out so much as just
computationally more difficult, as there are, almost by definition,
intervening elements between any **Probe **and a potential
**Comp**-situated **Goal**.

The standard-bearer for this approach is (Fox and Pesetsky 2005). This
work takes the view that there is nothing to explain about why the
periphery should be more accessible than any other part of the *phase
*for the simple fact that *everything *in a lower *phase *is in
principle accessible. The traditional distinction between **SpellOut —
**as a PF-only sequentialization process — and **Transfer — **as an LF
process that reads semantic relations from the assembled structure — is
maintained, and any computationally salient effects of *phases *exist to
ease the burden on **SpellOut**.

Syntactic tree structures are hierarchical in nature and do not by
themselves establish precedence relations. Indeed, the existence (and
ubiquity) of displacement phenomena in natural language puts tree
structures into tension with precedence relations, as items can be and
frequently are attached to multiple positions in the hierarchy, making
the mapping to any strict sequential precedence relation problematic.
The physical utterances that represent tree structures, however, adhere
to strict sequentiality between realized items, with an item articulated
only once in the general case no matter how many places it occupies in
the hierarchy (see (Felser 2004) for documented exceptions, however),
and typically in the sequential position naturally corresponding to the
*highest *hierarchical position it occupies (but see (Boskovic and Nunes
2007) for counterexamples). **SpellOut **is the PF process responsible
for establishing these relations.

*Phases *ease the burden on **SpellOut **by “pre-compiling” precedence
relations. At the end of a phase, ordered pairs are established between
each of the items involved, according to where they sit in an *in-order
traversal*<sup>*\[7\]* </sup>of the tree. Once established, these
relations are inviolable — circumventing them causes chaos at the
articulatory interface, and illegibility at an interface is Minimalism’s
analogue to “ungrammaticality” in other frameworks. This constraint is
codified in a **Linearization Preservation **principle:

The linear ordering of syntactic units is affected by Merge and Move
within a Spell-out Domain, but is fixed once and for all at the end of
each Spell-out Domain.

The authors believe this principle is what underlies Holmberg’s
Generalization (Holmberg 1986):

Object shift of an element *α *from the complement domain of a verb *β
*occurs only if *β *has moved out of VP

Concretely:

~~~~

~~~~

*Jag kysste henne inte *(“I didn’t kiss her”)

If the object is going to “shift” out of **VP — **to a hypothetical
“object agreement phrase” **AgrOP **or whatever the analysis in
question requires — it can only do so if the sequential ordering
relations established at the last phase are preserved. Since *v***P **is
a phase by hypothesis, the relative SVO ordering between subject, object
and verb established by that point in the derivation has to surface in
the final **SpellOut **of the expression. The subject must precede the
verb and the object, and the verb must precede the object. The negation
head *inte*, by contrast, is not ordered with respect to the subject,
verb and object at the (*v***P**) phase level. It will be ordered at the
**SpellOut **of the next phase up: **CP**. Items are free to reorder
with respect to *inte *at this point, but they may not reorder relative
to each other. In this system, everything in VP is fully visible and
accessible at the **CP **phase level, even though **VP **is

**Complement **to a phase head (and as such would be transfered to the
interfaces in more standard phase systems, rendering it inaccessible for
further operations). There is therefore no problem with **AgrO
**“seeing” *henne *or attracting it to its **Spec**. The only
constraint imposed by the lower phase on the ordering of *henne *is that
by the end of the present phase (**C**), *henne *must still be lower in
the hierarchy than *kysste *and *Jag — *as indeed it is.

The crucial point is that this system makes no codified distinction
between the subject *Jag *and the object *henne *with respect to this
requirement. The fact that *Jag *appears in the periphery and *henne *in
the core of **VP **is of no formal consequence. The phase encompasses
the entire phrase.

The **acceptance **approach takes the opposite tack, treating the phase
edge as indeed special and leaving explanation of this fact as a bit of
an open question. To the extent explanations are offered, they tend to
be conceptual. For example, (den Dikken 2014) justifies it with a
(somewhat circular) appeal to necessity: if there were no escape hatch
at the periphery, no derivation would ever succeed. If a phase, in
essence, is a unit domain for the purposes of interaction with the
interfaces, then (nearly) every derivation would crash for want of a way
to eliminate remaining uninterpretable features. Any uninterpretable
features which cannot be eliminated in the phase proper — and there are
nearly always such features, as they are the source of the derivational
engine — will need to be eliminated in the extended derivation. That
phrases seem to organize themselves into a core — **Head **and
**Complement — **and a periphery — (a variable number of)
**Specifier**(s) — is simply optimally compliant with these independent
requirements. If the system weren’t set up in this or some similar way,
it wouldn’t work.

This sort of approach is by far the most popular, and it tends to
embrace — again, out of necessity — what has come to be called the
**PIC**<sub>2 </sub>or the **Weak Version **of the **PIC**. In the
original formulation of the **Phase Impenetrability Condition **of
(Chomsky 2000), the

**Complement **to a phase head was spelled out at the merger of the next
phrase head:

In phase *α *with head H, the domain of H is not accessible to
operations outside

*α*, only H and its edge are accessible to such operations

This proved to be overly strict, however. Among other things, it would
seem to rule out the object shift derivation given above. At the point
where *inte *is merged in, items in *v***P **are transfered and no
longer available for syntactic operations, making it impossible for
**AgrO **to attract the object *henne*, since it is not at the phase
edge<sup>\[8\]</sup>. For this and other reasons, the definition was
modified in (Chomsky 2001) so that the **Complement **remained
accessible until the merger of the next **strong phase head**:

The domain of H is not accessible to operations at ZP; only H and its
edge are accessible to such operations.

With this definition, where **ZP **is the next *phase*, the object shift
derivation above is possible: *henne *is visible to all operations up to
the point where **C **is **Merge**d (with **TP**). Since **AgrO **is
**Merge**d below **C**, *henne *is still available for attraction to its
**Spec**.

It is really only the conceptual emphasis which is different between
**denial **and **acceptance**. The Fox and Pesetsky version avoids a lot
of technical complications, but at the expense of committing itself to a
philosophical claim which might not pan out. The claim here is that the
conceptual and articulatory interfaces are highly independent, with the
conceptual interface operating over the entire assembled structure
(which is why narrow syntax retains access to structures assembled in
previous phases), and only the articulatory interface requiring
incremental computation. This is insightful if it turns out to be true,
but there are reasons to be skeptical. Phases seem at least as
conceptually separable as they are phonetically, after<sup> </sup>all.
It seems plausible the *v *phrase and the **C **phrase are
grammatically/conceptually special, functioning as syntactic “kernels”
around which the derivation might organize itself. The idea that they
would be isolable in any articulatory way that other phrases are not
seems a bit less solid.

The more standard approach — the **acceptance **approach — has the
baggage of a number of unexplained technical add-ons. It’s not clear why
the grammar should wait until the *next highest phase *to spell out the
previous phase, nor why it should then split it in half and spell out
only part of it. These feel like stipulations. But as a tradeoff for the
more stipulative feel, the **acceptance **approach can remain agnostic
about how the interfaces work, which seems advisable at this stage in
the development of Linguistic science. Interfaces are, after all, a
theoretical construct — a mere placeholder for something Minimalist
researchers *expect *to find when Biological science has advanced far
enough to confirm or deny their existence. For now, they remain
necessarily vague, and speculation about exactly how they operate is
perhaps best avoided until more direct examination is possible.

For researchers unsatisfied with the stipulative feel of the standard
approach but unwilling to wander too far into speculation about the
nature of the interfaces, the best option has been to try to clarify the
definition of *phase — *a **reanalysis **approach. (Richards 2010) forms
a prominent example.

The central question of that work is of what constitutes a *phase — *how
does the system know where the boundary is? There are essentially two
possibilities here, corresponding to early and late conceptions of the
*phase *in the work of Noam Chomsky. In earlier work, Chomsky’s phases
were defined by the lexical subarrays the **Merge over Move **principle
motivated. The phase was the subarray, and the subarray defined the
phase. How subarrays came to be composed was a question for later
research (Chomsky 2000; Chomsky 2001), an approach heavily criticized as
circular and unenlightening (see e.g. (Boeckx and Grohmann 2007)). As
research progressed, Chomsky became more convinced of the idea that
phase heads simply *are *the core syntactic engine, concretely realized
as a condition by which *only *phase heads bear uninterpretable
features. Since “all syntax” happens around phase heads in this system,
lexical subarrays become almost redundant: a *phase *is the phase head
and what it selects, and nothing more is needed (Chomsky 2008).

On close examination, this approach neither eliminates the circularity
problem nor brings the field any closer to understanding the mysterious
edge condition. As (Richards 2010) notes, there is no meaningful
*conceptual *difference between defining a phase as whatever a phase
head selects and organizing the lexical array into subarrays. Either
way, the phase head is the defining kernel and is grouped with a
(limited) number of items that either do or don’t meet its
specifications.

But if there is no meaningful difference on the conceptual level, it can
still be the case that one or the other is more revealing as an
implementational model. They may be mere notational differences, but
notation that is well-suited to its target can be illuminating.

In this spirit, (Richards 2010) prefers lexical subarrays because they
focus attention on the *grouping *aspect, more clearly raising questions
about how the groups are chosen. The first insight this yields is that
the difference between the two definitions of the **Phase
Impenetrability Condition **given above reduce to a difference in how
**T **is grouped.

Recall that in the **Strong Phase Impenetrability Condition —
**sometimes called **PIC**<sub>1 — </sub> the complement to the phase
head is spelled out as soon as the next *phrase *head is merged — that
phrase be what it may:

In phase *α *with head H, the domain of H is not accessible to
operations outside

*α*, only H and its edge are accessible to such operations

As noted above, this definition is empirically problematic in a number
of ways. In addition to preventing certain approaches to object shift,
it also blocks any chance that **C **would have to interact with the
object in examples like the following (adapted from (Citko 2014)):

~~~~

~~~~

~~~~

**C **seems to need to be able to have access to features on the object
of the verb (*what*), and yet it can’t do so as long as the object is
buried in a spelled-out **Comp — **vP. One could get around this by
having the object adjoin to the left of *vP *(as illustrated), but it’s
not clear what would motivate the adjunction, as this is not a canonical
object position and so doesn’t seem a likely target for A movement.
Moreover — such adjunction blocks agreement between the subject
(*parrots*) and **T**. Analyses that involve an *AgrO *do not overcome
the difficulty: the complement of a spelled-out *v *phase is as opaque
to one type of higher-up phrase as another. **AgrO **doesn’t have any
special privileges here.

But if the so-called **Weak Phase Impenetrability Condition —
**sometimes called **PIC**<sub>2 — </sub>holds, the problem vanishes:

The domain of H is not accessible to operations at ZP; only H and its
edge are accessible to such operations.

Here, **ZP **refers to the *next highest phase — ***CP **in the case
where **H **is *v*. Since **T **is not a phase head, and since **T **is
lower in the hierarchy than **C**, the **VP Complement **of *v *remains
accessible to it — crucially including access to the
object<sup>\[9\]</sup>.

(Richards 2010)’s insight is to note that this is functionally
equivalent to simply including **T **in the lexical subarray with *v*.
Schematically, it amounts to a difference between this:

**Strong PIC**: \{C, T\}, \{v, V\}

and this:

**Weak PIC**: \{. . . C\}, \{T, v\}, \{V. . . \}

Furthermore, the idea that the only the “periphery” of the phase — that
is, its **Spec **and the phase head itself — should be accessible to
**Probe**s of higher phrases, but not the **Comp **falls out of this
grouping. The **Comp **of *v *here is the result of the completion of
operations on **V **and whatever else finds itself in the same lexical
subarray. **VP **is merged as **Complement **to *v *only after its cycle
has completed; *v *selects this assembled object as its internal
argument, and the internal argument remains active/accessible so long as
*v *is — that is, until the *v *phase completes. This provides a kind of
answer to why it should be the **Complement **of a phase head that is
spelled-out: it is because the **Complement **always originates in a
separate<sup> </sup>lexical array.

## <span id="anchor-18"></span><span id="anchor-19"></span><span id="anchor-20"></span>Feature Inheritance

Especially conceptually attractive in ruminations about *phases *is the
idea that *all and only *the phase heads have
*uninterpretable*/*unvalued *features. The philosophical appeal is
clear: to the extent that phases are (relatively) syntactically
autonomous, it is implementationally risky to place syntactic drivers
outside of the heads that mediate these boundaries. If phases are
demarcated by phase heads, and if phases are the drivers of syntactic
operations, and if syntactic operations are driven by *unvalued
*features, then phase heads alone should determine what “gets driven” in
their domain. The only way to implement this in a system driven by
lexical features is to confine the driving features to phase heads. For
once, definitional circularity pays off: if phase heads are the drivers
of syntactic operations, and if uninterpretable features are what drive
syntactic operations, then phase heads must be the heads that come with
uninterpretable features.

Conceptually appealing as this is, however, it leaves the program
without an account for **T**. **T **pretty clearly drives syntactic
operations, responsible as it is for verb positioning and subject
marking. **T **seems to need to be a phase head in practice but not in
concept.

(Chomsky 2008) proposes **Feature Inheritance **as a way of having this
particular cake while still eating it. **T **is not a phase head, but it
*acts like *one as soon as **C **is merged insofar as **C **transfers
its syntactically active features to it.

While the details of the mechanism for this transfer remain muddy, it
does have a number of empirical points in its favor. Since **T **does
not acquire its driver features until **C **merges in and completes the
phase, there is no question of *ordering *between **C**-driven and
**T**-driven operations. Rather, all operations happen “simultaneously”
in “phase time.” And if this is so, some nagging timing questions can be
put to rest.

### <span id="anchor-21"></span>Holmberg’s Generalization

For one, the countercyclicity in Holmberg’s generalization vanishes.
Holmberg’s Generalization was a fact about object shift that seemed to
be ordered “backward.” From the original (Holmberg 1986):

Object shift of an element α from the complement domain of a verb β
occurs only if β has moved out of VP

That’s all very well for a framework like *Government and Binding Theory
*which allows free movement, but the Minimalist Program’s grounding in
pairwise **Merge **entails that structure-building operations be
ordered. The paradox, then, is this: object movement is allowed only
after verb movement has succeeded, but once verb movement has succeeded
it’s too late for the lower object to move.

With the implication of feature inheritance that phases form some kind
of domain of simultane- ity for otherwise-ordered operations, however,
this concern can be laid to rest, and Holmberg’s Generalization ceases
to be a countercyclic misfit.

### <span id="anchor-22"></span>Subject Marking

Another formerly vexing ordering paradox that need no longer concern us
after the move to feature inheritance is the question of how the subject
makes it to **Spec**-TP at all. On the assumption that only the edge of
a phase head — and not its interior — is visible to operations at the
next phase level, both the subject and any **C**-bound *wh*-phrase
object must occupy **Spec**-*v***P **at the time **T **is merged.
Moreover, on the assumption that **Spec**-*v***P **is the subject’s

*θ*-position, the *wh*-phrase object is likely higher, as it was
adjoined later, having been moved from **Comp**-V\[10\]<sup> </sup>after
the (soon-to-be) subject’s initial **Merge**. If true, this would imply
that it blocks any **T Probe **hoping to receive *φ*-valuation from the
external argument — as it is itself a nominal category — which in turn
means that the external argument’s Case features will never be valued,
and the derivation will crash. This may even be true even under systems
that treat all **Spec**s as equidistant as it’s not clear that the **T
**probe can “pick and choose” from an array of similarly-situated items.

Under **feature inheritance **this problem can be made to go away in one
of two ways.

First, on the assumption that the *wh*-object and the external argument
were not already equidistant by virtue of both being specifiers (and on
the further assumption that equidistance obviates intervention), the
effective collapse of **C **and **T **into a single category through
feature inheritance makes the entire phase domain a “drop in time” for
the purposes of these operations. If **C **and **T **act like a single
lexical item, as per (Chomsky 2008), then all syntactic drivers of the
phase are unordered relative to each other, and operations can proceed
as makes sense. Whether or not the (soon-to-be) subject and *wh*-object
are ordered relative to one another, the **C**-**T **complex can try its
probes in whatever order works out.

Second, it could instead be that the **Probe**s on **C **and **T **are
still ordered, but by virute of **feature inheritance **the order is the
opposite of what their relative hierarchical positions<sup> </sup>would
imply. It all depends on the ordering of **Inherit **relative to
**Probe**. If **Probe **immediately follows **Merge**, as seems
reasonable, then **C **may **Probe **for a *wh *match *before ***Inherit
**passes its *φ *and Case features to **T**. **C**’s **focus **probe
finds and attracts the *wh*-object, which is displaced to the left edge
of **CP**. This leaves no intervener between **T **and the external
argument of *v***P **after **Inherit **completes.

As a motivation for the otherwise stipulative **Inherit**, this is of
course appealing, but it does beg the conceptual question of how to
*prevent *the active *φ *probe from attracting the subject to
**Spec**-**CP **before **Inherit **has a chance to work. The analysis is
based in the idea, after all, that **Probe **precedes **Inherit **in
operational order.

The answer is probably something like one or both of the following:

1.  **Inherit is Probe**. Whatever *probe *goes in search of the subject
    will have to pass through **TP **anyway. Whatever mechanism
    entangles **C **and **T **to allow **feature inheritance **might as
    well fire at this point as on **Merge**.
2.  On **Merge **and subsequent **Inherit**, **C **and **T **are no
    longer entirely separate entities, but instead behave as though they
    had been merged as a single lexical item<sup>\[11\]</sup>. If that’s
    the case, there is no meaningful difference between the *φ *probe
    originating from **C **or from **T**. **Inherit **simply changes
    which part of the complex acts as the site of attraction for those
    features, and it doesn’t actually matter where they originate from.
    Put differently, in **Inherit**-ing features from **C**, **T **also
    inherits whatever they attracted. It would be tempting here to say
    that this implies that the ordering of the subject below the *wh
    *landing site is yet another PF epiphenomenon. It isn’t so much that
    **T**, *per se*, inherits *φ *and Case as that associating *φ *and
    Case with **T **in the complex instructs PF to order their
    associates after the associates of features on **C**. But this is
    probably not right. Subject is ordered below **Operator ***in the
    hierarchy*, and not just for purposes of **SpellOut**. So,
    **Inheritance **means just that: **T **receives the features, and
    whatever is associated with them.

## <span id="anchor-23"></span>Summary

Phases are a bit of a problematic category in Minimalism. Though they
play a large role in modern analysis, it is not always entirely clear
what purpose they serve. More accurately, they seem to serve several
seemingly disparate ones. In one role, they are the delimiters of
*locality*. *Phases *define (relatively) independent syntactic domains.
In another role, they *punctuate *interpretation. Interpretive functions
in Minimalism are served by appeals to reconstruction effects, and
*phases *both delimit where those effects are observed and, on some
accounts, justify their existence. In yet another role, they are the
drivers of syntactic operations. There is a conspicuous division of
lexical items — and lexical features — into those that provide
interpretive substance, and those that drive operations. Phases reflect
this distinction by organizing the derivation into suboperations around
syntactic drivers. In still another role, they play a part in accounting
for the distribution of grammatical formatives like expletives. In a
final role, they provide *ordering *constraints, requiring that some
operations take place before others.

Implementation need only allow for building analyses compatible with
those prominent in the field. So long as it provides the means, it need
not share all of the philosophical commitments. In this spirit, it is
probably best to separate the disparate concerns bundled in *phases*, as
they seem ripe for separation. To the extent that things are
conceptually separable, an implementation should allow them to be
separated in practice.

As will be seen in Chapter 4, this system does not provide a *phase
*primitive. Rather, it addresses the implementation of (phenomena
associated with) *phases *in two separate ways.

On the *locality *side, it leans on Agree in a manner to be detailed in
Chapter 3. To give a preview, if Agree is conceptualized as a *valuation
*(or, if prefered, a *specification*) process, rather than a checking
process, probes can be bounded by choice of goal feature. A *phase
boundary*, then, is simply a “universal goal” — a goal that matches (and
therefore blocks) every conceivable probe, rendering items below the
head bearing the feature in question inaccessible.

On the *system architecture *side, this implementation provides
***lexical array***s which bundle lexical items for subprocessing. This
allows implementors to enforce ordering constraints by grouping items in
determined ways. Additionally, in a manner that gains clarity in
Chapters 4 and 5, by taking feature inheritance — as outlined above —
quite literally, the system can enforce domains of operations that span
beyond the phrase boundary. Providing lexical groupings in the form of
arrays is arguably a reimplementation of the notion of *phase *by other
means, as these groupings *are *architectural primitives\[12\]<sup>
</sup>in the system. If the reader prefers, it is not unfair to say that
this system commits itself to a very weak notion of *phase*, in which
every subgrouping (in most cases, every phrase) is a *phase*.

*Phases*, it will ultimately be argued, are an epiphenomenon — a
bundling of disparate primitives into a questionably motivated category.
As they pervade modern Minimalist analysis, however, it is important for
any implementation to survey them, and the motivations for postulating
them, and ensure that all associated phenomena are covered by other
means. That has been the purpose of this chapter.


[Back](jherring-1) — [Forth](jherring-3)
