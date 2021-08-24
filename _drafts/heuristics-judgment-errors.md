---
layout: post
title: Avoiding Systematic Errors When Making Judgments Under Uncertainty
---

Technology leaders---technical team leads, engineering managers, architects, and CTOs---make thousands of decisions, small and large, in a year. We say, colloquially, that some of these decisions require good *judgment*. This article is aimed at the technology decision maker and makes the following points: (a) a judgment is different from other kinds of decisions; (b) all judgments are subject to a degree of error; (c) one source of error is the method of making judgments; (d) we can improve the quality of our judgments, relatively easily and across a broad spectrum of scenarios if we recognize those sources.

## Decisions Under Uncertainty

Many decisions are based on beliefs concerning the likelihood of uncertain events. The beliefs may be expressed in statements like:

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

Did the above stories sound very reasonable? Did you find it hard to imagine how else could our ancestors have reasonably made these judgments? If so, you and I can agree that the heuristics used there are very useful. We should thank our ancestors for just throwing the spear at the prey before calculating ballistic trajectories, and not wondering if the probability distribution of tigers appearing in grasses are Gaussian (nope) or Poisson (yep) before running away.

Unfortunately, each of the heuristics can lead to errors under certain circumstances in systematic and predictable ways. Even more unfortunately, we use these heuristics when we do have the time to follow a more accurate process. We can't help it---the human brain is lazy and yet does a very good job of convincing us that it has done the work. Have you ever made a decision that felt "just right" but found it hard to explain why? Have you made a decision of major consequence based on "gut feel"? Have you mulled over a problem where suddenly something went "ting!" in your mind, and you arrived at the decision---and moreover, you got a feeling of satisfaction and convinction that the decision was right? This is our brain encouraging us to make a decision under uncertainty. We all know the parable of the donkey that starved when put exactly equidistant from two equally delectable and large bales of hay, because the poor donkey could not compute which bale of hay to go towards. Our emotions override our logic for us to survive. (Or so I believe--with zero data and less calcualation.)

## Technology Decisions

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

- We may not know, with certainty, what infrastructure the system will need in future; let's say up to a point, getting more infrastructure in the colocation facility is relatively inexpensive, but once our needs exceed the capacity of the rack, cage or floor, it becomes relatively very expensive to get more infrastructure; on the cloud, adding more infrastructure is more expensive per-unit, but scales linearly (or even better, sub-linearly, if our volumes are high); the uncertainty in future usage creates a risk of not using money optimally. We could ask business stakeholders for very precise forecasts of future growth and try to map that to increase in infrastructure, but we know that their forecasts are uncertain, and mapping increase in number of users to more infrastructure has always been more of an art than science.
- When figuring out how to address the (known) gaps, we encounter a new technology that could address a gap, but we've no experience with it; we don't know for sure if it will meet the performance needs of our system at peak load. We could run a test, but tests costs time and money.
- The cloud provider charges by usage for data transfer; we don't know precisely how much data transfer our system does, since we never needed to measure that in the past; we could start measuring it now to get a precise idea, but that will take time and cost (we will have to buy measurement software).

As you can see, there are several places where getting more (precise) information has a high cost, and in some cases we don't even consider the possibility because the cost and effort is nigh impossible (we may not even know where to start and may have to undertake a research project of unknown scope to determine that). We have to make estimates.

If you have said or heard statements like this, someone is making estimates:

* I think that...
* Chances are that...
* It is unlikely that...

In this article I am assuming that the decision makers have adequate knowledge and skills.Without those, we won't know what to estimate. The point of this article is that knowledge and skills are not enough. Beyond a certain point, acquiring more technical knowledge and skills provide diminishing returns and uncertainty becomes a dominant factor in making high quality judgments.

Increasing technical knowledge is not in conflict with increasing the ability to make better estimates. We can do both in parallel. Improving the ability to make better estimates is something that will provide benefits in a wide variety of situations. Importantly, once we have improved our technical knowledge and skills to some extent, it is time to pay attention to our ability to estimate.

## Shortcuts for Estimations



## Representativeness

**Abstract Definition.** When deciding how likely it is than an object *a* belongs to class *A*, or event *a* is the result of process *A*, we substitute it with the easier problem: how similar is *a* to my mental stereotype of *A*.

**TODO Lab experiment.** 

**Discussion.** In reality, *a* could belong to *A*, *B*, *C*, ... of which only one or two classes are of interest. When deciding the likelihood that *a* belongs to the classes of interest, we must not only consider how similar *a* is to any of these classes but also how frequent these classes are, overall.

TODO diagram.

TODO conrete example.

## TODO Problems with Availability

* **Availability**. When deciding if class *A* is more frequent or likely than class *B* we substitute it with the easier problem: how easily can I recally instances of *A* vs *B*?

## TODO Problems with Anchoring

* **Anchoring**. When estimating quantities numerically, we don't think of *base rates* and *confidence intervals* and instead solve a simpler problem: start with an initial number (the anchor), and adjust up or down until we feel we've adjusted enough.





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