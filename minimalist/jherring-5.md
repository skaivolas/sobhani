---
title: Grammar Construction in the Minimalist Program — Chapter 5 — Two Control-Based Examples
layout: page
---

[Back](jherring-4) — [Forth](jherring-6)

# <span id="anchor-89"></span>Chapter 5 — Two Control-Based Examples

## <span id="anchor-90"></span><span id="anchor-91"></span><span id="anchor-92"></span>Overview

Having now spelled out the implementational primitives in some detail,
what remains is to show their application to a practical example.

The utility in any grammar construction toolkit lies only secondarily in
its ability to verify a researcher’s claims about the coverage of his
theory. More important by far is its ability to highlight areas where a
given theory falls short. Often such shortcomings will be known and
acknowledged by the researcher, as no theory to date claims to cover all
or even most observed syntactic data. But in many cases they are either
unanticipated or not (publicly) acknolwledged. Science proceeds by
gathering data, reasoning to the best explanation, and then looking for
failure — and it is typically in repairing failure that the most
interesting and fruitful advances are made. A system such as the one
under construction succeeds to the extent it can help researchers — or
perhaps their rivals — identify points where theories break down,
adjudicating, as it were, disputes about the right way to proceed in the
development of a comprehensive theory of human grammar knowledge.

In this context, the Movement Theory of Control (MTC) (Hornstein 1999;
Boeckx, Hornstein, and Nunes 2010) presents an attractive test case.

Three qualities in particular suggest it as a fecund patch in which to
build and improve a grammar development system for the Minimalist
Program: it is controversial, disruptive, and based in attempts to
shrink the size of the universal grammar toolkit. Controversy guarantees
attention, which in turn tends to generate detailed, quality research as
a side-effect. The fact that the MTC aims at shrinking the grammar
inventory — specifically by eliminating PRO and the control module
(construal), where possible — makes a grammar development toolkit a
particularly nice fit, as the MTC project is, in essence, a
“refactoring” of previous analyses. In such situations, it’s nice to
have a compiler around to verify one’s claims, especially when, as is
the case with the Movement Theory of Control, such claims are founded in
the removal or relaxation of a number of constraints — most prominently
the Theta Criterion — that served to narrow the possible outputs of the
system. Any time one is removing constraints, overgeneration is a
danger, and an automatic generation system can help to spot it early.
The most attractive thing about the Movement Theory of Control as an
area of focus in developing this system, however, is its disruptive
nature. Innovation is born in disruption, and it is the relative freedom
Minimalist researchers have to innovate that poses the biggest challenge
to developing an LKB analogue for Minimalism. In a formalized system
like Head-Driven Phrase Structure Grammar, the author of a software
toolkit gets at least a blueprint of how the system should work from the
framework architects. Minimalism, by contrast, is a program and not a
theory, and it imposes no such discipline. Researchers can use whatever
mechanisms they like, provided they are justified by appeals to “minimal
design” and “legibility at the interfaces.” While in practice, as noted,
the Minimalist inventory of grammar mechanisms is not significantly
larger than that of other frameworks, in principle there are no hard
limits to the devices that researchers can dream up. Areas like the
Movement Theory of Control, which disrupt standard assumptions about how
the system should work, are worth watching precisely because they are
the areas where researchers are most likely to go “off script,” forcing
the authors of a grammar toolkit to either reanalyze the proposals in
terms amenable to the system, or to expand the system to accomodate.

## <span id="anchor-93"></span>The Movement Theory of Control

Broadly speaking, the Movement Theory of Control arises from two
observations: that PRO is a suspect category under Minimalist principles
— ripe for elimination — and that many types of control phenomena
pattern with A-movement, suggesting a means to replace PRO.

### <span id="anchor-94"></span>Problems with PRO

The main problem with PRO is that it was postulated to meet an outdated
requirement: “GF-*θ*,” or the requirement that all *θ *positions be
filled at D-Structure. If an item had a *θ*-role-bearing argument slot,
then that slot must be filled *before the derivation begins*. This ruled
out, as a consequence, both the idea that an item could bear more than
one *θ*-role and the possibility of moving an item into a *θ*-position
during the course of the derivation<sup>\[49\]</sup>. Consequently, if a
*θ*-role appeared to be discharged in an otherwise grammatical sentence,
*something *must be there to absorb it at the outset of the derivation,
even if that thing were never expressly pronounced. This was PRO, and
the fact that it seemed to participate in independently-attested
grammatical functions (such as locally binding a reflexive in sentences
such as *John ordered Bill*<sub>i </sub>*PRO*<sub>i </sub>*to shave
himself*<sub>i</sub>) bolstered claims of its existence.

Unmistakable even then, however, was the suspicious fact that PRO has
exactly the properties that the grammar needs it to have. It acts like
an anaphor when it needs to and like a pronoun otherwise. It is in
complementary distribution with full lexical items, only ever appearing
as the subject of an infinitive (or a gerund) when one is independently
needed<sup> </sup>but not pronounced, and only in a tightly restricted
set of environments (the subject of gerunds and infinitives) — i.e. only
in exactly those positions it was created to fill. In fact, this
stipulation was quite explicit in the form of “NULL case” (Chomsky and
Lasnik 1993), a type of case requirement that was only satisfiable by
PRO and only “attested” on heads that took PRO as an argument. Although
some conceptual motivation was given for this — PRO was a “pronominal
anaphor” and thus could not be governed without violating one or the
other of the otherwise mutually exclusive conditions A and B of the
Binding Theory — the motivation itself rested on a theory-internal
stipulation: that infinitival T obviated government.

Worse still, all of this was theoretically costly. PRO necessitated the
addition of a module to the grammar — the Control Module, with a process
of Construal — to explain its interpretation. This is because it was
never quite correct to say that PRO was a “pronominal anaphor.” Rather,
as pointed out by (Landau 2004) and (Bouchard 1984), among others, PRO
behaved as *either *an anaphor *or *a *pronoun *depending on the
situation. It was never actually both at once — and so a separate
process was needed to say which it was in any given context.

All of this was tolerable in the GB framework where the GF-*θ
*requirement obtained. It was, one could say, a price duly paid for that
assumption, and worth paying so long as that assumption seemed
worthwhile. Moreover, in the GB framework, there was a plausible
explanation for how it arose. Since lexical insertion happened only
after a complete structure had been generated, PRO could be
conceptualized as the consequence of *failure *to insert a lexical item
at a particular point in the structure. This accorded well with its
“purely grammatical” nature: it was syntax without independent lexical
content.

