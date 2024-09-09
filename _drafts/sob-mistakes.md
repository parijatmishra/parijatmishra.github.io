---
layout: post
title: Three Mental Shortcuts to Avoid
---

TODO: hook

TODO: takeaway

## Decision Making Process Model

> All models are wrong. Some are useful. ---Everybody

The model below introduces the key aspects of the process of decision making that are relevant to this discussion.

![A Model of Decision Making](/assets/img/decision-making-process-model.lucid.png)

In this model, the process of decision making is:

1. We imagine a desired state.
1. We observe the current reality.
1. We analyze differences between the desired state and reality.
1. We identify the gap between the desired state and reality.
1. We imagine one or more ways we could reduce the gap.
1. We arrive at some options. For each option, there are attributes whose values we know ("facts") and attributes whose values we don't ("unknowns").
1. For each unknown, we attempt to estimate its value or class.
1. The resulting estimates---quantities or class with probabilities---stand-in for the unknowns.
1. Evaluation is the process of using a decision algorithm to compute the desirability of each option using the values of its attributes. The algorithm usually is _filter-and-rank_, guided by some evaluation criteria.
1. From the filtered and ranked options, we choose the "best" one. We then implement it via actions.
1. Our actions affect reality, leading to a new one.
1. There is a chance that we might not choose the best option. Let's call the negative impact of this "risk".

Risk occurs due to flaws at each step of the process. I want to focus on what I think is a surprising aspect of estimation of unknowns (steps 7-8) that increases risk, without us being aware it.

## Defining Risk

Imagine if we could access a multiverse. If we had `N` options, we would spin up `N` universes, exactly the same, except for the option we exercised in that universe. We could then observe the _cost_ of exercising an option and the _gain/loss_ resulting from the option. One of them would be objectively the best according to our evalation criteria. Unfortunately we cannot do this, but still, there is at least conceptually a best option.

If we had all the necessary facts, and no unknowns, for each option, we would be able to deterministically compute the gain/loss and cost of each option and then deterministically choose the best option according to our decision algorithm and evaluation criteria. Unfortunately, we usually can't eliminate all the unknowns.

So, there _is_ an objective best option, but we don't know which one it is
because of the unknowns. The best we can do determine a probabilistic value or _estimate_ for each unknown, evaluate the options, and choose the optimal one.

This means that if we make an incorrect estimate for an unknown, our evaluation may pick the non-optimal option. Choosing the non-optimal option means we may incur more cost for less gain, compared to the optimal option, whatever that is.

Let's define _risk_ of an options as: (the _probability_ of choosing that option, times the _negative impact_ of choosing that option). Let's define overall risk as the sum of the risks of each option.

We want to reduce overall risk.

## Reducing Risk

One way of reducing risk is to reduce the negative impact of a chosen option. Instead of implementing an option in an all-or-nothing effort, we can try it in a smaller/limited scope. If it works, increase the scope. If it does not, we incurred some loss (or less gain) but we can try another option now. In this article, we assume that we've already done so and cannot make the scope any smaller.

Another way of reducing risks is to reduce the unknowns by acquiring more facts. This is done by research and experimentation. Beyond some point, the cost of acquisition of facts becomes higher than their value. Let's assume we have acquired as many facts as is possible and economical. That still leaves us with some unknowns.

At this point, the only thing we can do is to convert our unknowns into probabilistic figures by using estimation. Choosing a good estimation method will reduce our risk.

Most estimation problems boil down to:

1. **Classification.** How likely is object `α` to belong to the class `A`?
1. **Likehood.** Does `A` occur more frequently than `B`?
1. **Value.** What is the likely value of `α`? (More precisely, what is the range of values `α` could have with probability `p`?)

Once the problem statement has been identified, a range of methods ranging from back-of-the-envelope to tools-and-number-crunching can be applied.

To get an idea of the available methods, see:

1. <a href="https://www.amazon.com/How-Decide-Simple-Making-Choices/dp/B088P4XLVB/" target="_blank"></a> by Annie Duke---quick and simple methods, oriented towards personal decisions
1. <a href="https://www.amazon.com/How-Measure-Anything-Intangibles-Business/dp/1118539273/" target="_blank">How to Measure Anything: Finding the Value of Intangibles in Business</a> by Douglas W. Hubbard---ranging from quick and simple to laborious, oriented towards business/corporate settings

Selecting the right method requires that we define the estimation problem correctly. And therein lies a big problem.

## Heuristics

There is much research supporting the idea that our brains use two different processes for solving problems. The common phrase describing this dichotomy is "the **System 1** and **System 2** ways of thought". For more information, see <a href="https://en.wikipedia.org/wiki/Dual_process_theory" target="_blank">Dual-Process Theory</a> and <a href="https://en.wikipedia.org/wiki/Thinking,_Fast_and_Slow" target="_blank">Thinking, Fast and Slow</a> by Daniel Kahneman.

_System 1_ is unconscious and automatic, fast, effortless, emotional, and relies on stereotypes. Our brain engages it for things like:

1. Localizing the direction of the source of a sound
1. Solving `2 + 2  = ...`
1. Understanding simple sentences
1. Reacting emotionally to a picture

_System 2_ is conscious and deliberate, slow, effortful, emotionless, and relies on logic and computation. Our brain engages it for things like:

1. Determining the nature of the source of an unfamiliar sound
1. Solving `35 x 17 = ...`
1. Determining the correctness of a complex logical argument
1. Finding an obscure or hidden object in a picture

The estimation problems mentioned earlier require _System 2_ thinking. But: **Our brain does not let us see the estimation problem for what it is. It has evolved to substitute them with an easier problem. And we are not always aware of the substitution.**

Specifically, our brain substitutes the problem on the left with the problem on the right:

