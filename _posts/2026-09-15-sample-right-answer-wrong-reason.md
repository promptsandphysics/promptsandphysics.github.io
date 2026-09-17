---
title: "The right answer for the wrong reason"
date: 2026-09-15
author: "A. N. Example"
affiliation: "Institute for Example Studies"
career_stage: "Postdoc"
tags: [Experiments and practice, Understanding, Holography]
sample: true
excerpt_override: "A sample post. It exists to show how a typical contribution renders, including mathematics."
ai_disclosure: >-
  This post is a formatting sample written to demonstrate the layout of the
  disclosure box. A real disclosure would say which tool was used and for what.
---

*This is a sample post. It is here to show what a contribution looks like once
published — headings, mathematics, quotations, the disclosure box below. Delete
this file before launch.*

I asked it to reproduce a standard holographic entanglement entropy
computation. The setup was ordinary: a boundary interval $A$ of length $\ell$ in
a two-dimensional CFT, the bulk a pure AdS$_3$ slice with radius $L$, and I
wanted the Ryu–Takayanagi answer.

It wrote down

$$
S_A = \frac{\text{Area}(\gamma_A)}{4 G_N}
$$

and then, correctly, the geodesic length giving

$$
S_A = \frac{c}{3} \log\!\left(\frac{\ell}{\epsilon}\right),
\qquad c = \frac{3L}{2 G_N}.
$$

Which is right. The central charge is right, the logarithm is right, the cutoff
$\epsilon$ appears in the right place.

## Where it went wrong

Then I asked why the factor of $1/3$ rather than $1/6$, and it explained,
fluently and at length, that the interval has two endpoints — which is the
correct reason. So far so good. But when I changed the setup to a single
endpoint on a boundary with a physical edge, it gave me the same $c/3$ with the
same two-endpoint justification, apparently unable to notice that the
justification it had just given no longer applied.

> The failure was not the algebra. The algebra was flawless throughout. The
> failure was that the explanation and the computation were not connected to
> each other in the way they are connected in a person who understands the
> problem.

This is the thing I keep running into and cannot get comfortable with. A
student who produced the first answer with that reasoning would, nine times out
of ten, get the second one right too, because the reasoning is what generated
the answer. Here the reasoning appears to be generated alongside the answer,
from the same place, and the fact that they agreed the first time told me
nothing about whether they would agree the second time.

## What I actually do now

I have settled into using it roughly the way I use a very fast, very
well-read colleague who I do not trust:

1. Ask for the structure of an argument, never the conclusion.
2. Rebuild anything I intend to use.
3. Assume that a confident explanation is evidence about fluency, not about correctness.

That third one is the expensive habit to acquire, and I do not think I have
fully acquired it.
