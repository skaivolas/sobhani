---
title: Grammar Construction in the Minimalist Program — Chapter 3 — An Overview of Agree
layout: page
---

[Back](jherring-2) — [Forth](jherring-4)

# <span id="anchor-24"></span>Chapter 3 — An Overview of Agree

## <span id="anchor-25"></span><span id="anchor-26"></span><span id="anchor-27"></span>Motivation

Jargon is a common barrier to entry to any field. The inarguably
indispensible economy and precision of communication it affords
professionals keeps amateurs at bay, unable to even receive instruction
in the field’s latest insights without some re-education in how to use
superficially recognizable words. Minimalism’s reductionist heritage
virtually guarantees that this problem is worse for it than for other
branches of Lingusitics. The commitment to leveraging directly
observable processes to power even the most hypothetical of
un-observables (or at-most-indirectly-observables) necessarily results
in putting formerly familiar terms to counterintuitive use. While
**Agree **isn’t the worst offender on this front, it’s hard to deny that
Minimalism uses agreement phenomena for things well outside their normal
bailiwick.

Ask anyone, and he knows immediately what *agreement *means: it’s that
thing verbs do where they change their form based on the subject. If the
subject is 3rd person, add an *-s*, or maybe an *-es*. Otherwise, don’t.
For speakers of morphologically richer languages than English, it might
also be that thing adjectives do where they are pronounced differently
based on the class of the noun they modify. Whatever the domain, in
ordinary use, *agreement *is some flavor of pronunciation rule employed
to reflect already-understood relationships between words. As such, it’s
perhaps useful in a communicative sense, but it’s also ultimately
superficial.

Like with so much else in Minimalism, the minimalist researcher sees
this “backward.” If there is a pronunciation reflex, there must be a
process that results in it. And if pronunciation is superficial, the
process is not. Since the process exists, attributing things to it is
“free” — at least in the sense that we know we’re not multiplying
entities. Soon enough, by extended analogy, *everything *that involves
establishing relationships between words is attributable to (the process
that underlies) *agreement — *now called **Agree **(perhaps to mark the
departure) — even if there no direct alteration in pronunciation
associated with the relationship. What started as a reflex is now the
cause. If **Merge **underlies the assembly of complex syntactic objects
from atomic ones, **Agree **mediates the consequences of such
combinations: what the side effects are, and whether they are licit at
all.

## <span id="anchor-28"></span><span id="anchor-29"></span><span id="anchor-30"></span>Feature Checking

In the early days of Minimalism, accounting for “whether \[given
combinations\] are licit at all” was really all **Agree **did. The
foundational principles of the Program allowed for nothing else. These
principles included<sup>\[13\]</sup>:

**Inclusiveness Condition **No new features are introduced in the course
of linguistic deriva- tion

**No-Tampering Condition **No elements introduced by syntax are deleted
or modified in the course of linguistic derivation

The **No-Tampering Condition **ruled out the idea of *valuation*. If an
item — a verb, say — reflected *agreement *with a subject in its
pronuncation, then only because it had been selected from the Lexicon
with the features that specify that type already present. Anything else
would be *tampering — *altering the makeup of an item by adding feature
specifications that were not there before. As a consequence, a Lexicon
could be expected to contain express<sup> </sup>entries for *every
morphological alternation of a given item — *quite a storage memory
burden for morphologically rich Lexicons.

Enforcing what (Preminger 2014) terms “The Obligatoriness of Agreement”
— the observation that some morphological combinations<sup>\[14\]
</sup>are illicit — was a matter of *checking*. **Agree **simply
identified whether two items were structurally in a relevant
relationship with each other and then *check*ed whether that
relationship were allowed. It was not the case that, on encountering a
third-person, singular subject, the verb would alter its form to reflect
this relationship — the verb was either third-person and singular to
begin with, or the combination with the subject failed to succeed.

The **Inclusiveness Condition **ensured that **Agree **had no meaningful
side effects. Once a feature had been *check*ed, the best that could
happen is that it be marked as such, perhaps through
deletion<sup>\[15\]</sup>. Valuation of underspecified features —
something that would become standard in Minimalist theories after
(Chomsky 2001) — was rejected out of hand. Again, a verb agreeing with a
subject did so not because establishing the relationship with its
subject had altered its form in any way, but because it just so happened
to be the variant of the verb from the Lexicon that is capable of
combining with that subject.

