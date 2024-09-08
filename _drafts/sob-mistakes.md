---
layout: post
title: Three Mental Shortcuts to Avoid
---

TODO: hook

TODO: takeaway

## Decision Making Process Model

All models are wrong; some are useful.  Here is a model of the process of decision making that I will use to make concrete the aspects of decision making that are relevant to this discussion.

![A Model of Decision Making](/assets/img/decision-making-process-model.lucid.png)

The process goes like this:
1. We imagine a desired state.
1. We observe the current reality.
1. We analyze differences between the desired state and reality.
1. We identify the gap between the desired state and reality.
1. We think of different actions we could take to reduce the gap.
1. We arrive at some options.  An option consists of things we know for sure ("Facts") and things we don't ("Unknowns").  We cannot evaluate an option that has unknown components.
1. We engage is estimation: the process of converting an unknown into a probabilistic quantity.
1. The result is estimates that stand-in for the unknowns.
1. Evaluation criteria consists of attributes of an option to consider, and perhaps a weight for each attribute.  Evaluation is the process of finding or estimating the value of each attribute for each option, and then using a decision algorithm to compute the desirability of each option.  The algorithm usually is *filter*-then-*rank*.
1. From the filtered and ranked options, we choose the "best" one. We then implement it via actions.
1. Our actions affect reality, leading to a new one.
1. Let us define risk as the *probability* that the option we choose is not the best one, multiplied by the *cost* or *negative impact* that we will incur if our option indeed did not turn out to be the best one.


## Reducing Risk


One way of reducing risk is to reduce the cost or negative impact of each option.  Instead of implementing an option in an all-or-nothing effort, we can try it in a smaller scope and therefore reduce the cost or negative impact, reducing overall risk.  In this article, we assume that we've already done so and cannot make the scope any smaller.

The remaining way of reducing risk is to reduce the probability of choosing a non-optimal option.  There are two ways of reducing this probability.

The first way is to reduce the unknowns by increasing the known facts.  This is done by study and experimentation.  However, beyond some point, it is not possible to acquire more facts or such acquisition has very high costs (higher than the possible benefit of choosing the best option).  Let's assume we have acquired as many facts as is possible and economical.  That still leaves us with some unknowns.

At the point, the only thing we can do to reduce our risks is to convert our unknowns into probabilistic figures by using estimation.  There are three kinds of estimation problems:

1. **Classification.** How likely is object `α` to belong to the class `A`?
1. **Likehood.** Does `A` occur more frequently than `B`?
1. **Value.** What is the likely value of `α`? (More precisely, what is the range of values `α` could have with probability `p`?)

Once the problem statement has been identified, one or more methods can be applied to solve it.  For a good collection of methods, see <a href="https://www.amazon.com/How-Decide-Simple-Making-Choices/dp/B088P4XLVB/" target="_blank">How to Decide</a> by Annie Duke and <a href="https://www.amazon.com/How-Measure-Anything-Intangibles-Business/dp/1118539273/" target="_blank">How to Measure Anything</a> by Douglas W. Hubbard.

Selecting the right method requires that we define the estimation problem correctly.  And therein lies a big problem.


## Heuristics

There is much research supporting the idea that our brains use two entirely different processes for solving problems.  The common phrase describing this dichotomy is "the **System 1** and **System 2** ways of thought".  For more information, see <a href="https://en.wikipedia.org/wiki/Dual_process_theory" target="_blank">Dual-Process Theory</a> and <a href="https://en.wikipedia.org/wiki/Thinking,_Fast_and_Slow" target="_blank">Thinking, Fast and Slow</a> by Daniel Kahneman.

*System 1* is fast, automatic, efforless, emotional, stereotypical and unconscious.  Our brain engages it for things like:

1. Localizing the direction of the source of a sound
1. Solving `2 + 2  = ...`
1. Understanding simple sentences

*System 2* is slow, deliberate, effortful, logical, calculating and conscious.  Our brain engages it for things like:

1. Determining the nature of the source of an unfamiliar sound
1. Solving `35 x 17 = ...`
1. Determining the correctness of a complex logical argument

The estimation problems mentioned earlier require *System 2* processes.  However, our brains tend to substitute such estimation problems with a different problem and solve it via *System 1*.  We are not even aware that we are doing so.  Specifically:

| Problem to be Solved | Problem we *Actually* Solve |
|--------------------|---------------------|
| How **likely** is object `α` to belong to the class `A`? | How **similar** is object `α` to stereotypes of class `A`? |
| Does `A` occur more **frequently** than `B`? | Can I **remember** more instances of `A` than `B`? |
| What is the likely value of `α`? | Pick a number and adjust it up or down: does it feels "right" |


## Heuristic 1: Similarity

### Similarity: Arresting the Heuristic

### Similarity: Example

## Heuristic 2: Observability

### Observability: Arresting the Heuristic

### Observability: Example

## Heuristic 3: Baseline

### Observability: Arresting the Heuristic

### Observability: Example

## Postscript

**Pop psychology.** The internet and bookstores are full of content about how the human mind works and how we make decisions (or should make them). Much of this content is not fact based: it is opinion, speculation or pseudo-science.  Most authors over-generalize from a limited set of anecdotes, and present this as universal truth, or cherry pick their facts and do not make an honest attempt at finding or presenting evidence that might contradict their opinion.  The right way to deal with such content is either to recognize and treat it as such: an opinion that *might* be applicable but is not guaranteed to.

In addition, some fact-based content is outdated or proven to be incorrect, but persists in our minds.  An example is the[Dunning-Kruger Effect](https://en.wikipedia.org/wiki/Dunning%E2%80%93Kruger_effect)?  This effect is actually a statistical artifact due to the phenomenon of [regression to the mean](https://en.wikipedia.org/wiki/Regression_toward_the_mean).  Yet, it gets cited a lot because it is so compelling.  On encountering it, we nod and think "of course, this explains so many things"; unfortunately it does not and just perpetuates a potentially dangerous myth and unnecessarily demeans some groups of people.  There are *many* such "explanations" of mental phenomenon that feel very compelling, but might be incorrect.

**Evidence based research.**  The specialized nature, technical jargon and sheer volume of evidence-based research in the human mind is not easily accessible to the layperson.  Additionally, a research paper is also a kind of speculation, until it is peer reviewed and its results replicated---I, for one, do not have the time and skill to track which research results were proven over time and which fell by the wayside.  Believing every new piece of research that is reported in the media as gospel truth is dangerous.

Fortunately, some practising scientists have made the effort to summarize vast amount of research conducted over decades into language that is accessible to us, without sacrificing accuracy.  Some authors I trust are:

**How the human mind works and develops**:

1. [Steven Pinker](https://www.amazon.com/stores/Steven-Pinker/author/B000AQ3GGO)
1. [Janet Wild Astington](https://www.amazon.com/stores/Janet-W.-Astington/author/B001HD3VVE)
1. [Michael Tomasello](https://www.amazon.com/stores/Michael-Tomasello/author/B001HCZO4W)

**How to reduce uncertainty**:
1. [Douglas W. Hubbard](https://www.amazon.com/stores/Douglas-W.-Hubbard/author/B001JSJHIS)
1. [Annie Duke](https://www.amazon.com/stores/Annie-Duke/author/B001K88E4U)

**Cognitive biases**:
1. [Daniel Kahneman](https://www.amazon.com/stores/Daniel-Kahneman/author/B001ILFNQG)


