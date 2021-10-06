---
layout: post
title: Uncertainty, Mental Shortcuts, and Errors in Technology Decisions
---

If you are a technology leader, you know you make decisions, big or small, all the time. You also know that each decision carries some risk. Risks arise from several sources. One of the most common sources of risk in technology decisions is *uncertainty*, due to lack of information. Behavioral phychologists and economists have spent decades researching how humans make decisions under uncertainty. It turns out that humans use a few mental shortcuts to make estimates of uncertain quantities. These shortcuts often lead to systematic errors and incorrect decisions. Sadly, we are largely unaware we are using them. In this article I will elaborate on how uncertainty creates risk, mental shortcuts for estimating uncertain values, the kinds of errors the shortcuts create, and how to identify and stop the mental shortcuts. I hope this will help you reduce risks and increase the quality of your decisions, with only a little effort.

If you have seen instances where any of these shortcuts were being used, I would love to hear from you. I will update this article with your anecdotes if I find your stories clear and illustrative. Please do not share anything confidential, but do provide sufficient detail that a reader of this blog unfamiliar with your situation can understand the core idea.

## Risks and Uncertainty

For concreteness, let us imagine we are a startup, building a web application as part of our product. We need to make many decisions: what to build, how to build it, how to run it etc. To make good decisions, we need *information*. We need to know the priorities of different features our web application could have so we spend our meager resources on the ones that users want the most. We need to know how heavily the application will be used to be able to run it with good performance without over-provisioning it because that would be wasteful.

We often encounter gaps in available information. Consider these scenarios:

- The startup has done user surveys and research to indicate there is interest in its product, but the sample sizes are small and in artificial conditions. It does not know for sure if enough people will pay for that product to make the investment in developing and running it viable.
- We are evaluating two queuing systems. One is easy to get started with and operate but does not scale well. The other scales well but is complicated to get started with and operate---we will have to invest more time and effort to use it. We don't know how much load our queuing system will need to support in future.

A lack of information creates *uncertainty*, which in turn makes it probable that the option we choose is not the one that would lead to the best outcome.

Let us define risk as the *probability* that the option we choose is not the best one multiplied by *cost* that we will incur if our option indeed did not turn out to be the best one.

There are two ways to reduce risk:
1. Reduce the *cost* of making the wrong decision.
2. Reduce the *probability* of making the wrong decision.

There are several techniques for reducing the cost of making a mistake, such as building low-cost minimum viable products to get early feedback and using software abstraction layers to make it easy to swap products. Let us assume our hypothetical startup has used such techniques to reduce the cost of making a mistake. What remains? The probability of choosing a non-optimal option, which is determined by the gaps in available information.

Sometimes, we simply can't get more information. For example, in the case of the queuing system, while we've reduced the cost of error, the only way we can reduce the probability of error is to know what our future needs are. This may simply not be possible.

At other times, we *could* get more information but the *value* of the information is not worth the *cost* of doing so. For example, the easiest way to find out if people will pay for our product with zero cost is to not build the product ourselves but let someone else do it. Their success or failure will give us very valuable information. But the cost of the information is that we don't have a startup at all, or at least we are late to the market and have lost the initial chunk of users. Most startups would say that the cost outweighs the value of this information.

In a nutshell, there are times where we cannot or will not fill in gaps in available information, which creates uncertainty, which creates a probability that we will make a non-optimal decision, which creates risk.

## Uncertainty and Estimations

Can we do something about the uncertainty created by missing information? Actually, we already do. We substitute missing information with *estimates* and make predictions based on them. You have made an estimate based prediction if you've ever stated something like:

- I think that...
- Chances are that...
- It is unlikely that...

Since we are making estimates all the time, it pays to get get better at making them. Good estimates reduce uncertainty and therefore the probability of making an incorrect decision, just like information does.

To make better estimates, we can do two things.

1. We can increase our knowledge. Greater knowledge improves our mental model of processes, inputs and outputs, and helps us identify which variables make the most impact on outputs.
2. We can get better at judging uncertain quantities.

I am assuming readers are well aware of the importance of knowledge and are doing all they can already in that regard. The focus of this article is on the latter.

## Estimations and Heuristics