This approach to **Agree **lives on in the project by Ed Stabler and
colleagues to give a formal specification for Minimalist Grammars.
Starting with (Stabler 1997) and continuing to the present
day<sup>\[16\]</sup>, *Minimalist Grammars\[17\]*<sup> </sup>represent
features in terms of two oppositions: between *select *and *category
*features and between *licensor *and *licensee *features. Each pairing
is divided according to polarity, with a *select *feature pairing with a
matching *category *feature, and a *licensor *feature pairing with a
*licensee *feature. Features that match in type and bear opposite
polarity correspond directly to the checking relationship of (Chomsky
1995).

## <span id="anchor-31"></span><span id="anchor-32"></span><span id="anchor-33"></span>Valuation — a Rethinking

Feature checking is no longer, however, the standard approach among
Minimalist researchers. Starting with (Chomsky 2001) and slightly
before, the working paradigm shifted to one focused instead on
*valuation *for a variety of mostly conceptal reasons. For one thing, it
was recognized that a massively redundant lexicon, containing entries
for potentially large numbers of slight variations on individual items,
was not very “minimalist” in spirit. Instead, it should be
reconceptualized in “Bloomfieldian” terms — meaning here as the smallest
possible list of “exceptions,” i.e. unique properties of an individual
item that distinguish it from others.

*In any case, we can think of LEX as in principle “Bloomfieldian,” a
“list of exceptions” that provides just the information required to
yield the interface outputs, and does so in the best way, with least
redundancy and complication. *(Chomsky 2001)

For another, there was some discomfort with the tension, mentioned
earlier, between the **No-Tampering Condition **and the founding idea
that Syntax is driven by the need to remove interface-illegible
material. It seemed incongruous that the evolutionary development of
human linguistic systems would proceed by producing featural objects
that were specifically<sup> </sup>illegible at the interfaces to the
presumably prelinguistic systems with which *C*<sub>HL </sub>aimed to
integrate.

*It is as if formal features like case and agreement appear in syntax
only to be wiped out before syntactic elements are interpretable
*(Boeckx 2008a)

The idea that features are universally composed of a type or category
and a value specification for that type, and that what Syntax needed to
“repair” among lexical items before they could be interpretable in
combination at the interfaces was underspecification in the value, was a
much more comfortable fit. A thing that can in principle have a value
but lacks one just seems more like the kind of thing that an interface
would have trouble “reading” — as opposed to something expressly marked
“unreadable” — and so “uninterpretable” came to mean “unvalued.”
Moreover, it fit in well with competing approaches to grammar, such as
HPSG, which were driven by feature unification. Mechanisms available to
those approaches that had enjoyed some analytical success thus became
available to Minimalist researchers in their own program.

## <span id="anchor-34"></span><span id="anchor-35"></span><span id="anchor-36"></span>Mechanisms — Spec-Head and Probe-Goal

Whether valuation or checking, however, both are mere end results of the
operation that is actually under investigation. Having observed that
Syntax is at heart about lexical item combination, that some
combinations are licit while others are not, and that some licit
combinations of a given bag of items have one interpretation and others
another, the work to be done involves investigating these
structure-building operations. If **Merge **exists to combine items and
**Agree **to referee the combinations, then the enterprise of specifying
the grammar of a given language means mainly getting **Agree **right.

The centrality of **Agree **to Minimalist Syntax has its roots in
developments that began before the program itself — specifically in the
articulation of the functional core proposed in the seminal (Pollock
1989). To explain the differences in relative output positioning of
verbs, objects and adverbs between French and English in parametric
terms, Pollock found it convenient that there be a position between
verbal inflection and the (position at which the) verb itself (enters
the derivation) where the object sometimes was realized. Some of the
differences in English and French object positioning could then be
explained partly in terms of whether the object were in this position by
the time PF-relevant information were assembled, or
not<sup>\[18\]</sup>. The hitch came in motivating the
movement<sup>\[19\]</sup>, as there was no obvious compelling mechanism
for it. The most plausible candidate seemed to be case assignment, and
indeed, assuming it were case assignment lent the proposal an appealing
elegance, as it managed to harmonize case assignment strategies. Up to
that point, case had been assigned “under government,” which was, under
the hood, little more than a catch-all term for a variety of dissimilar
structural configurations researchers found it convenient to treat as a
natural class. Under government, subjects were assigned case in a
**Spec**-**Head **configuration (via *m-command*) and objects as the
**Comp **of a lexical head -the verb (under *c-command*, sisterhood, or
perhaps simply initial **Select**). The lack of uniformity was vexing to
a research program born of the need to reduce grammatical mechanisms to
a minimum as an answer to Poverty of Stimulus problems in child language
acquisition. With the introduction of the *Agr *node, this problem could
be overcome: objects raised to a **Spec **position to get/check case
just as subjects did, and only a single type of structural configuration
need be implicated in case assigment.

