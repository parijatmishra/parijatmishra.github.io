---
layout: post
title: Three Situations When Our Brain Works Against Us
---

Our brain is out to get us! When we have to make critical decisions under
uncertainty, it uses in appropriate mental shortcuts instead of solid reasoning.
And we are not even aware that this is happening.

**Example.**

A software vendor describes their product and points out several benefits that
they think are especially relevant to you. They give examples of some companies
who bought their product. They give you prices for various volumes or tiers. The
decision you need to make: should you buy this?

Making the decision requires estimating several unknowns, in a series of steps:

1. _How likely_ is your company to significantly benefit from the product? This
   would determine whether the product is worth investigating further.
1. _How frequent_ are the various use cases for the product in your company?
   This would determine what use cases to investigate first---the most frequent
   ones (it's too much effort to investigate all).
1. _What is the likely benefit in dollar value_? You estimate the likely benefit
   of the product for an instance of each use case you investigated.

You could stop at any of the steps. If you made it through, you compare the
total _estimated_ benefit to the _known_ cost, and make a go or no-go decision.

Nicely done!

Oh wait... The above is a theoretical model. In reality, at every step of the
process, you are estimating some unknowns, and if your estimates are wrong you
will make the wrong decision: you will either overypay by buying the product, or
miss an opportunity by not buying it.

**Mental Shorcuts.**

All the previous questions are about _probability_. There are two ways of
dealing with probability: intuition, and methodical reasoning. When faced with a
problem that required methodical reasoning, our brain fools us. It replaces:

1. The harder problem of "how likely?" with the easier "how similar?". Instead
   of anwering, "How likely is my company to belong to the set of companies that
   could benefit from the product?", our brain asks, "How similar is my company
   to the stereotype of companies benefiting from the product?". Unfortunately,
   your company might be quite different from the stereotype of the product's
   users but still have a great need for the product.
1. The harder problem of "how frequent?" with the easier "how easy to recall?"
   Instead of answering, "How common are the use cases of the product?" our
   brain asks "How easily can I remember instances of these use cases?" Chances
   are, unless you are intimately familiar with the product's use cases, you
   likely have encountered the use cases infrequently or not at all, and you
   don't know the true frequency.
1. The harder problem of "how much?" with the easier "pick an arbitrary number
   that we can relate to; now adjust up/down---does it feel about right?".

These mental shortcuts are evolutionarily adaptive mechanisms that helped our
ancestors survive in a hostile world. They helped our ancestors make decisions
_quickly_, when a slow decision was worse than a sub-optimal decision.

Imagine a pre-historic human foraging for fruits in a forst, and trying to
methodically compute the probability that the rustling in the trees is a lion or
something harmless. Yup, that human got eaten one day while he/she was still
calculating.

Our ancestors were the ones who did _not_ compute probabilities laboriously but
instead used heuristics: I remember someone was eaten by a lion 2 days ago; that
lion might be around---let's run away.

In the modern world, few decisions require making life-and-death decisions in
seconds or minutes. We _can_ take the time to think things through, but our
brain _does not want_ to do that.

## Decision Making Process Model

> All models are wrong. Some are useful. ---Everybody

The model below introduces the key aspects of the process of decision making
that are relevant to this discussion.

![A Model of Decision Making](/assets/img/decision-making-process-model.lucid.png)

In this model, the process of decision making is:

1. We imagine a desired state.
1. We observe the current reality.
1. We do a lot of thinking.
1. We identify the gap.
1. We imagine ways we could reduce the gap.
1. We arrive at some options. For each option, there are attributes whose values
   we know ("facts") and attributes whose values we don't ("unknowns").
1. For each unknown, we attempt to estimate it.
1. The resulting estimates replace the unknowns.
1. We use a decision algorithm to compute the desirability of each option using
   the values of its attributes. The algorithm usually is _filter-and-rank_,
   guided by some evaluation criteria.
1. We choose the top ranked option and implement it.
1. Our actions affect reality.
1. If we didn't choose the best option, we are not as close to the desired state
   as we wanted. This is risk.

Risk can occur due to flaws at any step of the process. I want to focus on the
steps that require estimation.

## Defining Risk

Conceptually, there _is_ an objective best option, but we don't know which one
it is because of unknowns.

If we had all the necessary facts with no unknowns, we would be able to
_deterministically_ compute the _gain_ and _cost_ of each option.

We usually can't eliminate all the unknowns. The best we can do is to make an
_estimate_ for each unknown. This leads to an _estimated_ _gain_ and _cost_ of
each option.

If we make an incorrect estimate, our decision algorithm may pick the
non-optimal option. Choosing the non-optimal option means we may incur more cost
for less gain, compared to the optimal option. Let's call the difference between
the chosen option and the optional option the _negative impact_.

Let's define _risk_ of an option as: the _probability_ of choosing that option,
times the _negative impact_ of choosing that option.

The overall risk is simply the sum of the risks of each option.

## Estimation and Heuristics

Most estimation problems boil down to:

1. _Likelihood._ How likely is object `α` to belong to the class `A`?
1. _Frequency._ Does `A` occur more frequently than `B`?
1. _Value._ What is the likely value of `α`? (More precisely, what is the range
   of values `α` could have with probability `p`?)

Once the problem statement has been identified, a range of methods ranging from
back-of-the-envelope to tools-and-number-crunching can be applied.

To get an idea of the available methods, see:

1. [How to Decide: Simple Tools for Making Better Choices](https://www.amazon.com/How-Decide-Simple-Making-Choices/dp/B088P4XLVB/)
1. [How to Measure Anything: Finding the Value of Intangibles in Business](https://www.amazon.com/How-Measure-Anything-Intangibles-Business/dp/1118539273/)

Selecting the right method requires that we define the estimation problem
correctly. And therein lies a big problem: **our brain does not let us see the
estimation problem for what it really is.**

## System 1 and System 2

There is much research supporting the idea that our brains use [two entirely
different processes](https://en.wikipedia.org/wiki/Dual_process_theory) for
solving problems, called **System 1** and **System 2**.

_System 1_ is unconscious and automatic, fast, effortless, emotional, and relies
on stereotypes. Our brain engages it for things like:

1. Localizing the direction of the source of a sound
1. Solving `2 + 2  = ...`
1. Understanding simple sentences
1. Reacting emotionally to a picture

_System 2_ is conscious and deliberate, slow, effortful, emotionless, and relies
on logic and computation. Our brain engages it for things like:

1. Determining the nature of the source of an unfamiliar sound
1. Solving `35 x 17 = ...`
1. Determining the correctness of a complex logical argument
1. Finding an obscure or hidden object in a picture

The estimation problems mentioned earlier require _System 2_ thinking, which
requires deliberate effort. Our brain subsitutes the problem with an easier one
that requires a _System 1_ heuristic, without us being aware of this
substitution.

| Problem to be Solved                                                     | Heuristic                                                                                     |
| ------------------------------------------------------------------------ | --------------------------------------------------------------------------------------------- |
| **Likelihood.** How _likely_ is it that object `α` belongs to class `A`? | **Representativeness.** How _similar_ is `α` to the _stereotype_ of class `A`?                |
| **Frequency.** Does `A` occur more _frequently_ than `B`?                | **Availability.** Can I _remember_ more instances of `A` than `B`?                            |
| **Value.** What is the _likely_ value of `α`?                            | **Anchoring.** _Pick_ an (arbitrary) number and _adjust_ it up or down until it _feels right_ |

## Heuristic 1: Representativeness

When faced with the question "How _likely_ is it that object `α` belongs to
class A?", our brain uses the heuristic "How _similar_ is object `α` to the
stereotype of class `A` (or `not-A`)?." These are not the same questions. To
see why, read the experimental evidence below.

Problems with this heuristic: **(a)** We think the limited information about
similarity is more predictive than it really is; we neglect to think of other
pertitent unknowns about similarity; **(b)** We ignore the "base-rate" of class
`A`: how common is the class, to start with?

### Representativeness: Experimental Evidence

Researchers conducted several experiments, asking subjects to estimate the
probability that a given individual was an engineer or lawyer. They divided
subjects into two groups for each experiment. Group 1 was told that the
population consisted of 70 engineers and 30 lawyers. Group 2 was told that the
population consisted of 30 engineers and 70 lawyers.

**Experiment A: Predicting Class When No Other Information is Available.**

The researchers gave subjects no additional information about the given
individual.

Subjects in group 1 predicted there was a 70% chance the individual was an
engineer, and those in group 2 predicted a 30% chance.

This is as expected: since subjects had no other information than the population
ratio, they used it for their likelihood predictions. So far, so good.

Things become interesting when _additional information_ is present.

**Experiment B: Predicting Class When Some Predictive Information is Present.**

The researchers constructed brief descriptions of a stereotypical engineer ("an
introverted, analytical man") and stereotypical lawyer ("an extroverted man who
loves debates"). They randomly gave one or other description to subjects across
the groups.

Subjects in both groups predicted that the individual was an engineer or lawyer
with _near 100% probability_, in accordance to the description they were given.
They completely ignored the population ratio they were given beforehand.

This is not logical.

While the description "an introverted, analytical man" does arguable match the
stereotypical engineer, do _all_ such individuals become engineers? Can at least
a few lawyers be introverted and analytical? What about other (unstated)
personanlity traits that could also affect choice of occupation? What about
environmental factors like parent's occupations or preferences? There are many
reasons an introverted and analytical person might have become a lawyer instead
of an engineer: just from the description itself, the probability is not 100%.

**Experiment C: Predicting Class When Non-Predictive Informatoin is Present.**

The researchers constructed detailed descriptions of the individual, which
nevertheless had no predictive power: it could apply either to an engineer or
lawyer equally well. E.g.: _"Dick is a 30 year old man. He is married with no
children. A man of high ability and motivation, he promises to be quite
successful in his field. He is well liked by his colleagues."_

Subjects in both groups predicted that the individual is _equally likely_ to be
engineer or lawyer. They completely ignored the population ratio they were given
beforehand.

Again, this is not logical.

The description did not provide any useful information about the occupation and
subjects should have just ignored it. Instead, subjects relied almost entirely
on the inconclusive description. Since the description was equally _similar_ to
a stereotypical engineer or lawyer, they incorrectly concluded that the
individual was equally _likely_ to be an engineer or lawyer.

## Heuristic 2: Availability

When faced with the question "Is the _frequency_ of class `A` greater than
`B`?", our brain uses the heuristic "Can I _recall_ more examples of class `A`
than class `B`?" These are not the same questions. To see why, read the
experimental evidence below.

Problems with this heuristic: **(a)** Whether we can recall instances of class
`A` has more to do with how our memory works (some things are easier to recall
than others) than the real frequency of `A`; **(b)** we are over-confident that
our own exposure to `A` is representative of its true prevalence.

### Availability: Experimental Evidence

**Experiment A: First Letter or Third Letter.**

Researchers chose a small set of letters from the English alphabet which occur
more often in the third place than in the first place of words in English.

They randomly assigned letters to subjects---all native English speakers---and
asked: "do more words start with this letter, or do more more words contain this
letter in the third position." Almost everyone judged, incorrectly, that more
words _start_ with the letter they were given.

The effect can be explained by the observation that it is much easier to recall
words that start with a given letter, than to recall words that contain some
letter in the third place. What effectively happened was, the subjects asked
themselves, "How many words can I recall starting with this letter? How many
words with this letter in third place?" Since they could recall more words which
started with the given letter, they predicted this class was more likely.

**Experiment B: More Men or More Women.**

Researchers divided subjects into multiple groups, and recited a list of
well-known personalities to each group. Different groups were presented with
different lists: in some lists the men were more famous than women, and in
others the women were more famous. They then asked each group: were there more
men than women in the list presented to them?

Each group incorrectly judged that the list presented had more names of the
gender that had the more famous names. In reality, the lists contained an equal
number of men and women.

This effect can be explained by the observation that it is easier to recall
famous names compared to less famous or unknown names.

**Experiment C: Probability of Traffic Accidents.**

When people are asked to estimate the probability of traffic accidents, they
rate the probability higher if they have recently observed an accident, and rate
it lower if they haven't observed an accident recently.

## Heuristic 3: Anchoring

When faced with the question "What is the likely value of `α`?", our brain uses
the heuristic "Guess an _arbitrary_ number; then, adjust it up or down until it
_feels right_". Sounds unbelievable? Not something you'd ever do? See the
experimental evidence below.

Problems with this heuristic: **(a)** Our initial guess is "anchored" to---is
influenced highly by---the last number we paid attention to, _even if that is
not related to the current situation_; **(b)** We are over-confident about how
close to the real value our initial guess is; because of this over-confidence,
we do not spend the effort required to gain factual information; **(c)** We
start feeling right too quickly, before making enough adjustment.

### Anchoring: Experimental Evidence

**Experiment A: Estimating Unfamiliar Quantities.**

Researchers divided subjects into several groups. For each group, they spun a
wheel-of-fortune and announced the resulting number. The researchers then posed
an estimation question and asked the participants:

- Do you think the number from the wheel-of-fortune is higher or lower than the
  quantity we just asked you to estimate?
- Now, create an estimate for the question we just asked you.

For each group and each question, the arbitrary number from the wheel-of-furtune
had a significant effect on the estimate.

E..g, one of the questions was: "What percentage of African countries are
members of the United Nations?" Group 1 was given the number 10 from the
wheel-of-furtune; their average estimate was that 25% of African countries are
UN members. Group 2 was given the number 65 from the wheel-of-furtune; their
average estiamte was that 45% of African countries are UN members.

Even though the subjects _knew_ that a number from a wheel-of-fortune has
nothing to do with the question posed, they were strongly influenced by it.

(Both groups were far off the mark: the real number is 90%.)

**Experiment B: Estimating the Product of 8 numbers.**

Researchers divided high-school students into two groups, gave them a
multiplication problem and asked them to estimate the result in less than 5
seconds. The time limit ensured that no one would be able to actually _do_ the
computation, and be forced to _estimate_.

Group 1 was asked to estimate `8 × 7 × 6 × 5 × 4 × 3 × 2 × 1`; their median
estimate was `2250`. Group 2 was asked to estimate `1 × 2 × 3 × 4 × 5 × 6 × 7 ×
8`; their median estimate was `512`.

Note that the numbers are exactly the same but in different orders. Why the big
difference in estimates?

This effect can be explained by the observations:

- Under time pressure, people would perform the first 2-3 multiplications, and
  then guess a number than was ~3 times higher. Those who were given the numbers
  in descending order started with a larger number than those who were given the
  numbers in ascending order.
- Group 1 would adjust their guess _down_ to account for the descending order;
  Group 2 would adjust their guess _up_ to account for the ascending order.
- Almost always, we don't adjust enough.

(The correct result for both questions is `40,320`. Both groups were very far
off.)

## Postscript

**Pop psychology.** The internet and bookstores are full of content about how
the human mind works and how we make decisions (or should make them). Much of
this content is not fact based: it is opinion, speculation or pseudo-science.
Most authors over-generalize from a limited set of anecdotes, and present this
as universal truth, or cherry pick their facts and do not make an honest attempt
at finding or presenting evidence that might contradict their opinion. The right
way to deal with such content is to recognize and treat it as such: an opinion
that _might_ be applicable but is not guaranteed to.

The content that is _bona-fide_ fact-based is sometimes outdated or proven to be
incorrect, but persists in our minds. Examples are the [Dunning-Kruger
Effect](https://en.wikipedia.org/wiki/Dunning%E2%80%93Kruger_effect), and the
book [Outliers: The Story of Success](https://www.amazon.com/dp/0316017930/) by
Malcolm Gladwell. The authors reported what they found, extrapolated to some
conclusion, and did not attempt to cheat anyone. Subsequently, the evidence
they've relied on has been shown to have different, equally or more plausible
explanations. However, their original conclusions were very compelling, and they
get cited a lot; the caveats do not.

The damage of unjustified confidence in particular narratives is not just to the
individuals claiming them, but to organizations and entire societies.

**Evidence based research.**

There _is_ obervation- or experiment-based research about the human mind. But
the specialized nature, technical jargon and sheer volume of evidence-based
research about the human mind is not easily accessible to the layperson.

We need people who can summarize research for the layperson. They need to be
able to keep track of research and interpret which pieces have been validated
enough vs which are speculative, and then they need to choose the highlights and
rewrite them in non-tecnical language. This is no small request!

The best people to do so would be academics who are actively researching and
teaching in the field. Is there any incentive for them to take the effort of
summarizing and translating tecnical research for lay-people? No.

> You have never heard true condescension until you have heard academics
> pronounce the word 'popularizer' --- [James
> Boyle](https://law.duke.edu/fac/boyle).

Fortunately, some practising scientists have made the effort to summarize vast
amount of research conducted over decades into language that is accessible to
us, without sacrificing accuracy. Some authors I trust are:

**How the human mind works and develops**:

1. [Steven Pinker](https://www.amazon.com/stores/Steven-Pinker/author/B000AQ3GGO)
1. [Janet Wild Astington](https://www.amazon.com/stores/Janet-W.-Astington/author/B001HD3VVE)
1. [Michael Tomasello](https://www.amazon.com/stores/Michael-Tomasello/author/B001HCZO4W)

**How to reduce uncertainty**:

1. [Douglas W. Hubbard](https://www.amazon.com/stores/Douglas-W.-Hubbard/author/B001JSJHIS)
1. [Annie Duke](https://www.amazon.com/stores/Annie-Duke/author/B001K88E4U)

**Cognitive biases**:

1. [Daniel Kahneman](https://www.amazon.com/stores/Daniel-Kahneman/author/B001ILFNQG)
