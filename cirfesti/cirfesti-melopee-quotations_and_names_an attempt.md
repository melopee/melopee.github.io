For the little that I've understand, names and quotations are debated. This article describes another attempt to solve the problem: how to properly quote names and titles, allowing _every_ possible names and quotations, without impossibilities due to morphology famyma'o (denpabu).

## Impossible properties of actual situation
By actual situation is meaned all proposals which are to quote or not quote some words, from lojban brivla to rafsi and foreign words.
As people had noticed, they all have pros and cons, but all what-it-seems to be flaws. Let's look some:
* CLL:
  * denpabu after cmevla
  * cmevla cannot begin with {la} or {lai} or {doi}
* Dotsite:
  * denpabu after cmevla
  * {la} or {lai} or {doi} are accepted in cmevla, but all cmevla which have to begin with denpabu
* {lu li'u}:
  * all that between these two words is taken as a quotation
* {lo'u le'u}:
  * same as {lu li'u} but for ungrammatical sentence(s)
* {zo}:
  * quote only the next word
* {zoi}:
  * quote the next word, with delimiters: additional word has to be chosen to separate the foreign words from the rest, e.g. {gy} in {zoi gy. Homo Sapiens .gy}
* {la'o}:
  * works as {zoi}, but add the semantic of name to the quoted words

These rules want to fight about one trick of lojban's morphology: words can be parsed without space or with. However, there is another rule which can be noted from actual situation: all what's between the quotation *is quoted*. It sounds strange saying like that, but see: it is not possible to insert a thing between {lu} and {li'u}, or between {zoi gy.} and {.gy}; without making this thing quoted. This property makes actual quotations kinda absolute, and so, easier to use. But this rule leads also to another problem: all cmavo-for-quotations with such properties will fail.

It is not hard to understand. Let's say that S is the startor, and T the terminator. So `S somequotation T` means `"somequotation"`. But what if we choose to have `"quotation T somequotation S anotherquotation"`? Because of the previously-mentionned rule, all that between S and T is quoted, so a trial might be `S quotation T somequotation S anotherquotation T`. Which expands, due to cmavo, to `"quotation" somequotation "anotherquotation"`, and so fails. You can try: it works for {lu}/{li'u}, {la'o}, {zoi}, and even {la} and its denpabu: names including what's-lojban-transcripts-denpabu (i.e. pause or glottal stop) fall in this principle. And it is not totally astonishing at the end: if quotations or names can be _any_ sounds or letters, why hoping quote names which are made of the cmavo startor and terminator?

## An escape
The solution that I propose is inspired from [LaTeX](https://en.wikipedia.org/wiki/LaTeX) commands. Shortly, LaTeX is a descriptive programming language for writing documents. So it uses several commands, as programming languages in general, to achieve graphical effects. Let's look at one of these.
The command `\section{My Title}` will displays `"My Title"` (with some pre-done font and size effects, but it's unimportant). And how to display `"} qswqds \section{I'm a joke title"` with `\section` command?
LaTeX does this fairly simply, with the command `\section{\} qswqds \textbackslash section\{I'm a joke title}`. And, no jokes, all is done: it achieves to write terminator, `}`, and startor, `\section{`.

I don't see any problem with such solutions, and so want to put it in lojban. Let's see how it's working.

The core is that this command uses, as terminator and startor, some characters which aren't display, i.e., quoted, without other charaters: and so, to display them, LaTeX uses escape characters: `\}` will display `"}"`, `\{` will display `"{"` `\textbackslash section` will display `"\section"` (`\\` is already defined in LaTeX, which explains why `\textbackslash ` is used instead).

Not regarding LaTeX specificities, I propose to use for lojban a startor and a terminator which will not be displayed, quoted, or taken in name; and, an escape character.

For names, let's reassign {la}, as startor; and {ku}, as terminator; and {zo}, as escape; for this purpose.
Examples:
  * {la lalxu ku citka}: means that the person named "lalxu" eats (neglecting some unuseful atemporal semantic considerations about "citka")
  * {la simpson ku citka}: means the same for the person named "simpson"
  * {la zo ku lalxu zo la ku citka}: same for the person named "kulalxula"
  * {la nuzoku.alofa ku trutca la tonga}: means that "Nuku'alofa is the capital of Tonga"
  * {la emil zo zo la ku ciska lo cutka}: means "Émile Zola writes books"
  
Same changes can be made with {lo'u}/{le'u}, {lu}/{li'u}...

This additional use that I put to {zo} seems to be coherent with {zo} semantic and safe from a grammatical point of view.
In this proposal, {ku} isn't an elidable terminator for {la}: it is heavier, but safier.

And what means {la ku ku}, or {la la ku}, or {la zo ku}? The latter is simple: just decide if {zo} needs to be escape or not. Previously, I have said that LaTeX did not display the startor and terminator, but it is incomplete: some produce errors and some not. For lojban, I think that the simplest solution is to say that {la ku ku} and {la la ku} are ungrammatical, not wanting to look which {ku} is the last or which {la} is the first; and where they are applying; in parsing. Also, combinations of {la} and {ku} are also forbidden, e.g. {la ku ku ku ku ku lalxu la la ku la ku citka} is forbidden.

## Unification
I've don't see any need to continue to distinguish the actual different quotations, since they derivate all from the same concept, ""display words/chains-of-sounds"". But if persons find it useful to separate names from quotations; from foreign from ungrammatical from grammatical... I just ask that all of theses cmavo are clearly defined, e.g. `la broda == lo se cmene zo broda`.

About that, {zoi} is a bit more tricky to change, since the denpabu are vital for limitors to be separate from the quoted word. However, when I say previously that all words was gibberish, it was a bit false since {zoi} works, because, for example, {gy.} can be quoted with limitors different from {gy.} and {.gy}. Due to this possibility to use any limitors, {zoi} can quote any words using limitors which are not problematics. But these limitors are also heavy to use, maybe it is for that ZOhOI, MEhOI were invented; and so I recommand, if people really want to have different cmavo for several distinctions, to use new cmavo which will have a semantic identical to {zoi}, and will work identical to new {la} and new {ku}, with new {zo}.

A last precision about morphology: this proposal doesn't take care of consonant-ending or not, which is the official use of denpabu, separate this kind of words from this other to not be merged; instead, it prefers to say that 'all between {la} and {ku} is a name', and that's all. No need to separate names from the other words, since {la} and {ku} provide a little separated world.

[//]: # (It's useful to have {zo} for grammatical quotations, since even {lu} and {li'u} can quote `"lu li'u"`, they cannot quote only {lu} or only {li'u})