This general approach flourished in what might be called the
proto-Minimalist Era<sup>\[20\]</sup>. (Chomsky 1991) noted that the
*Agr *head proposed in (Pollock 1989) might reasonably have been above
**Infl **rather than below it, to account for subject-verb agreement in
finite clauses<sup>\[21\]</sup>. And yet, Pollock’s evidence was
convincing that there needed to be a position of some kind *below
***Infl**. The solution was just to have two such *Agr *positions — one
for subjects, positioned above **Infl**, and one for objects positioned
below. Independent evidence seemed to confirm the conjecture: among
other examples, (Holmberg 1986) had noted years before that Icelandic
objects shift out of VP only then when they are case-marked NPs, and
never when they are PPs, thus implicating (case) agreement in motivating
movement. Examples<sup>\[22\] </sup>include:

1)  Nemandinn lasbókinna ekki

student.the read book.the not

"The student didn’t read the book."

1)  \*Jón talaði viðMaríu ekki

Jon spoke with Maria not

"John didn’t speak with Maria."

Likewise, Lasnik and Saito pointed out in an influential presentation
(Lasnik and Saito 1991) that the new *AgrO *position was compatible with
evidence that had been marshalled a decade before to support a
raising-to-object analysis of ECM constructions. From (Postal 1974):

1)  <span id="anchor-37"></span><span id="anchor-38"></span>Joan
    believes that he<sub>i </sub>is a genius even more than Bob<sub>i
    </sub>does.
2)  Joan believes him<sub>i </sub>to be a genius even more than
    Bob<sub>i </sub>does.