With the advent of Minimalism, however, things changed radically, and
D-Structure was one of the first constructions eliminated, taking the
GF-*θ *requirement with it. The *θ*-Criterion remained important as a
way of preventing overgeneration<sup>\[50\]</sup>, but it had lost its
basis in D-Structure and had to be restated as a requirement that
*θ*-roles cannot be discharged by internal merge (i.e. movement)
(Chomsky 1993 ; Chomsky 2001). Additionally, the new framework came with
a commitment to lexicalism. There should be no purely grammatical
formatives; structures should be formed exclusively through the **Merge
**of lexical material with other lexical material, or the output of
previous such operations. This left no room for positions in the
structure that were formed but not filled. With the level of
representation that had justified its theoretical cost removed and the
avenue for its generation closed off, PRO had to be recast as a peculiar
kind of lexical item, and it was natural to begin to question whether it
were worth the price. The argument for its existence became entirely
empirical, and the stage was set: to the extent phenomena whose
explanation rests on PRO can be reanalyzed in PRO-free terms, PRO should
be eliminated. This is what the Movement Theory of Control aims to do.

### <span id="anchor-95"></span>What to do with PRO

As its name implies, the MTC has an idea where to start: with
displacement, specifically with A-movement. It has been noticed that in
certain types of control (obligatory control), PRO patterns with
A-movement, behaving as though it were the trace of a moved item. Some
characteristics the two have in common include<sup>\[51\]</sup>:

**PRO is unpronounced**. No explanation for this is needed if PRO is an
A-trace, as A-traces are in the general case not pronounced (Hornstein
1999). It is a strange property for a lexical item to have, however
(Landau 2015).

Obligatory Control (OC) PRO requires a c-commanding antecedent

1.  He<sub>i </sub>hoped PRO<sub>i </sub>to shave himself<sub>i</sub>
2.  \*It<sub>i </sub>hoped PRO<sub>i </sub>to shave himself<sub>i</sub>
3.  \*John<sub>i</sub>’s campaign hoped PRO<sub>i </sub>to shave
    himself<sub>i</sub>
4.  \*John<sub>i </sub>thinks that it was hoped PRO<sub>i </sub>to shave
    himself<sub>i</sub>

Only the first sentence is grammatical. In the second, the intended
antecedent doesn’t match in *φ*-features, in the third it does not
c-command, and in the fourth it crosses over a clause boundary. PRO, it
seems, must be locally bound.

**OC PRO has an obligatory ***de se ***reading**

1\. \[The unfortunate\]<sub>i </sub>expects PRO<sub>i </sub>to get a
medal

This can only be interpreted to mean that *the unfortunate *expects *of
himself *that he will get a medal by contrast with *The
unfortunate*<sub>i </sub>*expects that he*<sub>i(j) </sub>*will get a
medal*, where *he *can be *the unfortunate *or, optionally, someone *the
unfortunate *mistakes for someone else but is actually he himself. The
details of whence *de se *readings arise are complex and somewhat
unclear, especially as regards why they arise from movement. The point
for the present discussion is simply that this is a property that OC
shares with A-movement, supporting the intuition that the same process
underlies both.

**OC PRO has a sloppy reading under ellipsis**

1\. John<sub>i </sub>wants PRO<sub>i </sub>to win and Bill<sub>j
</sub>does too.

*does *here can only be “wants PRO<sub>j=Bill </sub>to win”; it does not
get a reading where Bill wants John to win. If PRO is construed
independently by some other module, we’d have to say how that
restriction comes to be. If it’s simply a(n ellided) trace of the
movement of *Bill*, however, no independent explanation is necessary.

(Boeckx, Hornstein, and Nunes 2010) — and others working in the MTC
paradigm — are careful not to claim that all empirical obstacles to
reanalyzing (OC) PRO as A-movement thereby collapse. Rather, the claim
is just that these examples demonstrate sufficient similarity with
A-movement to make analyzing PRO in that way the null hypothesis. Since
independent stipulations in the form of bans on movement into
*θ*-position are needed to rule it out, the burden of proof is squarely
on its opponents.

## <span id="anchor-96"></span><span id="anchor-97"></span><span id="anchor-98"></span>Empirical Problems with the Movement Theory of Control

Arguments against the Movement Theory of Control are indeed primarily
empirical. Brief explanations of the most common follow.

### <span id="anchor-99"></span>Control is not Raising under Passivization

The most prominent argument in (Landau 2003) involves passivization. If
the salient difference between raising and control is only the
additional *θ*-role, as would be consistent with the MTC, then processes
which consume the outer *θ*-role, such as passivization, should render
control identical to raising. However, this does not seem to be the
case:

1.  John<sub>i </sub>tried John<sub>i </sub>to kiss Mary
2.  \*John<sub>i </sub>was hoped John<sub>i </sub>to kiss Mary
3.  John<sub>i </sub>was persuaded John<sub>i </sub>\[<sub>TP
    </sub>John<sub>i </sub>to kiss Mary\] (cf *Bill persuaded John to
    kiss Mary*.)

The second sentence is ungrammatical<sup>\[52\]</sup>, contrary to what
the MTC would predict. This has an explanation if PRO is a distinct
entity with properties that separate it from lexical DPs — something
about those properties (case, probably) can be marshalled to prohibit
PRO from raising to a lexical subject position. It’s difficult to see
how the MTC would block it, though, since “PRO” is simply *John*, a
lexical DP of the type that we independently know can be the subject of
a passive.

### <span id="anchor-100"></span>Defective Intervention Should Block Subject Control, Contrary to Fact

Another prominent argument in (Landau 2003) is that the citation of the
Minimal Distance Principle as evidence in favor of the Movement Theory
of Control is overstated.

1.  John<sub>i </sub>wanted PRO<sub>i </sub>to leave
2.  John<sub>i </sub>persuaded Mary<sub>j </sub>PRO<sub>j </sub>to leave
3.  John<sub>i </sub>promised Mary<sub>j </sub>PRO<sub>i </sub>to leave

If control is A-movement, and we know from A-movement that there are
intervention effects, then the general preference for object control in
cases where the matrix verb has two arguments follows naturally. The
trouble with that reasoning is that subject control should in principle
be impossible, as the object always intervenes, at least on the standard
assumpton that “distance”<sup> </sup>is mediated through c-command. The
point here is not that there are no workarounds — there are, and
proponents of the Movement Theory of Control have proposed in particular
to reanalyze the object of *promise *as a PP headed by a null P. The
point is that whatever workaround is invoked amounts to recreating the
Control Module by proxy, as the semantics of the matrix verb are the
appropriate locus of differentiation.

### <span id="anchor-101"></span>The Embedded Clause is an Independent Case Assignment Domain under Control

The most prominent argument in (Bobaljik and Landau 2009), but well
known from earlier sources (e.g. (Sigurdsson 2008; Thrainsson 1986)) is
that the Movement Theory of Control fails to account for the fact that
the embedded clause appears to be a separate domain for case assignment
under control but not for raising. This shows up prominently in quirky
case languages, where case assignment is dependent on the verb, with
some verbs following normal patterns and some imposing
deviant/idiosyncratic (“quirky”) case marking. The following pair of
Icelandic examples is from (Sigurdsson 2008):

