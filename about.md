---
layout: page
title: About
permalink: /about/
---

Tools that propose derivations, search the literature, grind through algebra and
suggest ansätze are no longer speculative. They sit on physicists' desks
alongside the Mathematica notebook and the morning arXiv listing. What is
uncertain is not whether this is happening, but what it does to the practice:
to what counts as a derivation and who counts as its author, to how taste and
physical intuition get formed, to the long apprenticeship of becoming a
theorist, and to the ordinary daily texture of the work.

These questions currently get discussed in three places. Benchmark papers,
which measure what a model can and cannot do but say little about what it is
like to work alongside one. Broad public commentary about AI, which rarely
touches the specifics of any actual field. And scattered personal blogs, group
chats and corridor conversations, which are often the most honest of the three
and the least likely to be read by anyone who wasn't already in the room.

All are useful. None of them is a common room.

## Why the narrow scope

This is a blog for people working in high-energy theory and quantum gravity.
Not because the questions stop at the boundary of the field, but because a
conversation is better when the participants share enough background that
nobody has to start from the beginning. You should be able to write "the
replica trick did the work, the model just recognised it" here and be
understood without a paragraph of setup.

We would rather host a hundred people who can talk to each other at full
technical depth than a thousand who have to keep translating.

## Who should write

We are especially interested in people who do not otherwise have a platform for
this kind of reflection, and who would rather not set up and maintain a blog of
their own. Established researchers with an audience are welcome, but so are PhD
students still forming a view, postdocs who have quietly changed how they work
and not told anyone, and people who tried these tools on a real calculation,
found them useless, and want to say exactly where they failed.

The range of reactions — enthusiasm, indifference, anxiety, contempt,
curiosity — is itself part of the record.

## What we want to publish

Contributions can take any form and any length. A three-paragraph account of a
calculation a model helped or badly mishandled. A longer essay on what physical
understanding means when a machine can produce correct steps without any. An
institutional critique of how a department, a journal, a collaboration or a lab
is handling this. An uncomfortable personal account of how your relationship to
your own work has shifted.

We are not looking for a house style or a party line, and we do not expect
consensus — we rather hope not to find it. We would publish something short and
true over something polished that does not quite believe itself. What we want
to preserve is an honest record of what it felt like to do theoretical physics
while the tools of the trade were changing underneath it.

This is a communal project. It will only be as good, as varied and as honest as
the people who write for it.

## Who runs this

{% for editor in site.data.editors %}
### {{ editor.name }}

{% if editor.role %}*{{ editor.role }}{% if editor.affiliation %}, {{ editor.affiliation }}{% endif %}*{% endif %}

{{ editor.bio }}
{% endfor %}