*him *would appear to c-command *Bob *in ([4](#_bookmark17)), ruling out
coreference, but the same is not true of *he *in ([3](#_bookmark16)).
The salient difference between the two is Case. *he *has **Nom **by
virtue of being the subject of a finite clause, but *him *must be
case-licensed by some other method. The fact that it appears to be in
the matrix clause for the purposes of binding implicates displacement in
its assignment of **ACC **under ECM.

Movement would seem to be correlated with case licensing. And once a
position was established for object agreement, there was little
objection to (Chomsky 1991) taking the short step of extending this to
subject agreement as well.

This solution — separate *Agr *positions for **Nom**(subject) and
**Acc**(object) case assignment — had the virtue of uniformity, but as a
general program it was ultimately too powerful to be really explanatory.
For a time, every problem looked like the same nail in need of the same
hammer: to account for any sequential ordering phenomenon, it was all
too easy to postulate a(n unpronounced) functional head in whatever
position in the hierarchy would yield the correct output order and
attract the necessary item to it with features stipulated for just that
purpose.

(Chomsky 1995) recognized the problem and took some steps to reining it
in. Functional heads assembled exclusively from features that cannot be
interpreted and were not pronounced were declared suspect. The *Agr
*heads had to go. Object shift was eventually reanalyzed as movement to
**Spec**-*v*P. Furthermore, displacement for the purpose of realizing
agreement was ruled uneconomical. If the agreement process can target
subparts of an item — i.e. only those features implicated — why should
movement (copy-and-remerge) be any different? The agreement relationship
is only between a pair of features, not a feature and a lexical item
*per se*, so only the implicated feature should move. Cases where the
whole category moved overtly as a reflex of **Agree **were relegated to
the need to satisfy EPP features on the target, an explanation which is
essentially a promissory note to report back when further investigation
has uncovered the real cause. It did, however, have the effect of
decoupling displacement from case/agreement, essentially speculating
that such displacement is motivated by independent morphological or
articuatory interface necessity.

As philosophically unsatisfying as jettisoning the uniformity afforded
by tying agreement to **Spec**-**Head **relations seemed, the move came
with a number of empirical virtues. Divorcing **Agree **from any local
configuration allowed it to happen at a distance, which captured a
number of other facts in a wide variety of languages. Prominently, it
retired longstanding puzzles about the agreement of expletives with
their associates and loss of inverse scope under VP-fronting as well as
opened the door to more intuitive explanations for quirky case and
long-distance agreement phenomena.

Expletive Replacement

Expletives agree with their associate NPs in existential constructions
in a way that is difficult to ascribe to movement.

1)  a. There are/\*is three men in the car.
    
    2.  They are/\*is one and the same element.

The verb in these examples\[23\]<sup> </sup>agrees with something to its
right and not with the expletive one finds in the canonical subject
position. Early explanations offered in (Chomsky 1986b) attempted to
reduce this to covert movement — the associate NP raised to subject
position and replaced the existential expletive covertly. However, this
got the scope and binding facts wrong (see (Lasnik 1999) for a full
explanation):

1)  <span id="anchor-39"></span><span id="anchor-40"></span>a. Someone
    from New York is likely to be at the party.
    
    2.  There is likely to be someone from New York at the party.

2)  a. A man<span id="anchor-41"></span><sub>i</sub>seems to
    himself<sub>i</sub>to be doing something wrong.
    
    2.  \*There seems to himself<sub>i</sub>to be a man<sub>i</sub>doing
        something wrong.

Only ([6a](#_bookmark18)) is ambiguous between wide and narrow scope for
*someone *which should not be the case if the two are identical at LF
after replacement. Likewise, *himself *should be bound for the purposes
of Condition A in ([7b](#_bookmark19)) but is not.

Scope Freezing under VP-fronting

A similar example can be found in German, where the fact that a marginal
scope ambiguity disappears under VP-fronting rules out any covert
movement analysis of case assignment. Examples are from (Bobaljik and
Wurmbrand 2005).

1)  <span id="anchor-42"></span><span id="anchor-43"></span>a. weil
    mindestens einem Kritiker jeder Film gefallen sollte

because at.least one.DAT critic every.NOM film please should

"Since at least one critic should like every movie."

1)  2.  <span id="anchor-44"></span><span id="anchor-45"></span>?\[jederFilm
        gefallen\]<sub>VP </sub>sollte mindestens einemKritiker

every.NOM film please should at.leastone.DAT critic

"Since at least one critic should like every movie."

Example ([8a](#_bookmark20)) is mildly ambiguous between wide and narrow
scope for “every Film.” Though glossed here in the sense that there
exists at least one critic who likes every movie, it can also be
interpreted to mean (albeit marginally) that every movie has at least
one critic who likes it. This is not true for ([8b](#_bookmark21)),
which can only have the first interpretation. And yet, *jeder Film *has
**Nom **case in both examples, casting doubt on the idea that covert
movement can be involved in this assignment. (If it were, the marginal
wide-scope reading for *jeder Film *should not be available in
([8a](#_bookmark20)).)

Quirky Case

In some cases, for some verbs, Icelandic subjects fail to agree with the
verb, which instead manifests agreement with an item lower in the
hierarchy — generally the object. Moreover, the target of agreement is
marked — exceptionally — with *nominative *case, and the subject
surfaces in some other “quirky” case — generally *dative*. The following
example (from (Taraldsen 1995)) shows the contrast:

1)  Hennileiddust/?\*leiddist *θ*eir

<sup>her.DAT.3sg </sup>bored.3pl/?\*3sg<sup>they.NOM.pl </sup>"She was
bored with them."

The verb agrees with and values case on *θeir*, rather than *Henni*, the
item that would actually appear to be in **Spec**-T (or whatever
agreement position is postulated), clearly showing that *agreement *is
not always coupled with the structural position canonically associated
with it.

Long-distance Agreement

A number of languages seem to optionally allow agreement between
embedded objects and matrix verbs, in possible (but this is
controversial) violation of standard versions of the **Phase
Impenetrability Condition**. The examples below are for Hindi from
(Bhatt 2005):

1)  a. Ram-nerotiikhaa-nii chaah-ii

Ram.ERG bread.f eat.INF.f want.f.sg "Ram wanted to eat bread"

1)  2.  Ram-nerotiikhaa-naa chaah-aa

Ram.ERG bread.f eat.INF.m want.m.sg "Ram wanted to eat bread"

The optionality is notable, as is the fact that the embedded clause is
non-finite, and therefore not a phase. But the problem isn’t so much
that this can happen across clause boundaries as that it can happen at
all. The identical word order and interpretation between the two
examples belies the idea that there are any consequential syntactic
differences between these sentences: *rotii — *the source of the
nonstandard agreement — would appear to be embedded in the subordinate
TP in both cases. Moreover, there is a subject in the canonical subject
position as well. Like with Icelandic quirky case, the most plausible
explanation is that **Agree **need not confine itself to **Spec**-**Head
**configurations.

Each of these phenoma is difficult if not impossible to model without
decoupling **Agree **from its movement reflex.

In addition to its empirical attractiveness, the move to decouple
agreement from **Spec**-**Head **configurations wasn’t as much of a
theoretical step backward as it initially seemed. After all, on closer
inspection, it’s clear that **Agree\[24\]**<sup> </sup>needs to precede
displacement of the feature- supplying item to the **Spec **of its
attractor in any case, else how does the feature-seeking head know which
item in its **Comp **to target?

Probe and Goal

The hypothesis that **Agree **required a **Spec**-**Head **configuration
to be realized having been rejected<sup>\[25\]</sup>, it was now
necessary to give character to the alternative. Even with the locality
requirement loosened, *agreement *remained a highly constrained
operation. Only certain pairs of items matched for its purposes, and the
intervention effects that had made movement analyses attractive
remained.

Given these restrictions, the new metaphor was straightfoward: there
would be an operation **Agree **in which a **Probe — **a head bearing
(uninterpretable) features in need of a value — would go seeking a
**Goal — **a syntactic obect able to supply what the **Probe **needs
(Chomsky 2000). This metaphor captured the discrimination of the
operation — not all objects encountered along the search path need be
relevant — and of course there’s no trouble imagining that *probe*s can
be interrupted or blocked by elements that match enough to distract but
not so much as to fulfill (so-called *defective intervention*). The
latter aspect allows **Agree **to retain the insights of movement-based
analyses of *agreement*, but it is the former that ultimately<sup>
</sup>preserves the derivational character of the system, as it has been
argued (Abels 2003; Boeckx 2008c) that so-called “punctuated paths” —
the ability for long-distance syntactic operations to “skip” intervening
nodes — is the remaining salient operational difference between
Minimalism and unification-based theories (LFG, HPSG) after GB’s turn to
lexicalism.

Despite the new metaphor and expanded empirical coverage, the
implementational impact of the shift was minimal. The search domain
remains the **Comp **of the **Probe**-ing head, and intervention effects
are as they were before: anything of the right category can interrupt
the probe by (1) being “closest” along the path to other potential goals
and (2) lacking the requisite feature values to satisfy the probe. It’s
in the details of (1) and (2), mostly, that individual Minimalist
approaches tend to differentiate themselves.

Of the two, (2) tends to have a much broader range than (1). While it is
possible to imagine alternatives to hierarchical C-command as a measure
of “distance,” the binary branching structures that pairwise **Merge
**imposes make them awkward. A **Head **selecting its **Comp
**automatically c-commands it and all of the **Comp**’s constituents,
and as these were likewise assembled by a **Head **selecting a **Comp**,
the definition is recursive and applies all the way down the hierarchy.
“Distance” falls quite naturaly out of the **Probe **metaphor: a
**Probe**-ing **Head **inspects the constituents of its **Comp**, each
in turn, looking inside them if necessary, until it hits a match or has
exhausted the search space. Since this process proceeds stepwise,
“closer” can be defined procedurally — whichever nodes come first in
the algorithmically-defined search order are “closer” than those that
come later. Because the fit is so natural, variants on distance
algorithms generally take the tack of defining exceptions — and these
exceptions, in turn, generally involve allowing something that is
technically “further” by the baseline computation of distance to count
as though it were “closer” than the hierarchy would suggest. These are
things like counting **Spec**ifiers (and adjuncts) of a phrase as
“equidistant” for search purposes, even though they were assembled in
some order by pairwise **Merge **and are therefore technically
hierarchically represented. Another such modification is
“restructuring,” which has a long and varied
history<sup>\[26\]</sup>, but also tends to involve “shortening”
distances and removing “barriers” to allow otherwise illicit operations
to go through. See (Wurmbrand 2015) and (Wurmbrand 2001) for surveys of
Minimalist approaches.

Specification of the features involved in **Agree **tends to offer more
degrees of freedom to researchers seeking to capture new empirical
discoveries, and so this is where most of the action will be in
providing a grammar development tool for Minimalism. In the foundational
texts, **Agree **is relatively simple.

A brief overview of **Probe**-**Goal **algorithms found in the
literature follows. This is followed by a cursory overiew of several
phenomena that help define the range over which feature specification
has to work when **Agree **succeeds.

**Derivation by Phase **(Chomsky 2001)

A **Probe **P agrees with a **Goal **G if:

1.  P c-commands G
2.  Both P and G are *active*
3.  P matches a feature of G
4.  The matching feature on P is *unvalued *and the matching feature on
    G is *valued*

Worth noting here is that *both ***Probe **and **Goal **must be *active
*in some sense. This is largely up to the grammar designer, but
generally it means having an unvalued feaure.

**Feature Sharing **(Pesetsky and Torrego 2007)

1.  A **Probe **P is an *unvalued *feature F on a **Head**
2.  Its **Goal **G is a *valued *instance of F in P’s c-command domain
3.  Replace the feature on the P with the one from G

This differs from the (Chomsky 2001) version in establishing a more
direct connection between the two items involved: they actually share
structure.

**Reverse Agree **(Zeijlstra 2012)

**Agree **relates a **Probe **P to a **Goal **G if:

1.  P and G are in a proper local domain
2.  P has an *uninterpretable *feature
3.  G has a matching *interpretable *feature
4.  **P is c-commanded by G**
5.  There is no intervening object carrying the same feature between P
    and G

This differs from (Chomsky 2001) primarily in directionality: Goals
(*valued/interpretable*) c-command Probes (*unvalued/uninterpretable*)
rather than the other way around.

**Parametric Agree **(Baker 2008)

A language may implement only one of the following versions:

A feature F agrees with DP. . .

1.  . . . if F *c-commands *DP
2.  . . . if DP *c-commands *F
3.  . . . if DP *c-commands *F or F *c-commands *DP

In other words, the directionality of **Agree **is parametric.

**Checking **(Chomsky 1995; Adger 2003; Stabler 1997)

An *uninterpretable *feature F is *checked *on a syntactic object X

1.  when X is in a *c-command *relation with another syntactic object Y
2.  which has a matching *interpretable *feature F.

Though now out of fashion, this was the dominant paradigm in the early
days of the Minimalist Program and must be implementable in any
comprehensive Minimalist grammar building environment. Worth noting is
that directionality is free as stated. System can choose to impose
directionality requirements as they wish.

**Polyvalent Agree **(Merchant 2011)

1.  There is a function **Val **that returns the value of a feature F:
    Val(F)
2.  “Unvalued” features F’ can have default values in some languages. In
    this case, Val(F’) returns this value
3.  If a syntactic object X *c-commands *an object Y and X has a *valued
    *feature F with value Val(F) and Y has a matching *unvalued *feature
    F’ with “value” Val(F’), then let Val(F’) = Val(F), Val(F’)

This system is rather complicated and, by admission of the author,
incomplete, as it was designed to deal with a puzzling
phenomenon<sup>\[27\]</sup>. The general idea is that Feature values can
form *nested sets *which respond in various ways to different
environments. The nest- ing allows values to be hierarchical. An
important point is that features — even unvalued features — retain a
record of their past “values”. This makes a nice fit with the Minimalist
Program’s founding principles, since feature values are never destroyed
in the derivation, merely rearranged/reconfigued.

**Feature Inheritance **(Chomsky 2008)

Pursuant to the idea that *all and only *the phase heads of a derivation
bear *unval- ued*/*uninterpretable *features, it was necessary to add a
new tool to the set. T, not being a phase head, could not be the locus
of any derivation-driving features, and yet evidence that it was a locus
of features associated with subjecthood was strong. The solution was to
allow features that are realized in one place to originate in another:
**Feature Inheritance **(as covered in the previous chapter). T would
receive C’s unvalued *φ *and valued *Case*\[*NOM *\] features, allowing
it to function as a **Probe **even though it isn’t lexically equipped to
   be one. This system is best thought of as an extension to the
**Derivation by Phase **approach of (Chomsky 2001). Everything that
applies there applies here, with the following embellishments:

1.  A functional head selecting another functional phrase can transfer
    features to it, provided they are not already specified on that
    head.
2.  Once in this kind of relationship, the two functional heads act in
    many respects as though they are a single lexical item.
3.  The apparent countercyclic movement this gives rise to (the subject
    presumably raises to **Spec**-TP only after the **Probe **appears on
    it) is not countercyclic at all since it happens *within the phase*.

It is the last point that is the innovation relevant to **Agree
**because it forms such a radical departure from the structure-based
concepts of syntactic distance that underlie most accounts of
intervention effects. Everything within the same phase is equidistant,
and subjects and objects both situated at the edge of *v***P **do not
intervene against **Probe**s targeting the other.

## <span id="anchor-46"></span><span id="anchor-47"></span><span id="anchor-48"></span>Relativized probes

To complicate matters, there is some evidence that **Agree **needs to be
*relativized — *in the sense that **Probe **can skip, for the purposes
of **Agree**, arguments that are of the matching category but do not
have the “right” feature values. The motivating example is the Kichean
*Agent-Focus *Construction (Preminger 2014).

**Agent-Focus Constructions in Kichean**

The phenomenon in question applies to constructions where the subject is
focused and works by giving morphological preference to 1st/2nd person
arguments over 3rd person arguments.

1)  Ja yin x-in/\*NULL-ax-an riachin

<sup>FOC me </sup>COM-1sg/\*sg.ABS-hear-AF <sup>the man </sup>"It was me
who heard the man"

1)  ja riachin x-in/\*NULL-ax-a yin

<sup>FOC the man </sup>COM-1sg/\*sg.ABS-hear-AF <sup>me</sup>

"It was the man who heard me"

The focused subject is presumably higher than the object in both
sentences, and yet the agreement probe only ever seems to find the 1sg
argument, regardless of where it is in the hierarchy. In the second
example, *ri achin *(“the man”) should in theory block any attempts by
the verbal *φ *probe to reach the more deeply embedded object *yin
*(“me”), but this is not the case. Similar effects are seen when
both arguments are 3rd person but one is plural and the other singular:
the plural argument “wins” regardless of position in the hierarchy. The
only time 3sg morphology surfaces in this construction is when there are
no other types of arguments. When *both *arguments are 1st/2nd, by
contrast, the construction patterns as one would expect and agreement is
preferentially with the higher argument — the subject.

1/2sg/pl \> 3pl \> 3sg

This example and examples like it justify what Preminger calls
*relativized probe*. Put simply, **Probe **can be sensitive to more than
just the *class *of feature — it can be specified for actual *values *of
features — or at least classes of values. The idea is that there is some
kind of feature geometry — familiar from Phonology — where certain
values of features are represented as subsets of the larger feature
class. A probe can be specialized to look for only features of the
subset. In this case, the **Probe **in AF constructions is specialized
for a more specific subset than just *φ*. Simplifying somewhat, the
probe looks for a subset of *φ *that is specified for \[**author**\] —
the name chosen for “not 3rd person,” more or less. If it does not find
a match, it surfaces in its default form — which is to say, 3rd person
agreement in this construction in this language marks not agreement but
rather a *failure *to agree. The preference for plural over singular is
implemented by assuming separate **Probe**ing heads for **number **and
**person**<sup>**\[28\]**</sup>.

## <span id="anchor-49"></span>Summary

Minimalism admits of only one structure-building operation — **Merge —
**and this operation is in principle unbounded. Any two syntactic
objects can be freely combined into a new structure. Taken in isolation,
this defeats the purpose of grammatical analysis: it is largely the job
of a grammmarian to say what combinations are *not *allowed. This is the
function played by **Agree**. If **Merge **allows any combination,
**Agree **at least defines what the consequences of the combination are.
In a great many cases, the consequences are such that they are not
useable by the interfaces, and this is the locus of grammatical
explanation in Minimalism.

This chapter has shown a progression away from a checking concept of
**Agree **toward one concerned with valuation(/specification). In more
general terms, it is a move away from licensing and toward one concerned
with *effects*. **Agree **records the effects of an operation, and this,
in turn, helps determine whether a given series of operations is
ultimately licit.

Based on a necessarily broad empirical survey, it is clear that a modern
Minimalist toolkit must include a collection of mechanisms for
agreement. These mechanisms must:

1.  Operate over *features *as a medium
2.  Be constrained by *categories*
3.  Involve *valuation — *including sensitivity to previously-defined
    values
4.  Be able to operate at a distance — put differently, they must be
    able to skip intervening/irrelevant items
5.  Operate over binary pairs — as identified by polarity/valence
    specified on the features, and in the roles of *probe *and *goal
    *assumed as a consequence
6.  Trigger further operations as “follow-on” effects or side-effects

Chapters 4 and 5 will demonstrate how all of these concerns are
addressed.


[Back](jherring-2) — [Forth](jherring-4)