1)  a. Mennirnir/\*Mönnunum vonast til \[að PRO verða baðum hjalpað\]

men.the.N/\*D hope for to PRO be both.D helped.DFT

"The men hope to both be helped"

1)  2.  Mönnunum/\*Mennirnir virðist baðum \[t hafa verið hjalpað\]

men.the.D/\*N seem both.D t have been helped.DFT

"The men seemed to have both been helped"

*hjalpað *is a quirky case verb and assigns Dative. In the control
example (1c), dative marking does appear on the agreeing participle and
on *baðum *in the emebedded clause, but in the matrix clause the subject
surfaces nominative and indeed cannot be dative. There is case mismatch
between the matrix controller and the controlled PRO. No such mismatch
occurs in the raising example, however. Case concord would appear to be
clause-bound. These facts are consistent with an implementational split
between raising and control in which control involves two chains in
separate clauses and raising only one.

### <span id="anchor-102"></span>Partial Control

Probably the biggest implementation challenge for the Movement Theory of
Control comes from partial control. As detailed in (Landau 2000),
partial control is a phenomenon where the reference of the controlled
PRO is accounted for but not exhasted by the reference of the
controller. Examples include:

1.  The chair<sub>i </sub>preferred PRO<sub>i+ </sub>to gather at 6.
2.  Bill<sub>i </sub>regretted PRO<sub>i+ </sub>meeting without a
    concrete agenda.
3.  Mary<sub>i </sub>wondered whether PRO<sub>i+ </sub>to apply together
    for the grant.

The challenge for the MTC is obvious: there is no known mechanism which
would allow a pronounced copy of an item to refer to itself but its
lower copies to additionally refer to outside entities. Possible
workarounds would need to either posit additional, unpronounced material
to account for the additional reference, or find a way to form an
A-chain in which the members were distinct in spite of everything. The
former solution is conceptually stipulative, undercutting the main
theoretical attraction of the MTC, and the latter recreates the control
module by other means.

## <span id="anchor-103"></span>The Agree Theory of Control

Whatever its empirical challenges, the Movement Theory of Control is
inarguably well grounded in Minimalist principles. In scrutinizing the
justification for PRO, it asks minimalist questions, and in suggesting
its replacement through independently-attested mechanisms of grammar, it
proposes minimalist answers. But it would be too simplistic — and
perhaps even a bit romantic — to cast the debate as a classic tumble
about where to draw the line between theory and
practice<sup>\[53\]</sup>. For one thing, MTC proponents argue that they
have risen to the challenge of addressing many proposed empirical
problems, and that those that remain will be more illuminating for the
study of human grammar if investigated with a mind to resolving the
issue with displacement. For another, opponents are not without
theoretical grounding of their own.

In particular, alternatives to the Movement Theory of Control rely
heavily on **Agree **operations to mediate the relevant dependencies.
Since in virtually all modern theories displacement only ever occurs as
a side-effect of **Agree**, and as instances of **Agree **without
accompanying displacement become ever more common in analyses, opponents
of the Movement Theory of Control can plausibly claim that it is
premature. While it’s certainly true that Minimalism guides researchers
to eschew stipulative grammar formatives where possible, the argument
goes, an equally valid minimalist principle would encourage expression
of grammatical relations in terms of mechanisms known to be operative in
*all *long-distance dependencies before there is sufficient evidence to
assume the more specialized treatment. Control relations will have to be
explained in terms of **Agree **no matter what; why add displacement to
the mix before such a move is forced by the data?

Because of the heavy reliance on **Agree**, it is common to refer to
alternatives to the Movement Theory of Control as “Agree Theor\[ies\] of
Control.” Most prominently, the “Calculus of Control” approach of
(Landau 2004; Landau 2006; Landau 2008) is so called. A brief sketch of
its operation is given below.

Like movement-based approaches, the Calculus of Control starts with the
understanding that PRO is a problematic creature, a byproduct of mostly
theory-internal concerns whose distribution and behavior is in need of
independent explanation. If a derivation of PRO from independent
princples remains out of reach for now, then the next best thing is to
account for its distribution by appeal to something less stipulative —
or at least stipulated on the basis of better\[54\]<sup>
</sup>emprirical observations — than “null case.” This is done through a
“calculus” that involves the interaction of Semantic Tense and Abstract
Agreement — features of C and I/T — that conspire, or don’t, to create
an environemnt where PRO can be merged. Here “Semantic Tense” is meant
to be independent of morphological representation. This feature encodes
the degree to which meaningful tense is interpreted by a contribution
from the bearing head itself (\[+T\]), or is entirely inherited from a
selecting head (\[–T\]).

Arguing primarily from data on Balkan subjunctives, Landau shows that
obligatory control only ever happens in environments where the tense of
the embedded clause is in some sense linked to, or dependent on, the
tense of the main clause. This could be because the tense of the
embedded clause is either non-existent or completely parasitic on the
tense of the main clause — called *anaphoric *tense — or because it is
determined by it, though represented separately — called *dependent
*tense. Where tense is completely independent, there is no control at
all, and any null subject is *pro *and has completely independent
reference from any aspiring<sup> </sup>matrix controller.

Tense for the purposes of embedded clause selection arises — or doesn’t
— from a conspiracy of features on embedded C and I/T. It is always
interpretable on T and uninterpretable on C. By standard assumption, if
the Tense feature on T and C match, the uninterpretable member of the
pair is deleted, and the interpretable member lingers. *Anaphoric *tense
is represented with a \[–T\] feature on C, and dependent with \[+T\]. C
need not, however, bear a Tense feature. When it does not, the Tense of
the lower clause is free — as is the case in most languages when the
lower clause is indicative. Put differently, an abstract Tense feature
on C provides a medium through which a matrix clause can *locally
*select an appropriately-tensed clausal complement. The checking
relation between C and T ensures that C manifests the clause’s Tense,
and the selecting matrix head can combine, or not, appropriately.

Agreement forms the second component of the Calculus. Landau assumes
that the Agree feature is parasitic on Tense, appearing only then when
Tense is present and specified for dependent tense. In cases where Tense
on C is either anaphoric or not specific, there is no Agree feature.

This breaks down in the following way:

NO CONTROL

**Indicative — **C: NULL, T:\[+T,+Agr\]

**Balkan Finite Subjunctive — **C: \[+T,+Agr\], T:\[+T,+Agr\]

OBLIGATORY CONTROL

**Exhaustive Control Infinitive — **C: \[–T\], T:\[–T,-Agr\]

**Balkan Control Subjunctive — **C: \[–T\], T:\[–T,+Agr\]

**Partial Control Infinitive — **C: \[+T, (+Agr)\], T: \[+T, -Agr\]

(Additional specifications for Hebrew finite control clauses are skipped
here.)