The problem with making estimates is that humans don't make them well, in most situations. Let's think about how does one make an estimate. What happens when we say "Chances are that..."?

Consider a problem our ancestors may have encountered, where good estimation was the difference between survival and death. Our proverbial ancestor is walking along a mountainous landscape, hunting and gathering. He spots a lion in the distance. He has to decide whether to run away and start hunting somewhere else, or maintain a cautious distance and continue on their way.

There is a lot of evidence that humans employ two distinct modes of thinking: intuitive and quick (System 1) and systematic and plodding (System 2).

Let's talk about the System 2 method of solving this problem first. This method starts by creating a model of the problem space including processes, inputs and outputs. Processes and inputs can have variables associated with them. We gather all reasonably available information. For the information we don't have, we *ascertain a range of values*. Then we do some calculations guided by the model. Finally, we express the result of the calculations as an estimate.

In our ancestors case, the process is *hungry lions eat people*, and *if the lion we to chase me, I need enough head start to run away*. The input variables are *How quickly can the lion get to me?* and *How hungry is the lion?*. Our ancestor may have very good information about a lion's speed and conclude *The lion can get to me in 30 seconds*. They may not have good information about the lion's hunger but could make an estimate such as *The lion is sitting next to a half-eaten carcass; it is probably not very hungry and therefore unlikely to chase me if I stay some distance away*. Conclusion: proceed cautiously.

Often, we don't have the time to go through all these steps. When time is limited, do we use System 2, perhaps with fewer calculations? Surely our ancestor did not do detailed measurements of lion's distance and speed, or look up a lion's dietary requirements in a book.

When we don't have time, our brains an entirely different process called System 1. System 1 works via mental shortcuts, or **heuristics**, to make estimates. Heuristics work by not answering the original estimation problem, but subsituting them with a subtly different and easier problem and answering that.

In our ancestor's case, using System 1, their thinking would go along these lines: last week I heard about a hunter getting eaten by a lion. Lions are dangerous. It's not worth thinking about whether or not the lion is likely to chase me, because the cost of making an error there is very high. Conclusion: run away.

Alternatively, our ancestor may have thought like this: I've not heard of a hunter getting eaten by a lion in months. That only happens in the dry, lean seasons. There is probably no reason to run away. Conclusion: proceed cautiously.

As you can see, in the made up story above, our ancestor used a more intuitive way of solving the problem that depended on subjective experience and recollection. They used a "mental shortcut" or heuristic: what do I recall about similar situations.

You and I can agree that heuristics have served our ancestors well and kept them safe. They are useful, especially when time is scarce.

Unfortunately, we use heuristics even when we *do have the time* to follow a more accurate process, and where the risk of getting things wrong is economic, not life and death. We do this unintentionally. The human brain is lazy and yet does a very good job of convincing us that it has done the work.

Have you ever made a decision that felt "just right" but found it hard to explain why? Have you made a decision of major consequence based on a strong "gut feeling"? Have you mulled over and over on a problem where suddenly something went "ting!" in your mind, and you arrived at the decision, and moreover, were very confident that your decision is right? If so, your brain probably used a heuristic.

Since heuristics work by answering a different question from the original problem, they can lead to systematic errors and depending on the circumstances, severe ones. Combined with the fact we use them without even realizing we are doing so, we have a double whammy: we don't know that some of our estimation methods are error-prone and we don't know when we are using those methods.

There are three core heuristics that I will discuss in this article.

* Representativeness: our brain substitutes the hard question of *How likely?* with the simpler question *How similar?*.
* Availability: our brain substitutes the hard question of *How frequent?* with the simpler question *How easy to recall?*
* Anchoring and Adjustment: our brain substitutes the hard question of *how much* with the simpler question of *pick a number and adjust up or down---do you feel you've adjusted enough?*.

## Heuristic 1: Representativeness

When faced with problems of the form:

> how likely is that an instance **a** belongs to class **A**

we substitute is with a simpler problem:

> how much does **a** resemble **A**?

If *a* is highly *representative* of *A*, the heuristic assumes that *a* is highly *likely* to be an instance of *A*. Sounds logical? Not so, mathematically. The probability that *a* belongs to *A* depends on two independent variables:

