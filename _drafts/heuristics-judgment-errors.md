---
layout: post
title: Avoiding Systematic Errors When Making Judgments Under Uncertainty
---

Technology leaders---technical team leads, engineering managers, architects, and CTOs---make thousands of decisions, small and large, in a year. We say, colloquially, that some of these decisions require good *judgment*. This article is aimed at the technology decision maker and makes the following points: (a) a judgment is different from other kinds of decisions; (b) all judgments are subject to a degree of error; (c) one source of error is the method of making judgments; (d) we can improve the quality of our judgments, relatively easily and across a broad spectrum of scenarios if we recognize those sources.

## Technology Decisions And Uncertainty

Making technology judgments requires three ingredients: (a) knowledge and skills; (b) information; and (c) ability to estimate uncertain quantities. It may seem that (a) and (b) alone are sufficient. However, in any but the most trivial judgments, we do not have perfect information. The available information is usually incomplete. Even with the information we do have, different sources may disagree about the value. For information we do not have, Uncertainty creates risk. We could get more information to reduce the risk. However, getting more information has a cost in terms of time and risk. If the value of information (the risk reduced) is less than the cost of getting it, we should stop and make the decision now. But what do we do about the missing information? We use estimates in its place.

As a concrete example, consider the decision: should we migrate our CRM system, that runs on physical servers in a rented colocation facility, to the public cloud? The factors we are considering are: (a) will it run well on the cloud, i.e. technical feasibility? (b) how much will it cost to run in the long term? (c) how much will the one time cost of moving the CRM to the cloud be? (d) are the previous two costs, over 3-5 years, less than the cost of continuing to run it where it is now?

To make the decision, we need to:

- know how it works and what infrastructure it needs now and in the future;
- know how the selected cloud provider(s) systems work;
- map the needs of our system to what is available and identify the gaps or differences;
- figure out how to address the gaps, so it could run successfully on the cloud;
- calculate what it costs to run currently;
- calcualte what it will cost to migrate and run in the ckoud;
- decide which cost is higher, over a period of time.

There are several sources of uncertainty that create risks. Here is a non-exhaustive list of uncertainties and how we might reduce the uncertainty by getting more information:

- We may not know what infrastructure the system will need in future. We could ask business stakeholders for very precise forecasts of future growth and try to map that to increase in infrastructure, but we know that their forecasts are uncertain, and mapping increase in number of users to more infrastructure has always been more of an art than science.
- When figuring out how to address the (known) gaps, we encounter a new technology that could address a gap, but we've no experience with it; we don't know for sure if it will meet the performance needs of our system at peak load. We could run some tests, but tests require time, effort and money.
- The cloud provider charges by usage for data transfer; we don't know precisely how much data transfer our system does, since we never needed to measure that in the past; we could start measuring it now to get a precise idea, but that will take time and cost (we will have to buy measurement software).

As you can see, there are several places where getting more accurate information has a high cost, and in some cases the cost and effort is nigh impossible. We may not even know where to start and may have to undertake a research project of unknown scope to determine *how* to get the information. The alternative: make estimates.

In this article I am assuming that the decision makers *have adequate knowledge and skills*.Without those, we won't know what to estimate. The point of this article is that knowledge and skills are not enough. Beyond a certain point, acquiring more technical knowledge and skills provide diminishing returns and uncertainty becomes a dominant factor in making higher quality judgments.

Increasing technical knowledge is not in conflict with increasing the ability to make better estimates. We can do both in parallel. Additionally, improving the ability to make better estimates is something that will provide benefits in a wide variety of situations.

## Estimates and Heuristics

Estimates are often expressed as beliefs concerning the likelihood of uncertain events, in statements like:

- I think that...
- Chances are that...
- It is unlikely that...

How does one arrive at the belief? One possibility is to create a mental model of the problem space including causes, effects and parameters; gather all reasonably available data; ascertain a range of values where precise data is not available; do some calculations; and finally express the result of the calculations as a statement of belief. But sometimes we don't have the time to go through all these steps. With limited time, do we execute a faster, perhaps less accurate, version of the above process? For example, do we do make coarser estimations and execute less accurate calculations?