The main generalization is that control is an “elsewhere” case: it is
blocked wherever I/T is \[+T,+Agr\]. Obligatory control environments are
not a natural class — rather, they arise whenever there is some featural
deficiency on the T head.

The Control Module itself arises from an interpretable feature \[–R\] on
PRO. An uninterpretable counterpart of this feature arises on T or C
whenever (a) *both *\[T\] and \[Agr\] are present and

2)  one or the other of them is \[–\]. If both are present and \[+\],
    the \[R\] feature is also present and \[+\] — i.e. is \[+R\] and
    obviates control. R is lacking altogether when either \[T\] or
    \[Agr\] is not present. The right way to think about \[R\] then is
    as an “independent reference feature.” T (or C) with \[+R\] selects
    an expression with independent reference — i.e a lexical DP or a
    pronoun (or, by implication, *pro*). \[–R\] matches with an item
    that needs to get its reference from elsewhere — i.e. selects PRO.

In theoretical terms this is, of course, more or less a recreation of
the GB and “null case” systems. We still have a feature that
specifically selects PRO and only PRO and happens to only arise in
precisely those environments where PRO can appear. Likewise, PRO appears
in this environment only because nothing else can. Just like in GB,
where PRO was a position without content, where lexical insertion had
failed, here PRO represents a kind of environmental deficiency as well.
The innovation comes in making this environment parasitic on independent
factors — semantic tense and morphological agreement — that are known to
determine control environments by virtue of their absence.

The control module itself works under two assumptions: (1) that
features, even checked features, are not “used up” until the end of the
phase, so that uninterpretable features can probe more than once before
phase end, and (2) that *Agree *establishes relationships between heads,
and so is capable of transmitting information — the antecedent’s
referential index in this case — across long-distance dependencies, a
standard assumption.

Exhaustive control (EC) works as follows:

2)  1.  T has an uninterpretable \[–R\] feature by virtue of (a) having
        specifications for both \[T\] and \[Agr\], (b) at least one of
        which (both in this case) is \[–\].
    2.  T cannot check its uninterpretable \[–R\] feature on C because
        C, being specified \[–T\] only, fails to meet the “both”
        requirement (requirement (a) in the previous point) for having
        an \[R\] feature at all — therefore it lacks any such feature.
    3.  T must check its \[–R\] feature on PRO, then. So, PRO is
        present.
    4.  The \[–R\] feature on PRO means PRO has to enter into a second
        relationship to get its reference. It can do this with an item
        that is \[+R\] — i.e. with whatever functional head selected the
        controller. This head (T in the case of subject control) will
        necessarily bear an uninterpretable \[–R\] feature, the feature
        that selects the \[+R\] referential DP in its specifier. Under
        the assumption that *probe*s are active until the end of the
        phase, it will *probe *a second time into its complement. Since
        C bears no intervening \[R\] feature of its own (lacking
        \[Agr\]), there is nothing to block the *probe *finding the
        \[–R\] feature on PRO. Having inherited a \[+R\] value from
        the DP in its specifier (that is, having inherited a *reference
        value *from it), PRO will be able to check its \[–R\] feature
        and get a reference. This is how it comes to be coindexed with
        the controller.

Partial control works similarly, with one critical difference:

1.  T has an uninterpretable \[–R\] feature by virtue of (a) having
    specifications for both \[T\] and \[Agr\], (b) at least one of which
    (T in this case) is \[–\].
2.  Since T is \[–R\], as before, it will check PRO.
3.  Because C is specified for \[+T,+Agr\], it also has \[+R\], so T can
    enter into a relationship with it. Since it is \[+R\], PRO will get
    reference from it, since PRO is already in a relationship with T.
4.  As with exhaustive control, the functional head that selects the
    controller will continue to probe during its phase even though it
    has already satisfied its \[+R\] requirement by means of having
    selected the (ultimate) controller.
5.  This time, it will stop at C, which has an intervening feature
    \[+R\] of its own, not finding PRO. However, because the (ultimate)
    controller is in a checking relationship with the probing matrix
    head, and the probing matrix head is in a checking relationship with
    C, and C is in a checking relationship with T, and T is in a
    checking relationship with PRO, the controller comes to control PRO
    *mediated through C*. It is this mediation that gives rise to
    partial control effects — because PRO gets its reference from two
    places, one concrete (the lexical subject controller in the matrix)
    and one abstract (C in the embedded clause).

## <span id="anchor-104"></span><span id="anchor-105"></span><span id="anchor-106"></span>Implementation

The purpose of this project is to lay the groundwork — both theoretical
and practical — for a grammar construction toolkit for the Minimalist
Program. On the theoretical side, it identifies a minimal set of devices
capable of covering the most widely-cited analyses, and on the practical
side it makes these available to researchers in the form of an
implemented and useable toolkit. The proof, of course, is in the
pudding, and the following sections outline how a researcher might go
about implementing tricky analyses in the competing systems of the
Movement and Agree Theories of Control with the tools available in the
system. In each case, the actual implementation reveals hidden
assumptions (albeit minor in the case of the Agree Theory) not mentioned
in the original reports that illuminate details of the theory.

### <span id="anchor-107"></span>Movement Theory of Control — Visser’s Generalization

Subject control structures which involve a matrix object are problematic
for movement- based theories of control as the theory must account for
why the object doesn’t intervene. Passivization is a problem for *any
*derivational theory for similar reasons — at least to the extent the
analysis involves the use of a null subject, as has been standard since
shortly after (Baker, Johnson, and Roberts 1989)<sup>\[55\]</sup>. Thus,
Visser’s Generalization (Bresnan 1982), according to which subject
control verbs cannot passivize — put differently, control by an implicit
subject in passives is impossible — poses a particular difficulty.

The problem is roughly this.

*John was kicked *is clearly grammatical. On the standard analysis, the
canonical object *John *raises to subject position to get case because:
(1) the external *θ*-role of the verb has been absorbed by the passive
morpheme which (2) by *Burzio’s Generalization *renders it incapable of
assigning **ACC **case so (3) to be case-licensed, *John *must move to
the next plausible location for case assignment, which is **Spec**-T.

The structure is meant to look something like this:

~~~~

~~~~

The problematic bit is the *pro *in **Spec**-vP. It is motivated by
evidence that the implicit argument in a passive construction can
control:

*The ship was pro*<sub>i </sub>*sunk PRO*<sub>i </sub>*to collect the
insurance *(Bhatt and Pancheva 2006)

Whoever sunk the ship also intended to collect the insurance; this fact
is presumably accounted for in the usual way — binding of a lower PRO by
a higher argument, leading to coreference.

The trouble is that the *pro*, as a D category, should intervene in any
attempts to raise the object to subject position.

The account that (Hornstein and Polinsky 2010) give is not too
controversial: in addition to absorbing the external *θ*-role (and
subsequently also **ACC**), passive-*v *also admits of an additional
**Spec**, and *John *makes its way to this position on its way to T.
When T is **Merge**d, it is at least equidistant with *pro *and hence
visible to the **Probe**.