1. How probable are the classes *A* and *not A*, in the first place, independent of any *a*?
2. Given the information about *a* how likely is it an instance of *A*, independent of the probability of *A* having occured.

These variables are then combined to give a final probability that *a* belongs to *A*. This is a fundamental concept in probability theory called conditional probability. However, the heuristic of representativeness ignores probability (1) and gives too much importance to probability (2). This leads to bad estimates.

### Experimental Evidence

An experiment was conducted where subjects had to estimate the probability that an individual, picked from a population of engineers and lawyers, was actually an engineer. The subjects were divided into several groups and given different information.

#### Predictions when information about the individual was not present

* Group A1: subjects were told that the poupulation consisted of 70 engineers and 30 lawyers. They were given no information about the individual. As expected, the group on average predicted that the individual was 70% likely to be an engineer.

* Group A2: subjects were told that the poupulation consisted of 30 engineers and 70 lawyers. They were given no information about the individual. As expected, the group on average predicted that the individual was 30% likely to be an engineer.

Groups A1 and A2 used only the prior probabilities (correctly), as no other information was available. They also did not show a bias towards any occupation.

#### Predictions when information about the individual was present had predictive power

* Group B1: subjects were told that the poupulation consisted of 70 engineers and 30 lawyers. Additionally they were given a brief fictitious "personality description" of the individual. The description had very little information but would match the stereotype of an engineer or lawyer. For exampke, one description was "an introverted, analytical man". This group on average estimated the likelihood of the individual being an engineer or lawyer, depending on what stereotype they were presented, to be almost 100%.

* Group B2: subjects were told that the poupulation consisted of 30 engineers and 70 lawyers. Additionally they were given a brief fictitious "personality description" of the individual, like group B1. They made predictions similar to group B1.

Both group B1 and B2 seemingly completely ignored the proportion of engineers in the population when deciding whether a randomly picked individual would be an engineer. They gave enormous weight to the piece of information they had. They effectively said "if the description of the individual resembles an engineer, the individual is highly likely to be an engineer".