No. We use an entirely different process.

(By "we" I mean humans. Apologies to our AI overlords who are reading this in the far future.)

There is a lot of evidence that we employ two distinct modes of thinking: intuitively (System 1) and systematically (System 2). System 2 is what I described earlier. When thinking intuitively, people assess the probability of an uncertain event or the value of an uncertain quantity using a limited number of heuristic principles. The heuristics substitute a complex task with a simpler one.

Our ancestors had to make a lot of decisions with imperfect information in limited time. The human brain evolved to make estimate probabilities quickly with limited accuracy, rather than slowly with great accuracy. Here are three "just so" stories that are plausible about decisions our ancestors would have had to make and how they'd make them:

* We are gathering food in the forest. We encounter a colorful berry that we haven't quite seen before. We need to decide if the newly encountered berry is safe or unsafe to eat. Food is scarce and we will be rewarded for getting more, but it won't do if the tribal chief gets the runnies or worse. We substitute this question with the easier question: is this berry similar to my mental stereotype of berries known to be safe to eat?
* We are stalking animals to hunt in the prairie grass. We spot some movement in the grass. We need to decide the relative liklihood of a movement in the grass is due to a tiger (catastrophic) or gazelle (benign or beneficial). This is a hard question that requires knowing the relative frequencies of tiger and gazelle populations in the area of interest at the time of year. We substitute it with the easier question: how many gazelles and tigers can I recall seeing lately and what was the relative frequency?
* We are stalking animals to hunt in the prairie grass. It takes time to find and stalk them and we get only two chances a day on average. We've spotted some animals. We need to decide whether we can throw our spear far and accurately enough to hit an animal with >50% probability, or if should we try to get closer but risk spooking the animal. This is a hard question that would require us to keep track of the distances of our past throws, the conditions under which we executed them and what we know about the sensitivity of the animal. We substitute it with the easier question: what was the distance of my last successful throw, and am I feeling strong/weaker than that time?

Did the above stories sound very reasonable? Did you find it hard to imagine how else could our ancestors have reasonably made these judgments? If so, you and I can agree that the heuristics used there are very useful. We should thank our ancestors for just throwing the spear at the prey before calculating ballistic trajectories, and not wondering if the probability distribution of tigers appearing in grasses are Gaussian (nope) or Poisson (yep) before running away. While the above are made up stories, there is a lot of evidence that the substitution of complex tasks with specific simpler heuristics does occur.

Unfortunately, each of the heuristics can lead to errors under certain circumstances in systematic and predictable ways. Even more unfortunately, we use these heuristics when we do have the time to follow a more accurate process. We can't help it---the human brain is lazy and yet does a very good job of convincing us that it has done the work. Have you ever made a decision that felt "just right" but found it hard to explain why? Have you made a decision of major consequence based on "gut feel"? Have you mulled over a problem where suddenly something went "ting!" in your mind, and you arrived at the decision---and moreover, you got a feeling of satisfaction and convinction that the decision was right? This is our brain encouraging us to make a decision under uncertainty by taking a "shortcut"--a simpler heuristic. Our emotions override our logic for us to survive. We all know the parable of the logical donkey that starved when put exactly equidistant from two equally delectable and large bales of hay, because it could not logically decide which bale of hay to go towards.

There are three heuristics that are commonly used, each for a different kind of problem. We discuss them below.

## Representativeness

*Abstract Definition.* When deciding how likely it is than an object *a* belongs to class *A*, or event *a* is the result of process *A*, we substitute it with the easier problem: how similar is *a* to my mental stereotype of *A*. If *a* is highly representative of *A*, it is assumed that *a* is highly likely to be an instance of *A*. Sounds logical?