![](Pictures/1002B84700001EB300001DE59D5BB1C2CA5DD8D9.svgPictures/10000201000000DF000000D92D4C451FE2180A94.png)

(Hornstein and Polinsky 2010) don’t commit themselves to any particular
motivation for this movement, but they hint that it might be to value
*φ*-features on the passive participle (since this sort of agreement is
visible in a number of languages). Whatever the motivation, it solves
the problem.

However, it raises another one: if the additional **Spec **is available
for passives, how do we prevent the following:

1.  \*John<sub>i </sub>was hoped PRO<sub>i </sub>to win.
2.  \*Mary<sub>i </sub>was promised (by John<sub>j</sub>) PRO<sub>j
    </sub>to win.

The puzzle of the *promise *example requires recognition of the fact
that ECM verbs allow passivization under control:

1\. John was expected to invite Mary to the prom

(Hornstein and Polinsky analyze *~~John~~ to invite Mary to the prom *as
a TP, but nothing hinges on that here.)

Meaning — the additional/outer **Spec**-vP that provided an escape hatch
is also available in ECM constructions. It can’t, however, be available
in object-less subject control:

\*John<sub>i </sub>was pro<sub>j </sub>hoped PRO<sub>i </sub>to win.

Presumably ECM verbs and ditransitive subject control verbs can be made
to form a (natural) class, and the above example ruled out by the fact
that *hope *isn’t a member. Hornstein and Polinsky never say what
generalization accounts for this, but it seems natural to assume that
they have in mind that the extra **Spec **is there as a side-effect of
the absorption of **ACC **case. In a purely lexicalist system, then,
passive-*v *comes in two forms, one that selects transitive V and one
intransitive, and the one that selects transitive happens to have an
outer **Spec**.

If that is the generalization, though, lack of an extra **Spec**-vP
(obviating intervention by the null subject) cannot be the explanation
for the ungrammaticality of *\*Mary*<sub>i </sub>*was promised (by*

*John*<sub>j</sub>*) PRO*<sub>j </sub>*to win*.

The solution proposed has a classic “rule-ordering” feel to it.
Basically, the idea is that in *promise*-type verbs, the internal
argument is not **ACC **anyway, but rather some kind of dative
experiencer and thus buried in a PP headed by a null P.

Passivization for such verbs is really some kind of pseudopassive: it’s
the object of the preposition that passivizes rather than the entire
phrase.

Mary was promised a rose garden (by John)<sup>\[56\]</sup>

Hornstein and Polinsky take this to indicate that some kind of
incorporation has taken place. Presumably once V adjoins to *v*, *v*-V P
is reanalyzed as *v*-V-P, transforming the external argument of the V
into a regular DP. This is arguably necessary to allow *Mary *any sort
of mobility at all — cf:

A rose garden was promised to Mary

??A rose garden was promised Mary

Hornstein and Polinsky are not clear on when the incorporation happens
in the reference example, but they are certain it must happen before any
attempt to raise any embedded *pro *to **Spec**-v, as this is how they
propose to rule out

\*Mary<sub>j </sub>was pro<sub>i </sub>promised- ~~to~~ Mary<sub>j
</sub>~~promised~~ pro<sub>i </sub>to win (by John<sub>i</sub>).

From repeated references to concerns of “violation of cyclicity/respect
for the Extension Condition,” one can assume they have in mind that
incorporation happens *before ***Merge **of T; anything later than that
would be altering already-determined truths about the structure “out of
turn.” While this suffices for the example at hand, one would really
like more detail here, in light of the fact that incorporation seems to
be optional — cf *A rose garden was promised to Mary *above.<sup>\[57\]
</sup>For the purposes of the implementation below, it will be taken to
happen as a side-effect of head movement of V to *v — *specifically, in
the *compact *cycle mentioned in the previous chapter.

With all aspects of the analysis assembled, it’s possible to provide an
implementation guide in the system.

The lexical array is:

John, promise, to-P, Mary, to<sub>inf</sub>, win, v<sub>trans</sub>,
v<sub>ditrans</sub>, T, C

grouped into subarrays as follows:

\{win, John, v<sub>intrans</sub>\}, \{to<sub>inf</sub>\}, \{to-P, Mary\},
\{promise, v<sub>ditrans</sub>\}, \{T-past, C\}

In “generation mode” all of this could be randomized, but for the
purposes of explication the arrangement that works is chosen.

A ***stage ***is seeded with an empty ***workspace ***and the first of
the ***lexical subarray***s: \{win, John, v<sub>intrans</sub>\}

**Activate **chooses v<sub>intrans</sub>

v<sub>intrans </sub>**Select**s *win — *which is to say, it has a
**selector **feature that will match a **selectee **feature on *win*.
*Win *is moved out of the ***lexical array ***into the ***workspace***,
specifically it is unshifted onto *v*’s *constituents stack — *(since
**merge **is a side-effect of **select**, and **select **happens
whenever selectional features match and value).

**compact **happens as a side-effect of this **merge**, the
uninterpretable **selector **features are eliminated from *v*, and
**transfer **occurs as a result — specifically of the **donate
**variety: all V’s features unshift onto the front of *v*’s feature
stack, effectively implementing head adjunction to *v*.

*v *is still active because it still has a **probe — **a **selector
**feature looking for a D-category **selectee**. **merge-over-move
**requires it to first look in the ***lexical array***, which it does
and finds *John*.

Again, **merge **is a side-effect of **select**, *John *is moved to the
end of *v*’s “constituents” array, making if effectively a **Spec**.

*v*’s **probes **are not exhausted — there is still a *theta *probe,
which is satisfied on *John*. Having exhausted its **probes**, *v*’s
**selectee **becomes active.

Now that *John *is active, it can try its *case ***probe**, first on the
head T and later, if not successful, on the items in the head’s
*constituents *array. It finds nothing.

There are no lexical items in the ***lexical array***, so the ***stage
***halts in a *divergent *state.

A new stage is created to deal with the next ***lexical array***, which
is simply to<sub>inf</sub>.

The output of the previous ***stage ***is placed in the ***workspace
***of the current one. *to*<sub>inf </sub>is **activated**, which means
**selected **from the array. It has a **selector Probe **which, by
**merge-over-move**, must first inspect the ***lexical array***. This is
empty, so it looks into the stage’s items. There is one — the output of
the previous stage, so it **probes **into this and finds a match on *v*.

**select **has **merge **as a side-effect, so the output of the previous
stage is moved to *to*’s *constituents *array. **value **and **compact
**take place, removing the **selector **feature on *to*.

*to *is still active, as it has an EPP **probe**. EPP is an aberrent
**probe **that **selects **without **valuing**. It finds a match in
*John*, which is copied from *v*’s constituent list and added to *to*’s
as a **Spec **(i.e. is placed on the end).<sup>\[58\]</sup>