| Problem to be Solved                                     | Problem we _Actually_ Solve                                       |
| -------------------------------------------------------- | ----------------------------------------------------------------- |
| How _likely_ is it that object `α` belongs to class `A`? | How _similar_ is `α` to the _stereotype_ of class `A`?            |
| Does `A` occur more _frequently_ than `B`?               | Can I _remember_ more instances of `A` than `B`?                  |
| What is the _likely_ value of `α`?                       | _Pick_ a number and _adjust_ it up or down until it _feels right_ |

<a href="https://en.wikipedia.org/wiki/Daniel_Kahneman" target="_blank">Daniel Kahneman</a>, winner of the _Nobel Memorial Prize in Economic Sciences_, _Presidential Medal of Freedom_ and other awards, calls this process of substitution, "heuristics".

Without proof, I speculate that these heuristics are evolutionarily adaptive behaviors that helped our ancestors survive in a hostile world, where math and computers did not exist and quick and risk-averse decisions were better than optimal decisions. It is time to rethink them.

## Heuristic 1: Similarity

### Similarity: Experimental Evidence

Several experiments were conducted where participants were asked to estimate the probability that a given individual, picked from a population of engineers and lawyers, was actually an engineer. In each experiment, participants were divided into two groups; each group was given different information about the individual and the population, and the average of their predictions were compared.

**Experiment A: Predicting Class When No Other Information is Available.**

Group 1 was told that the population consisted of 70 engineers and 30 lawyers. Group 2 was told that the population consisted of 30 engineers and 70 lawyers. They were given no additional facts about the picked individual. The average prediction for each group was inline exactly the population ratio.

**Experiment B: Predicting Class When Some Predictive Information is Present.**

Group 1 was told that the population consisted of 70 engineers and 30 lawyers. Group 2 was told that the population consisted of 30 engineers and 70 lawyers. Additionally, participants in each group were given _brief and fictitious_ personality descriptions of the individual (different participants got different descriptions). The descriptions were designed to match the stereotype of either an engineer or lawyer. For e.g., the description designed to match the stereotype of an engineer was "an introverted, analytical man", while the description matching the stereotype was "an extroverted, intuitive man".

Participants in both groups, individually, over-indexed on the description and seemingly ignored the population ratios. That is, everyone, in either group, who saw the description "an introverted, analytical man" predicted that the individual was an engineer with near 100% confidence, and vice versa.

**The problem**. Are all engineers are introverted and analytical? Will all introverted and analytical people seek engineering as an occupation? There are other factors involved: is there a good and afforable engineering school they have access to? Were any influential parental figures lawyers? Was the school debate team captain a more welcoming person than the head of the physics club? Did the school have luminary alumnis who were lawyers? What about other unknown personality characteristics? Thinking of these factors, would you say the conclusion that the description predicts an engineer is a slam-dunk? If not, there is a percentage of engineers who do not match the description. There is _some_ probability that an individual who matches the stereotype does not belong to that group. Therefore the prediction should not have been made with 100% confidence---the population ratio should have been taken into account. It seemingly was not.

### Similarity: Arresting the Heuristic

### Similarity: Example

## Heuristic 2: Observability

### Observability: Arresting the Heuristic

### Observability: Example

## Heuristic 3: Baseline

### Observability: Arresting the Heuristic

### Observability: Example

## Postscript

**Pop psychology.** The internet and bookstores are full of content about how the human mind works and how we make decisions (or should make them). Much of this content is not fact based: it is opinion, speculation or pseudo-science. Most authors over-generalize from a limited set of anecdotes, and present this as universal truth, or cherry pick their facts and do not make an honest attempt at finding or presenting evidence that might contradict their opinion. The right way to deal with such content is either to recognize and treat it as such: an opinion that _might_ be applicable but is not guaranteed to.

In addition, some fact-based content is outdated or proven to be incorrect, but persists in our minds. An example is the[Dunning-Kruger Effect](https://en.wikipedia.org/wiki/Dunning%E2%80%93Kruger_effect)? This effect is actually a statistical artifact due to the phenomenon of [regression to the mean](https://en.wikipedia.org/wiki/Regression_toward_the_mean). Yet, it gets cited a lot because it is so compelling. On encountering it, we nod and think "of course, this explains so many things"; unfortunately it does not and just perpetuates a potentially dangerous myth and unnecessarily demeans some groups of people. There are _many_ such "explanations" of mental phenomenon that feel very compelling, but might be incorrect.

**Evidence based research.** The specialized nature, technical jargon and sheer volume of evidence-based research in the human mind is not easily accessible to the layperson. Additionally, a research paper is also a kind of speculation, until it is peer reviewed and its results replicated---I, for one, do not have the time and skill to track which research results were proven over time and which fell by the wayside. Believing every new piece of research that is reported in the media as gospel truth is dangerous.

Fortunately, some practising scientists have made the effort to summarize vast amount of research conducted over decades into language that is accessible to us, without sacrificing accuracy. Some authors I trust are:

**How the human mind works and develops**:

1. [Steven Pinker](https://www.amazon.com/stores/Steven-Pinker/author/B000AQ3GGO)
1. [Janet Wild Astington](https://www.amazon.com/stores/Janet-W.-Astington/author/B001HD3VVE)
1. [Michael Tomasello](https://www.amazon.com/stores/Michael-Tomasello/author/B001HCZO4W)

**How to reduce uncertainty**:

1. [Douglas W. Hubbard](https://www.amazon.com/stores/Douglas-W.-Hubbard/author/B001JSJHIS)
1. [Annie Duke](https://www.amazon.com/stores/Annie-Duke/author/B001K88E4U)

**Cognitive biases**:

1. [Daniel Kahneman](https://www.amazon.com/stores/Daniel-Kahneman/author/B001ILFNQG)