Arguably, "an introverted, analytical man" does match the stereotype of an engineer. (At least, that's what the authors of the experimental study concluded. I mean no offense to any profession.) But how much information does this description contain? More precisely, how much predictive power does this information have?

Consider: are you sure *all* engineers are introverted and analytical? If not, there is a percentage of engineers who do not match the description. The additional information presented by the description does not increase the probability to 100%.

Consider: can lawyers be introverted and analytical? If so, the description could match a portion of lawyers. There is at least some probability that the described individual could be a lawyer.

Consider: will all introverted and analytical people seek engineering as an occupation? There are other factors involved: is there a good and afforable engineering school they have access to? Were any of their parents or influential parental figures lawyers? Was the school debate team captain a more welcoming person or the head of the physics club? Did their school have luminary alumnis who were engineers, or lawyers? What about other unknown personality characteristics? Thinking of these factors, would you say the conclusion that the description predicts an engineer is a slam-dunk?

The description could have tweaked the prior probabilities, but not by a lot. Yet, given just a smidgen of information of dubious value, both groups B1 and B2 ignored the prior probabilities entirely.

#### Predictions when information about the individual was present but had no predictive power

* Group C1: subjects were told that the poupulation consisted of 70 engineers and 30 lawyers. Additionally they were given detailed personality descriptions. However, the descriptions were deliberately designed not to match any occupational stereotypes and more generally, not give any clues as to occupation. For example, a description could be "Dick is a 30 year old man. He is married with no children. A man of high ability and motivation, he promises to be quite successful in his field. He is well liked by his colleagues." This group on average predicted that the individual is equally likely to be an engineer or lawyer.

* Group C2: subjects were told that the poupulation consisted of 30 engineers and 70 lawyers. They were also given the same personality descriptions like group C1. This group also on average made the same predictions as group C1.

In this case, the additional information about the individual that the groups got was deliberaly inconclusive. They should have disregarded the information and just used prior probabilities like group A1 and A2. However, the inconclusive information dominated their thought process and erased considerations of prior probability. In other words, subjects with no additional information (groups A1 and A2) made better predictions than subjects given useless additional information (groups C1 and C2).

#### Experimental Evidence: Summmary

Many experiments have been confirmed the existence of the representativeness heuristic in different scenarios. It is well established that humans tend to think that "sameness"---no matter how tenuous---is a strong predictor of "likely" and do not consider prior probabilities. Somewhat alarmingly, even useless information, where "sameness" does not dominate one way or other, is enough to erase the consideration of prior probabilities. As we saw above, it leads to absurd predictions.

### Countering the Heuristic

When making decisions like:
* Should we take this action (adopt a technology, make a change)?
* Should we prioritize X or Y?
* Which tech is best for Z objective?
* Given some data, what is the most likely explanation?

stop yourself and consider if you are substituting similarity for likelihood. If you are, then ask what are the various possible classes, some of which you may not even have considered initially. Then look for prior probabilities of the classes. You need not be very precise. Finally, assess what information you have, and how much does it change the prior probabilities. You may be surprised that you were blind to some highly likely classes.

Let me illustrate with a simplified but real example. A few months ago I spoke to the founder-CTO of an early stage startup. By early I mean they had a product idea and a sketch of functionality and architecture, but no code or development team yet. One question the founder had was about the choice of programming language: would NodeJS perform as well as Java at high loads as they acquired users, he asked? He wanted to make the "right" decision, optimizing cost and performance. Instead of debating the characteristics of programming languages (and inserting my own preference of language), I asked the founder to take a step back and reconsider the question.

Here is how I broke down the founder's situation. I am a startup and I know something about its future needs (this is the instance, *a*). I want to know what is the likelihood that my startup belongs to:

* Class *A*: the kind of startup where speed and cost efficiency of code is paramount
* Class *B*: the kind of startup where speed of feature development and rapid iteration is paramount
* Class *C*: some other kind

Let us consider the *prior probabilities*. A quick search for "startup success statistics" and reading articles from [Investopedia](https://www.investopedia.com/articles/personal-finance/040915/how-many-startups-fail-and-why.asp) and [Forbes](https://www.forbes.com/sites/neilpatel/2015/01/16/90-of-startups-will-fail-heres-what-you-need-to-know-about-the-10/?sh=16107e716679) shows that 90% of startups fail, and the causes of failure are: (a) being in the wrong market; (b) lack of customer and market research; (c) bar partnerships; (d) ineffective marketing; (e) not having industry expertise; (f) running out of money which further can be subdivided into (f1) not having enuogh sales/growth; (f2) inefficient operations. Only (f2) is the kind of startup described in class *A*.

From this we can ascertain that class *B* and *C* together account for more than 90% probability, and class *A* accounts for less than 10% probability. The numbers are approximate but the difference is so stark that we don't need to be too accurate.

Let's add information about *a* now: the startup was building a recruiting/jobs website. The kind of workloads would be front end website, some backend web services, a resume upload/retrieval data store and perhaps some automatic document scanning to extract text. Nothing screams "raw high performance" requirements from the programming language chosen. Given this information, startup *a* is much more likely to be one where they are rapidly developing features to find a product-market fit (*B*), or building effective marketing and sales channels (*C*) than one which has a good product-market fit and growth and just needs to keep costs low (*A*).

I advised the founder that they should not decide which programming language to use at this time. They should hire good talent and let *them* choose which programming language to use based on their skillset.

## Heuristic 2: Availability

When faced with problems of the form:

> Is class **A** more frequent or likely than class **B**?

we substitute it with the easier problem:

> How easily can I recall instances of **A** vs **B**?

Here, we assume that likely (equivalently: more frequently occurring) things are easier to recall. This heuristic is called Availability. The heuristic extends to:
* More likely things will turn up more frequently if we search in any specific knowledge base
* More likely things are easier to imagine

The way our brain works, some things are easier to recall than others and some things are easier to imagine than others, regardless of their actual frequency. Knowledge bases may have skew in which kinds of things they store and make available. For example, there are more blog articles and marketing literature about the successful application of a technology than failed ones, providing a skewed view of how applicable that technology is.

The heuristic of availability ignores the possibility that our ability to recall or search for instances of a class may not return representative data.

### Experimental Evidence

Subjects, all native English speakers, were given a small set of letters from the English alphabet and asked "do more words start with this given letter or do more words contain this letter in the third position?". Almost everyone judged that more words start with the given letters. In fact, the letters were chosen such that they occur more often in the third place. The effect can be explained by the observation that it is much easier to recall words that start with a given letter, than words that contain the letter in an arbitrary position.

Subjects heard a list of well-known personalities of male and female genders, and subsequently were asked to judge whether the list contained more names of men than of women. Different groups were presented with different lists. In some lists, the men were relatively more famous than women and in other lists the women were more famous than men. In each group, subjects erroneously judged that the class (gender) that had more famous names was also more frequent.

It is a common experience that subjective probability estimates of traffic accidents rise temporarily when one observes an accident by the side of the road.

### Countering the Heuristic

Lifelong experience has taught us that, in general, instances of large classes are recalled better and faster than instances of less frequent classes. So this heuristic serves a useful purpose. However, in technology, we often encounter situations that are novel to us or where we simply have not been exposed to the various classes equally. To make good decisions, we need to suspend this heuristic and look harder for objective data.

When making technology decisions of the form:
* What is the probability of outcome *A* happening (or not happening)?
* Is *A* more likely or frequent than *B*?
* What are the various possible outcomes, and their relative likelihood?

ask yourself if you are depending purely on your ability to recall or mentally "search" for instances of each class? If so, consider if you've been equally exposed to the various classes and capable of recalling them with equal ease? If not, you may have to stop yourself and do a more objective, mechanical evaluation.

Let me illustrate this with an observation I have had in technology.

Developers, especially those in startups, are usually quick to adopt new frameworks and programming languages over ones they are quite familiar with. Senior engineers and architects often say/feel: "it is time to redesign X completely from scratch". If asked, they will cite the strengths of the new framework/language/architecture and how it solves the problems they have with their existing tools. The availability heuristic is working in two ways here:

* It is easier to recall problems with current tools than their strengths, simply because one spends less time and effort on things the tool is excellent at and much time on things the tool is not so good at. New tools may solve the problems current tools have, but are they as good at what the current tools do well?
* If existing tools have problems that we found out the hard way, new tools may have their own non-obvious problems too. However, it is hard to imagine the ways new tools can fail since we haven't had deep experience with them. That does not mean the new tools won't have problems. We can and should invest time in finding out what those would be and have a plan to address them. Yet we often don't.

I am not saying that we should never adopt new tools. I am just pointing out that enthusiasm about new tools is often inflated and objective data gathering not done due to blind spots created by the availability heuristic, leading to inaccurate estimates of costs vs benefits and insufficient experimentation and testing.

## Heuristic 3: Anchoring and Adjusting

We often have to answer the question:

> What is the likely value of X?

which actually is the more complex question:

> What is range of values that X could have with N% probability?

where *N* is just making the subjective term "likely" more concrete. We substitute such questions with the simpler algorithm:

> Start with an initial guess number and adjust it up and down; stop when we feel we've adjusted enough.

There are two problems with this heuristic:

* Our initial guess or estimate is influenced strongly by factors that are not relevant to the quantity being estimated.
* We don't adjust enough; our feeling of "enough" kicks in earlier than it should.


### Experimental Evidence

Subjects were told to estimate various quantities, stated in percentages. Before being asked for their estimate, a number between 0 and 100 was determined by spinning a wheel of fortune in the subjects' presence. The subjects were first asked to indicate whether that number was higher or lower than the value of the quantity they were being asked to estimate, and then to create an estimate by moving upwards or downwards from the given number. Different groups were given different numbers for each quantity and these arbitrary numbers had a significant effect on estimates. For example, two groups were asked to estimate the percentage of African countries in the United Nations. They were given the numbers 10 and 65 from the wheel of fortune. Their average estimates were 25% and 45%, respectively. There was no reason for their estimates to be so different, except the starting number they were given. The subjects knew the starting number was effectively random but were unable to ignore it or compensate enough for it. (The real value is 90-10%% depending on whether some disputed territories are treated as countries or not.)

Two groups of high school students were asked to estimate, within 5 seconds, the value of a numerical expression written on the blackboard. One group was given the expression `8 × 7 × 6 × 5 × 4 × 3 × 2 × 1`. Another group was given `1 × 2 × 3 × 4 × 5 × 6 × 7 × 8`. To rapidly answer such questions, people may perform a few steps of computation and estimate the full product by extrapolation or adjustment. Because people typically adjust insufficiently, this procedure leads to underestimation. Secondly, the result of the first few steps depends on the initial numbers and leads to very different anchors. Indeed, the median estimate from the group given the numbers in ascending order was 512, and the median estimate from the group given the numbers in descending order was 2250, reflecting the impact of the first few numbers they encountered. Both severely underestimated: the real value is 40,320.

### Countering the Heuristic

If at all possible, don't do "quick estimates" for anything of consequence. Still, there are sitations where you simply don't have time to do a more thorough estimate. In such cases, just know that the estimate is quite likely to be *very* wrong and be humble and prepared to change your mind when someone presents a more thought through estimate.

Anytime you are going to estimate a numerical value, stop and ask yourself: what is the last number you saw or heard. It is almost certainly behaving as your anchor. You can't get rid of the anchor. If you've made an estimate already, starting again with a different anchor won't help---you will feel psychological pressure to defend your first estimate, especially if the new estimate is significantly different from your original one. The only way to get an independent assessment is to ask someone else who has not been exposed to your anchor.

And since we always have some anchor, it is best if the anchor is the *prior probability* of the class of things you are trying to make an estimate for. That is, before estimating the value of *x*, think of progressively more general classes *X1*, *X2*, ... it could belong to and see if you recall or can search for a reliable value for the class. Use that as your anchor before adjusting up or down using what information you have about *x*.

Anytime you are adjusting quantities upwards or downwards to get a subjective feeling of "good enough", ask yourself---what is the basis of the magnitude of the adjustment. If there is not an objective answer, know that you are more likely to be under-adjusting than over-adjusting.

Be wary when negotiating prices with vendors. Always do your own estimation first (you don't have to disclose it). Otherwise, the vendor's initial number will become your anchor over which you will haggle (downwards of course) and will adjust insufficiently.

# Closing remarks

There is much literature on the topic of [cognitive biases](https://en.wikipedia.org/wiki/List_of_cognitive_biases) and exhortations on avoiding them. There are a great many biases. It seems none of our mental faculties are free from problematic errors. While it is important to know about cognitive biases in general, and specific one in particular, to hopefully avoid and make better judgments, can anyone really remembers all of them and spot them when they are happening? There are just too many. Is there a more tractable way of improving decision making than carry a thick tome listing all our biases and neurotically thumbing them before every decision?

Heuristics are a better mental model for improving decisions. For one, they are fewer in number and easier to remember (I use the mnemonic **RAA** for **R**epresentativeness, **A**vailability, **A**nchoring and Adjusting). Secondly---and beware that this is just my speculation and I've not seen any peer reviewed evidence for this---it seems they can explain many biases. For e.g., the so-called [Survivorship Bias](https://en.wikipedia.org/wiki/Survivorship_bias) and [Frequency Illusion](https://en.wikipedia.org/wiki/Frequency_illusion) can be be explained by the Availability heuristic. [Agent detection](https://en.wikipedia.org/wiki/Agent_detection) can be explained by Representativeness.

I hope that knowing about these heuristics will help you to at least some extent, make better decisions. Or at least, take a healthily sceptical view of the solidity of your decisions.

# Further Reading

If you are interested in this topic and want to read more, here are a few sources:

* [Judgment under Uncertainty: Heuristics and Biases.](https://www.jstor.org/stable/1738360) by Daniel Kahneman and Amos Tversky, a landmark paper from 1973 which is the basis of the current article.
* [Thinking, Fast and Slow](https://www.amazon.com/Thinking-Fast-Slow-Daniel-Kahneman/dp/0374533555) by Daniel Kahneman. The concept of System 1 and System 2 is explained in this book from 2011.
* [Noise: A Flaw in Human Judgment](https://www.amazon.com/Noise-Human-Judgment-Daniel-Kahneman-ebook/dp/B08KSC11KQ/) by Daniel Kahneman, Olivier Sibony and Cass Sunstein. This book from 2021 goes beyond the topics explored in this article and talks about another source of errors in judgment, one not talked much about.