Now that *John *is active, it can try its *case ***probe**, first on the
head *v *and later, if not successful, on the items in the head’s
*constituents *array. It finds nothing.

The ***stage ***remains *divergent*, because although there is only one
object in the ***workspace***, there are unvalued features. Because the
***lexical array ***is exhausted, however, the ***stage ***cannot
continue, so a new ***stage ***is created for the next ***lexical
subarray***.

This is \{to-P, Mary\}, one of the two crucial points.

As before, previous output is placed into the currently-active
***workspace***.

Next, the ***stage *****activate**s *to*, which involves **selecting
**it from the ***lexical array***. *to *then **probes**, which by
**merge-over-move **must begin in the ***lexical array***. It finds a
match for its **selector **feature in ***Mary***. As usual, **match **is
followed by **value **and **compact**. ***Mary ***is now active but has
only a **case **probe. Depending on individual implementation, this may
find a match on P, or it may wait until *to Mary *is (eventually)
**merge**d with the rest of the tree. Either way, there’s nothing more
that happens at this ***stage***, so let’s assume *Mary ***probe**s *to
*and gets its **case **feature valued, just to get it out of the way.

This ***stage ***is still *divergent *because of (i) unvalued **selectee
**features on P and (ii) unvalued **case **features on *John *(which is
in the output of the previously-divergent **stage **and now sitting in
the **active **array of the current ***stage***.

Next up is \{promise, v<sub>ditrans</sub>\}. This stage illustrates an
interesting but ultimately inconse- quential quirk of the system in that
the argument to the phase head must itself take arguments, and yet the
algorithm following up to this point preferentially selects the head
with the most active non-selector **probes — **i.e. the phase head (if
it exists). This will give the appearance of countercyclic **merge**.
However, nothing really hangs on this. (Chomsky 2008) has already
suggested that everything at the phase level happens simultaneously;
this system takes that to the bank.

*v *is **activated **and must find a **goal **for its **selector
**probe. **merge-over-move **requires that it look for this first in the
***lexical array***, and so it finds *promise*. **select **happens,
followed by **merge **and **value **and **compact**. Part of **compact
**in this case is **head movement**: V incorporates into *v*.

Recall that this involves transfer of *all *of V’s remaining feature
array to *v*; in effect, they become the same **head**. Thus, what might
have alarmed the reader about the ordering here need not: arguments to V
are still selected in the proper order — the only difference from
standard accounts in the literature is that V does not have to “cross
over” anything in its **Spec **to get to *v *since **head movement
**happens first.

V having *unshift*ed its features onto *v*, its **probes **are now
active — in “reverse” order, in accordance with the Mirror Principle,
actually (Baker 1988).

It will find *John to win *and *to Mary *in the proper order and add
them to the constituents array of V-v after **select**, **value **and
**compact **on each.

Now, at this stage, **head movement **of P to V-v should really happen,
since this would be the final operation that involves only the V and v
domains. Since P has no remaining features, this is entirely vacuous.
But notice that this, in effect, means that incorporation happens
*before John *can raise to subject. *Mary *should therefore block. In
system terms, this is so because the next **probe **on V-v will be *v*’s
subject probe. Since *John to win *and *to Mary *were **merge**d in that
order, *John to win *is in **Comp **and *to Mary *in **Spec**. *to Mary
*is in principle higher than *John to win*.

However, remember at what level this is occuring. V-v incorporation has
already happened; these are already the same phrase. So, when *v*’s
subject **probe **looks in its *constituents *array, it will actually
look at *John to win *first. *John *can raise to subject just fine.
Thus, this **select**s and then (re)-**merges **followed by **value
**and **compact **(of *v*’s **selector **and *John*’s **case
**features).

The rest of the derivation will proceed in the obvious way, with T
**selecting ***v *and **probing **to find *John*, which is now the
highest element in the P-V-*v *complex, and then this in turn being
selected by C to close off the derivation (or, if prefered, T can
**inherit **all relevant features only *after ***merge **with C in a
(Chomsky 2008) style system, with *John *“countercyclically” raising to
**Spec**-T only after this occurs.

What has been sketched here is the most natural derivation in the
present system — and, arguably, the most natural derivation of this
sentence. An astute reader will have noticed that it poses some
interesting difficulties for the (Hornstein and Polinsky 2010) account
of Visser’s Generalization, however. In particular, there are two.

First, for all the talk of the importance of having P-incorporation
happen “cyclically”, it’s difficult to defend the idea that it should
happen any later than as an immediate consequence of **merge **with *v*.
Even if there are nits to pick with the ordering of operations sketched
here, such as insisting that *promise *first **merge**s with *John to
win *and then with *to Mary *and only *then *allowing the whole VP
complex to merge with *v*, as is the more standard
approach<sup>\[59\]</sup>, they will not really make it more “natural”
for incorporation to have to wait until *v *has had a chance to raise
*John *to subject out of the embedded clause just because that’s the
outcome the authors want. Delaying incorporation until after all
argument positions have been saturated is possible in this system (one
need only make incorporation parasitic on a feature specialized for the
purpose that comes later in the list of **probes **on *v*), but it is
stipulative.

Of course, the intended analysis in (Hornstein and Polinsky 2010) is
that incorporation doesn’t happen in the active version at all — it is
only forced by the passive, presumably as part of the process that
absorbs the internal *θ*-role of *promise*. That is a reasonably
standard assumption, and it accords well with acquisition facts (also
cited in the chapter) that show that *promise*-type subject control
constructions are acquired late, if at all. The insight seems to be that
if the system is going to deviate from expected behavior<sup>\[60\]
</sup>to engineer a **Spec **for T, it can only do so locally, and it is
precisely because the attempt is so local that it
fails<sup>\[61\]</sup>. But given the ordering of operations, it’s not
really clear that the derivation fails for the reasons the authors
assert. Or rather, if it does, then because there is a hidden
*θ*-criterion-like assumption in their analysis which requires that an
item not fill more than one argument role for the same head — precisely
the sort of thing they are hoping to avoid.

Second, the whole idea of saturating arguments before incorporation begs
another question, which is why the **probe **that finds a subject in the
*John *buried in the embedded clause that is the Object of *promise
*couldn’t find one that simply *was *its complement — in, e.g., *John
was kicked *from before. Recall that passive morphology adds a **Spec
**to allow *John *to be higher than a putative null subject *pro *that
has previously been **merged **in. Further recall that the motivation
for movement to this **Spec **was never expressly given, but
hypothesized to be to check *φ *features on V-*v*. If this is all true,
what reasons would there be that would prevent *v*, in the event of the
hypothetical absence of a *pro *in the ***lexical array***, from
**probe**ing its **Comp**, finding *John*<sup>*\[62\]*</sup>,
(re)-**merge**ing *John *in its **Spec**, and then checking the required
*φ*-features at the same time?. There do not seem to be any without
additional machinery.

Of course, there are good reasons to ban **Comp**-to-**Spec **movement.
The point is that Hornstein and Polinsky will need to enforce such a
filter. *Something *has to enforce the presence of *pro *on this
analysis, and whatever that may be, it’s suspiciously close to
recreating the *θ*-criterion by other means.<sup>\[63\]</sup>

The upshot is that the explanation for the ungrammaticality of *\*Mary
was promised to win *goes through — incorporation does indeed, in the
most natural setup, precede any attempt to raise *pro *to subject,
blocking the attempt.

### <span id="anchor-108"></span>Hidden Assumptions

The careful reader will have noticed that Hornstein and Polinsky got off
on a technicality here. The two derivations actually work in the way
they described for very different reasons. In the first case, it works
only because the default behavior of this system incorporates V *before
*merging any arguments. If V were forced to accept its arguments *before
**merge***ing with ***v***, as is the standard assumption, then
incorporation of P would block raising of *John *to subject just as
easily as it blocks *pro*. Everything, therefore, inges on
implementation details of a system that doesn’t work in the way that the
authors probably assume.

More to the point, there is nothing stopping the system from functioning
in the way that is generally assumed. More detailed discussion of the
mechanics of just such a derivation is given in Appendix A, but the
broad point is that if the system is implemented in such a way that a
***probe ***runs in *reverse *order over the ***constituents ***array,
enforcing hierarchy, the blocking effects return, as the system will
find *Mary — *since it is a DP in good standing after P incorporation —
before finding *John*. This would require a bit of reinterpretation of
system functionality, but it is minor: **head incorporation**, properly
understood, is merely a way for a binary branching system to behave like
a shallow-tree system (a system in which trees<sup> </sup>can branch as
much as needed to include all phrasal arguments) without entirely giving
up on the binary representation.

Hornstein and Polinsky’s timing problem is now real: they need a way for
P-incorporation to happen in the passive derivation *only — *or, if it
happens in the active derivation, then after a delay. So one possible
hidden assumption (assuming it is not simply an oversight) that is
discovered by use of a system like this one is that incorporation of the
kind described is specific to *passive *“promise.” It is, of course,
possible to build this assumption in to the system: one need only give
passive ***v ***and active ***v ***different categories (as seems
natural) and then write the ***strategy ***function (see Chapter 4) so
that it forces incorporation only on **select **by the *passive
*version. This works, but of course it is not linguistically satisfying;
it has the character of a hack.

There are more serious hidden assumptions that are not so easily
resolved, however. Foremost among these is the assumption that *pro *can
appear freely either in SPEC-to or SPEC-v. The problem is easily
revealed by inclusion of *pro *in the lexical array that starts the
active derivation. There are reasonable ways to block *pro *from
appearing as the external argument to *v *in the active derivation, of
course, but if they are linguistically honest they tie themselves to the
presence or absense of the external *θ*-role, which sounds suspiciously
like a step down the road to reinvention of the traditional
*θ*-criterion. But what can’t really be done on the assumptions that
Hornstein and Polinsky are making is to block *pro *from the SPEC-T
position in the lower clause. The trouble is that in the active version,
there is absolutely no problem with initial-***merge***ing *John *in
SPEC-v. After all, this is the canonical position for its first merge.
Here it gets a *θ*-role, and it is in a position to raise to get case
(and become the grammatical subject) in SPEC-T. Without some way of
preventing *pro *in the lower clause, *John promised Mary pro to win
*can mean *John*<sub>i </sub>*promised Mary*<sub>j </sub>*pro*<sub>k
</sub>*to win — *to wit that John promised Mary that *someone else
entirely *would win. This reading is simply not available.

The Calculus of Control avoids these problems by means of its “honest
stipulation” — Landau’s term of art for his concession that his (former)
system reinvents the PRO module by other means. Perhaps it is a
stipulation, but by tightly regulating what can appear in PRO positions,
the Calculus of Control system correctly gets a crash on any attempt to
introduce a disallowed element there. Again, the reader is refered to
Appendix A for details of the derivation.

### <span id="anchor-109"></span>Agree Theory of Control — Visser’s Generalization

As seen in the previous section, lack of precision about when, exactly,
the incorporation of the P that heads the external argument of *promise
*into V-*v *occurs allows the Movement Theory of Control-based treatment
of Visser’s Generalization facts in (Hornstein and Polinsky 2010) to
appear more principled than it is. On close examination, for the
analysis to work, incorporation has to happen at exactly the moment
necessary to either allow raising to subject (in *John promised Mary to
win*) or to block it (in *\*Mary was promised to win*), and this seems
less than insightful. Can an Agree theory do any better?

Landau’s Calculus of Control accepts PRO as an “honest stipulation”
(Landau 2004) in exchange for, he argues, a better fit with the
empirical facts. More precisely, the “honest stipulation” is that
control is an elsewhere case that obtains whenever an embedded T or C
head is defective in one or both of **Abstract Tense **and **Agr**. In
general, T heads should fully represent Tense (\[+T\]) and Agreement
(\[+Agr\]). If they are dependent on another head (usually C) in either
regard, or simply fail to manifest either (infinitive *to*), they are
marked with a diacritic feature (\[–R\]) indicating that they can only
attract an item that is similarly dependent on outside specification —
in this case for its *reference*. This place is held by PRO — admittedly
a “pure grammatical formative” of dubious suitability to the Minimalist
Program

\- until more light can be shed on the subject. Since PRO must get
reference to be licensed, control happens as a byproduct.

In the case of Visser’s Generalization, as pointed out by (Urk 2013),
this has the virtue of tying the phenomenon to **Agree**, which seems
empirically correct. That study gives the following revised definition
of the phenomenon:

Obligatory control by an implicit subject is impossible if an overt DP
agrees with T

The revision owes to the facts of impersonal passives in languages like
German,

1)  \*Der Lehrer<sub>i </sub>wurde gebeten ihn<sub>i </sub>zu kitzeln
    dürfen.

The teacher wasbegged him to tickle allow

"The teacher<sub>i </sub>was begged to be allowed to tickle
him<sub>i</sub>"

1)  Mirwurde versprochen, mir nochheute den Link für das Update zu
    schicken