The error occurs because *a* could potentially belong to several classes: *A*, *B*, *C*,... Even if there are no explicit multiple classes, there are at least two: *A* and *not A* (aka *A'*). The probability that *a* belongs to *A* depends on two factors:

1. How probable is *A*, in the first place? This is called *prior probability*. If we knew nothing about *a*, it's probability of belonging to *A* is just the prior probability.
2. Now, given information about *a*, how much does that information increase or decrease the probability of *a* belonging to *A*.

This is a fundamental concept in probability theory---conditional probability---but when the problem is framed in the above manner, we tend to forget factor (1), leading to severe errors.

**TODO diagram.**

*Experiment.* Subjects were divided into three groups. Two were shown brief personality descriptions of several individuals, allegedly drawn randomly from a population of 100 people who were either engineers or lawyers. In the first group, subjects were told the population consisted of 70 engineers and 30 lawyers. In the second group, subjects were told that the population consisted of 30 engineers and 70 lawyers. In the third group, the subjects were not given any description at all, just one of the two population compositions.

As expected, subjects in the third group, who were not given any description at all, predicted the likelihood of a random individual to be a lawyer or engineer as per the population composition they were given. That was all the information they had to go on.

The two groups who were given a description effectively *ignored the population composition*. For example, a description like "an introverted, analytical man" was considered to be predicting an engineer, regardless of what the population composition was.

The effect remained even when the descriptions were *deliberately* designed to provide no information about occupational likelhood. For example, some subjects were given a descripion like:

> Dick is a 30 year old man. He is married with no children. A man of high ability and high motivation, he promises to be quite successful in his field. He is well liked by his colleagues.

With this description, subjects inferred that the description does not predict the occupation at all. They should have behaved liked the third group and used the population distribution as the likelihood of the individual being a lawyer or engineer. Instead, subjects inferred the likelihood of 50% either way.

What's going on here?

First, consider, how strongly does a personality description like "introverted; analytical" predict someone will turn out to be an engineer? 100%? I'd say no. A fair number of engineers are extroveted, and many are intuitive rather than analytical. It's also the case that no one is 100% introverted all the time or analytical all the time. In which case, the subjects should have considered the *prior probability* of a random person being an engineer or lawyer (the population distribution) and then modified it with their perception of how much information the description adds. That's not what happened. Subjects ignored the prior probability.

Secondly, when the "information" was not informative at all, subjects could not make up their minds whether the described individual was a lawyer or engineer. They *should have* fallen back on the population distribution to determine the likelihood, like the third group, but they did not.

Representativness causes several errors:

1. *Insensitivity to prior probabilities.* When given a description, we latch on to the the most closely matching explanation ignoring the probabilities that an explanation that matches less closely but occurs much often could be the right one. This is illustrated in the example above.
2. *Insensitivity to sample size.* We may know about the distribution of the total population. We take a small sample. We expect the distribution of the small sample to be the same as the overall population, and are surprised when it deviates significantly. We look for causal explanations, when in reality, the explanation is simply chance.
3. *Misconceptions about probability.* The following tosses of a fair coin are equally likely: (1) H-T-H-T-T-H; (2) H-H-H-T-T-T; (3) H-H-H-H-H-T. People think that (1) is more likely.
4. *Overestimating the predictive power of evidence.*

### TODO Give one or more technology example

## TODO Availability

*Abstract Defintion.* When deciding if class *A* is more frequent or likely than class *B* we substitute it with the easier problem: how easily can I recall instances of *A* vs *B*? We ignore whether *A* is easier to recall than *B*, or if we are likely to be exposed to *A* and *B* relative to their probability in our personal experience.


### Systemtatic Errors Arising From Availability

### TODO Give one or more technology example

## TODO Anchoring

* **Anchoring**. When estimating quantities numerically, we don't think of *base rates* and *confidence intervals* and instead solve a simpler problem: start with an initial number (the anchor), and adjust up or down until we feel we've adjusted enough.

### Systemtatic Errors Arising From Anchoring

### TODO Give one or more technology example




Most common heuristics:
- Representativeness
- Availability
- Anchoring and Adjustment

Representativeness
- Abstract definition
- Concrete example
- Lab study
- Application

Availability
- Abstract definition
- Concrete example
- Lab study
- Application

Anchoring
- Abstract definition
- Concrete example
- Lab study
- Application

Conclusions