Me.DAT was promised, me.DAT already today the link for the update to
send 

"I was promised to be sent the link to the update today."

The first sentence shows that the personal passive — where agreement
obtains between *Der Lehrer *and T-*wurde — *is ruled out just an in
English. But in the second sentence, which is an impersonal passive, a
construct that English doesn’t really have in precisely this form, there
is no similar problem. Visser’s Generalization effects are correlated
with a *nominative *argument agreeing with T; otherwise, they don’t
obtain.

This achieves the same result by slightly more intuitive means. Like in
the MTC analysis, the core problem with sentences like *\*Mary was
promised to win (by John) *is one of construal:

the *pro *that is the subject of *promise *can’t establish a
relationship with the PRO that is the subject of *to win*. Given MTC
commitments, construal failures must be cast in movement terms, so that
means the problem is that *pro *can’t move from **Spec**-to to the
external argument position of the matrix *v*. This gets the right
result, but it doesn’t really have any good explanation for why **Agree
**between the matrix T would be implicated. Empirically, however, there
is reason to believe that Visser’s Generalization only applies to
constructions in which matrix T has successfully **Agree**d with a
nominal.

So, how would that be implemented in the present system?

To rule out *\*Mary was promised to win*, the derivation proceeds in
much the same way as the MTC derivation. We start with the same set of
primitives arranged in the same way, just with the addition of *PRO*:

\{win, PRO, v<sub>intrans</sub>\}, \{to<sub>inf</sub>\}, \{C\}, \{to-P, Mary\},
\{promise, v<sub>pass</sub>\}, \{T-past, C\}

The first part of the derivation proceeds as before — *v ***select**s
*win *and then PRO. Then *to*<sub>inf </sub>**select**s the ***syntactic
object ***formed by this complex. Because *to*<sub>inf </sub>is
specified \[+T, -Agr\], it comes with an \[–R\] feature, which requires
it to select only PRO.<sup>\[64\]</sup>. So, PRO is **probe**d and moved
to **Spec**-*to *(in system terms, it is **select**ed and added to the
end of the constituents list of *to*<sub>inf</sub>; *PRO win *is in the
first position of that list).

Since this is a recreation *in spirit *of the null case approach, this
***stage ***is *divergent *because PRO is missing features —
specifically \[R\]. But PRO itelf does not come out of the lexicon
deficient. Rather, it **inherit**s the deficiency from T — in system
terms, T exercises the **share **option on feature valuation, and PRO
becomes entangled with T’s \[–R\] feature, guaranteeing<sup> </sup>that
it will end up with whatever reference T receives.

From here, it is **merge**d with C, which, since this matrix allows
partial control, is \[+T, (+Agr)\]. It therefore has a \[+R\] feature
which **value**s, again through **share**, the one on *to *and, by
implication, the one on PRO. However, at this stage in the derivation
the value is abstract — merely a placeholder.

From there, the derivation proceeds as before. The details are slightly
different, however, as this is a passive construction. So, *promise
***select**s *to Mary*, and the preposition incorporates, but
*v*<sub>pass </sub>does not value anything with case features. It also
**select**s an external *pro*. This is easy to enforce because this
system has no problem with the *θ*-Criterion, and there is a ban on
double assignment of *θ *features.

Because *Mary *is available to **probe **by T, when that is **merge**d
with the existing matrix *v *structure, *Mary *raises to **Spec**-T
(again, in system terms it is pulled out of the first object in T’s
***constituent list ***and put on the end of same). This means that T
has **Agree**d with *Mary*. Since matrix T is \[+T, +Agr\], it is also
\[+R\]. By assumption (in Landau’s system), **probe **continues until it
is exhausted, so after **probe**ing its **Spec**, the matrix T continues
to **probe **into its **Comp**. It will eventually find C and **share
**its reference, which has been valued by *Mary*. This fact prevents it
from ever being in an reference relationship with *pro *(the implicit
subject), and this, rather than outright defective intervention
ungrammaticality, explains why subject control is impossible under
passivization. Control is still allowed, and indeed, *Mary*<sub>i
</sub>*was promised PRO*<sub>i </sub>*to win *works (at least for many
speakers) under that interpretation.

The piece that is missing from Landau’s system that close implementation
in this system reveals is that there’s nothing actually preventing the
**probe **from continuing on after it’s entered into a relationship with
(embedded) C. If **probe**s can continue exhaustively, why can’t this
one keep looking in C’s **Comp **after having hit C itself?

(Landau 2004) needs the C intermediary to implement Partial Control.
It’s not entirely clear from the original paper whether PC isn’t
achieved through relationship with C and PRO simultaneously — with
direct reference (to *Mary*) mediated through the direct relationship
with the T complex and the implicit additional referents through C. That
doesn’t *seem *to be what Landau has in mind — reference seems to go
exclusively through C as a transmission medium — but if the author has
no objection, perhaps this system could actually be implemented that
way.

However, it’s more likely that what’s intended is that C is a *phase
*head, and **probe**s can’t **probe **over *phase *boundaries.
Therefore, C has the **barrier feature **from the previous chapter, and
all **probe**s stop at the C head. The relationship is mediated through
C because a more direct relationship is simply forbidden.

In light of that, however, it is worth noting that the analysis for
Hebrew OC in the same work relied on an *exact *feature match between
\[+T, +Agr\] on C and \[+T, +Agr\] on T eliminating both pairs,
effectively rendering the *phase *transparent. In those cases, EC
obtains, and the matrix functional head (T or *v *depending on the
specific phenomenon represented) does indeed enter into a relationship
with PRO directly. So, *phases *are sometimes transparent for Landau and
sometimes not, and the mechanism by which this is enforced can’t really
be the one advertised (presence of a \[+R\] feature on C) because we
know that **probe**s can go as far as they like in this system. For the
purposes of faithful implementation of the system as Landau seems to
have intended it, \[+R\] C heads bear the **barrier **feature in this
system.

### <span id="anchor-110"></span>Hidden Assumptions

The assumptions on this theory are a bit more subtle. One — that the
*probe *will continue past C, establishing more links in Partial Control
cases than the theory advertises, is real but probably not
consequential. Either Landau intended there to be features on the
relevant C heads that block such probes, or there are two links — one
direct and one mediated — between PRO and its binder rather than one.
Two links probably isn’t a problem, since the aim of the analysis is for
the reference of PRO to expand beyond that inherinted from its
antecedent anyway; it’s the *presence of the mediated reference *that
really matters.

However, the existence of multiple-probe itself is not so innocent. One
then needs to be careful what probes are used for. For example, in the
system implementation, it’s assumed that **select **is a ***probe***,
meaning that a head — *v*, say — can keep ***probe***ing even *after
*it’s found an external argument, possibly gathering several.
Mechanisms have to be put in place to prevent this in situations where
it’s not wanted. The typical one would be “case freezing” — not allowing
arguments to be considered as goals after their case features are
valued. That’s fine as far as it goes, but it runs into trouble on
standard defective intervention analyses, where it is precisely the
presence of an “inactive” (i.e. case-valued) element that prevents the
probe from reaching its canonical goal.

Presumably none of this is a problem for Landau’s system because it
doesn’t conceive of **select **in probe-goal terms. As “hidden”
assumptions go, this admittedly isn’t very revealing, but it is
nevertheless the kind of detail that one doesn’t notice before making an
honest implementation attempt.


[Back](jherring-4) — [Forth](jherring-6)
