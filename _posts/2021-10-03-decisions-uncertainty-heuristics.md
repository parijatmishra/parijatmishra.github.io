---
layout: post
title: Uncertainty, Mental Shortcuts, and Errors in Technology Decisions
---

If you are a technology leader, you know you make decisions, big or small, all the time. You also know that each decision carries some risk. Risks arise from several sources. We know how to mitigate many of the sources, but one of them is insidious: **uncertainty due to lack of information**. Behavioral phychologists and economists have spent decades researching how humans make decisions under uncertainty, and have found that a very wide variety of errors in decisions arise due to a few---just three, in fact---mental shortcuts humans use on a daily basis. These shortcuts, while useful in some circumstances, create systematic and even predictable errors. Sadly, we are largely unaware we are using them. In this article I will discuss what we know about how humans deal with uncertainty intuitively, the kinds of errors this can create, and how to identify and stop the mental shortcuts that can lead us to make errors. I hope this will help you increase the quality of your decisions and reduce risk, with only a little effort.

If you have seen instances where any of these shortcuts were being used, I would love to hear from you. I will update this article with your anecdotes if I find your stories clear and illustrative. Please do not share anything confidential, but do provide sufficient detail that a reader of this blog unfamiliar with your situation can understand the core idea.

## Risks and Uncertainty

For concreteness, let us imagine we are a startup, building a web application as part of our product. We need to make many decisions: what to build, how to build it, how to run it etc. The first thing we need to make good decisions is *knowledge and skills*: web technologies, experience with applying them, and running applications. The better our knowledge and skills, the higher the likelihood that the quality of our decisions will be good.

Knowledge and skills are not enough, though: we also need *information*. We need to know what features our web application should have. We need to know how heavily the application will be used to be able to run it at appropriate scale. We often encounter gaps in available information. Consider these scenarios:

- The startup has done user surveys and research to indicate there is interest in a product, but the sample sizes are small and in artificial conditions. It does not know *for sure* if enough people will pay for that product to make the investment in developing and running it viable.
- There are three client libraries for the database we have chosen: which one will satisfy our requirements best in terms of features and performance? We've read their documentation but the difference between them with respect to *our* feature and performance needs is not clear.
- We are evaluating two queuing systems. One is easy to get started with and operate but does not scale horizontally. The other scales horizontally but is complicated to get started with and operate---we will have to invest more time and effort to use it. We don't know how much load our queuing system will need to support in future.

A lack of information creates *uncertainty*, which in turn creates a *risk* that the option we choose will be incorrect. Let us define risk as *cost* of choosing the incorrect option times the *probability* of our choice being incorrect. The decision problem them becomes: which option has the lowest risk?

There are two ways to reduce risk:
1. Reduce the *cost* of making the wrong decision. There are several techniques. For example, the startup could build a so-called "minimum viable product" instead of a full-blown product to test the waters. We could build an abstraction layer on top of the queuing systems to allow us to switch the products in the future if we need to.
2. Reduce the *probability* of making the wrong decision. We can do this by getting more information. We could write proofs-of-concept programs using each of the database client libraries to find out whether they are easy to use for our foreseeable use cases and what their performance is like.

When making decisions, we should use both these methods to reduce the risk as much as we can. Let us assume our hypothetical startup has done so. What remains? Gap in information.

Sometimes, we simply can't get the information. For example, we could study the queuing systems all we like, but we lack information about the future load.

At other times, we *could* get more information but decide that the *value* of the information is not worth the *cost* of doing so. For example, our startup could choose to not build the product at all but wait for someone else to do so. If someone else succeeds, then we have the information we need: there are enough paying customers for our product. Now we can build the product ourselves with significantly reduced risk: this is the value of the additional information. The cost of the information is: losing the first mover advantage and a major chunk of the market, and losing the satisfaction of doing something innovative. We may decide it's not worth waiting.

There are two additional sources of risk.

1. Lack of knowledge and skills. If we don't have these, we won't even know what information to consider and what is uncertain.
2. Biased motivation. Sometimes, decision makers are not motivated to make objectively correct decisions. For example, an engineering manager may not tell the CTO that the chances of his project failing is 90% and should be scrapped because the organizational culture makes it difficult to do so.

Before making a decision, you should seek to eliminate these risks first, before focusing on informational risks. I am not going to discuss these risks further in this article.

## Uncertainty and Estimations

Let's go back to the decision of which queuing product to choose. Let's say we decided to reduce the cost of choosing the incorrect product by creating an abstraction layer in our code and making it easier to switch products in the future. Now we still have to buy, install and run the product. This does take time, effort and money that would be wasted if our prediction about the future load turns out to be wrong. Can we do something about it?

Yes. We can make *estimates* about the likelihood of different futures and choose the one most likely. Estimation is the act of judging probabilities of outcomes or values. Good estimates reduce uncertainty and therefore the probability of making an incorrect decision, just like information does.

You may philosophically disagree with the role of estimation in decision making. Your may be thinking: *Either I know something perfectly, or I don't know anything about it. How can I predict or estimate something I don't have information about? If I can't predict the future, I might as well rely on a coin toss---there's no point in trying to estimate.*

I put it to you that you are making estimates all the time. Estimates are often expressed as beliefs concerning the likelihood of uncertain events. You have made an estimate if you've ever stated something like:

- I think that...
- Chances are that...
- It is unlikely that...

Since you are doing it anyway, it pays to get better at making estimates. There are two parts to making good estimates. The first one is about increasing our knowledge and skills. The second is *behavioral*---actually applying the knowledge and skills. The focus of this article is on the second part: our *behavioral* tendency to use intuition to make estimates and how to combat it.

## Estimations and Heuristics

How does one make an estimate? What happens when we say "Chances are that..."? There is a lot of evidence that we employ two distinct modes of thinking: intuitive and quick (System 1) and systematic and plodding (System 2).
Let's talk about System 2 first. This method starts by creating a model of the problem space including causes, processes, and effects. Causes and processes can have parameters or variables associated with them (how far is that lion? how hungry?). Then we gather all reasonably available information (the lion could get to me in 30 seconds). For the information we don't have, we *ascertain a range of values* (the lion is sitting next to a carcass, so probably not very hungry). Then we do some calculations guided by the model (lion close but not very hungry). Finally express the result of the calculations as an estimate (chances are that the lion is not going to chase me). Often, we don't have the time to go through all these steps. When time is limited we *do not* simply dial down the precision of System 2 thinking to make it faster.

No. We use an entirely different process. The human brain evolved to estimate probabilities quickly with limited accuracy, rather than slowly and great accuracy. Our ancestors had to make a lot of decisions with imperfect information in limited time. Here are three "just so" stories that are plausible about decisions our ancestors would have had to make and how they'd make them:

* We are gathering food in the forest. We encounter a colorful berry that we haven't quite seen before. Food is scarce and we will be rewarded for getting more if the berry is edible. But if it is poisonous then we are likely to be punished. Is the berry safe to eat? It's a hard question. We substitute this question with the easier question: is this berry similar to my mental stereotype of berries known to be safe to eat?
* We are stalking animals to hunt in the prairie grass. We spot some movement in the grass. We need to decide the relative liklihood of a movement in the grass is due to a tiger (catastrophic) or gazelle (benign or beneficial). This is a hard question that requires knowing the relative frequencies of tiger and gazelle populations in the area of interest at the time of year. We substitute it with the easier question: how many gazelles and tigers can I recall seeing lately and what was the relative frequency?
* We are stalking animals to hunt in the prairie grass. It takes time to find and stalk them and we get only two chances a day on average. We've spotted some animals. We need to decide whether we can throw our spear far and accurately enough to hit an animal with >50% probability, or if should we try to get closer but risk spooking the animal. This is a hard question that would require us to keep track of the distances of our past throws, the conditions under which we executed them and what we know about the sensitivity of the animal. We substitute it with the easier question: what was the distance of my last successful throw, and am I feeling strong/weaker than that time?

Did the above stories sound very reasonable? Did you find it hard to imagine how else could our ancestors have made these decisions? If so, you and I can agree that the heuristics used there are very useful. While the above are made up stories, there is a lot of evidence that the substitution of complex tasks with specific simpler heuristics does occur.

**Our brain is constantly substituting complex estimation problems with simpler ones, i.e., using heuristics, without us even realizing it. We think the two problems are the same when they are not.**

We use these heuristics even when we do have the time to follow a more accurate process. We can't help it---the human brain is lazy and yet does a very good job of convincing us that it has done the work. Have you ever made a decision that felt "just right" but found it hard to explain why? Have you made a decision of major consequence based on "gut feel"? Have you mulled over a problem where suddenly something went "ting!" in your mind, and you arrived at the decision---and moreover, you got a feeling of satisfaction and convinction that the decision was right?

Unfortunately, these heuristics are not just somewhat less accurate ways of making estimates. Since they are answering a very different question from the original problem, they can lead to systematic errors and depending on the circumstances, severe ones. Combined with the fact we use them without even realizing we are doing so, we have a double whammy: we don't know that some of our estimation methods are error-prone and we don't know when we are using those methods.

The plan for the rest of the article is to describe three common heuristics and the issues with them.

## Heuristic 1: Representativeness

When faced with problems of the form:

> how likely is that an instance **a** belongs to class **A**

we substitute is with a simpler problem:

> how much does **a** resemble **A**?

If *a* is highly **representative** of *A*, it is assumed that *a* is highly **likely** to be an instance of *A*. Sounds logical? The problem is that *a* could potentially belong to several classes: *A*, *B*, *C*,... (Even if there are no explicit multiple classes, there are at least two: *A* and *not A*). The probability that *a* belongs to *A* depends on two factors:

1. How probable are the classes *A* and *not A*, in the first place? This is called *prior probability*. If we knew nothing about *a*, its probability of *belonging to A* is simply the *prior probability of A*.
2. Now, given information about *a*, how much does that information increase or decrease the probability of *a* belonging to *A*.

This is a fundamental concept in probability theory---conditional probability. However, the heuristic of representativeness ignores probability (1). When all the classses *a* could belong to are roughly equally numerous then the heuristic serves well. Otherwise, it does not. Now let us consider the errors it could lead to.

### Experimental Evidence

An experiment was conducted where subjects had to estimate the probability that an individual (*a*), picked from a population of engineers (*A*) and lawyers (*not A*), was actually an engineer (likelihood that *a* is an instance of *A*). The subjects were divided into several groups and given different information.

#### Predictions when information about *a* was not present

* Group A1: subjects were told nothing about the individual but were told that the poupulation consisted of 70 engineers and 30 lawyers. As expected, the group on average predicted that the individual was 70% likely to be an engineer.

* Group A2: subjects were told nothing about the individual but were told that the population consisted of 30 engineers and 70 lawyers. This group on average predicted that the individual was 30% likely to be an engineer.

Groups A1 and A2 used the prior probabilities correctly, as no other information was available.

#### Predictions when information about *a* was present and of predictive power

* Group B1: subjects were given the same population numbers as group A1 (70 engineers and 30 lawyers) and additionally were given a brief fictitious "personality description" of the individual. The description had very little information but would match the stereotype of an engineer or lawyer. For exampke, one description was "an introverted, analytical man". This group on average estimated the likelihood of the individual being an engineer or lawyer to be almost 100%, depending on what stereotype they were presented.

* Group B2: subjects were given the same population statistics as group A2 (30 engineers and 70 lawyers) and additionally were given a brief fictitious "personality description" of the individual, like group B1. They too ignored the population statistic and made predictions just like group B1, depending on what stereotype they were presented.

Arguably, "an introverted, analytical man" does match the stereotype of an engineer. That is to say, the instance *resembles* the class. But how much information does this description contain? Consider: are you sure *all* engineers are introverted and analytical? If not, there is a percentage of engineers who do not match the description. Consider: can lawyers be introverted and analytical? If so, the description could match a portion of lawyers. Consider: will all introverted and analytical people seek engineering as an occupation? There are other factors involved: is there a good and afforable engineering school they have access to? Were any of their parents or influential parental figures lawyers? If they were analytical, were they better in the school debate team or physics club? Did their school have luminary alumnis who were engineers or lawyers? What about other unknown personality characteristics? Thinking of these factors, would you say the conclusion that the description predicts an engineer is a slam-dunk?

The description could have tweaked the prior probabilities, but not by a lot. Yet, given just a smidgen of information of dubious value, both groups B1 and B2 ignored the prior probabilities entirely.

#### Predictions when information about *a* was present and inconclusive

* Group C1: subjects were given the same population statistics as group A1 (70 engineers and 30 lawyers) and also a personality description. However, the descriptions were deliberately designed not to match any occupational stereotypes and more generally, not give any clues as to occupation. For example, a description could be "Dick is a 30 year old man. He is married with no children. A man of high ability and motivation, he promises to be quite successful in his field. He is well liked by his colleagues." This group on average predicted that the individual is equally likely to be an engineer or lawyer.

* Group C2: subjects were given the same population statistics as group A2 (30 engineers and 70 lawyers) and personality descriptions like group C1. This group also on average made the same predictions as group C1: the individual is equally likely to be an engineer or lawyer.

In this case, the groups got inconclusive information. The information by itself does not predict anything. They should have disregarded the information and just used prior probabilities like group A1 and A2. However, the inconclusive information dominated their thought process. In other words, subjects with no additional information (groups A1 and A2) made better predictions than subjects given useless information (groups C1 and C2).

#### Experimental Evidence: Summmary

The experiment has been replicated in many different ways. It is well established that humans tend to think that "sameness"---no matter how tenuous---is a strong predictor of "likely" and do not consider prior probabilities. Somewhat alarmingly, even useless information, where "sameness" does not dominate one way or other, is enough to erase the consideration of prior probabilities. As we saw above, it leads to absurd predictions.

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

The way our brain works, some things are easier to recall than others unrelated to frequency regardless of their actual frequency. Some things are easier to imagine than others. Knowledge bases may have skew in which kinds of things they store and make available.

### Experimental Evidence

Subjects, all native English speakers, were given a small set of letters from the English alphabet and asked "do more words start with this given letter or do more words contain this letter in the third position?". Almost everyone judged that more words start with the given letters. In fact, the letters were chosen such that they occur more often in the third place. The effect can be explained by the observation that it is much easier to recall words that start with a given letter, than words that contain the letter in an arbitrary position.

Subjects heard a list of well-known personalities of male and female genders, and subsequently were asked to judge whether the list contained more names of men than of women. Different groups were presented with different lists. In some lists, the men were relatively more famous than women and in other lists the women were more famous than men. In each group, subjects erroneously judged that the class (gender) that had more famous names was also more frequent.

It is a common experience that subjective probability estimates of traffic accidents rise temporarily when one observes an accident by the side of the road.

### Countering the Heuristic

In all the above, and more, observations, subjects confused ease of recollection with actual frequency or lilelihood, and moreover were quite confident that their judgment was accurate. Lifelong experience has taught us that, in general, instances of large classes are recalled better and faster than instances of less frequent classes. So this heuristic serves a useful purpose. However, in technology, we often encounter situations that are novel to us or where we simply have not been exposed to the various classes equally. To make objectively good decisions, we need to suspend this heuristic. This heuristic is subtly different from Representativeness: it does not use *similarity* of an instance to a class, but only examines at the relative frequency of classes.

When making technology decisions of the form:
* What is the probability of outcome *A* happening (or not happening)?
* Is *A* more likely or frequent than *B*?
* What are the various possible outcomes, and their relative likelihood?

ask yourself if you are depending purely on your ability to recall or mentally "search" for instances of each class? If so, consider if you've been equally exposed to the various classes and capable of recalling them with equal ease? If not, you may have to stop yourself and do a more objective, mechanical evaluation.

Let me illustrate this with a few common observations I have had in technology.

Developers, especially those in startups, are usually quick to adopt new frameworks and programming languages over ones they are quite familiar with. Senior engineers and architects often say/feel: "it is time to redesign X completely from scratch". If asked, they will cite the strengths of the new framework/language/architecture and how it solves the problems they have with their existing tools. The availability heuristic is working in two ways here:

* It is easier to recall problems with current tools than their strengths, simply because one spends less time and effort on things the tool is excellent at and much time on things the tools is not so good at. New tools may solve the problems current tools have, but are they as good at what the current tools do well?
* If existing tools have problems that we found out the hard way, new tools may have their own non-obvious problems too. However, it is hard to imagine the ways new tools can fail since we haven't had deep experience with them. That does not mean the new tools won't have problems. We can and should invest time in finding out what those would be and have a plan to address them. Yet we often don't.

I am not saying that we should never adopt new tools. I am just pointing out that enthusiasm about new tools is often inflated and objective data gathering not done due to blind spots created by the availability heuristic, leading to insufficient clarity about costs and benefits.

## Heuristic 3: Anchoring and Adjusting

When faced with questions of the form:

> What is the likely value of X?

which actually is the more complex question:

> What is range of values of X that I am N% confident about?

where *N* is the quantification of "likely", which is subjective. We substitute such questions with the simpler question:

> Start with an initial guess number and adjust it up and down until we feel we've adjusted enough.

There are two problems with this heuristic:

* Our initial guess or estimate is influenced strongly by factors that are not relevant to the quantity being estimated
* We don't adjust enough


### Experimental Evidence

Subjects were asked to estiamte various quantities, stated in percentages. Before being asked for their estimate, a number between 0 and 100 was determined by spinning a wheel of fortune in the subjects' presence. The subjects were first asked to indicate whether that number was higher or lower than the value of the quantity they were being asked to estimate, and then to create an estimate by moving upwards or downwards from the given number. Different groups were given different numbers for each quantity and these arbitrary numbers had a significant effect on estimates. For example, two groups were asked to estimate the percentage of African countries in the United Nations. They were given the numbers 10 and 65 from the wheel of fortune. Their estimates were 25% and 45%, respectively.

Two groups of high school students were asked to estimate, within 5 seconds, the value of a numerical expression written on the blackboard. One group was given the expression `8 × 7 × 6 × 5 × 4 × 3 × 2 × 1`. Another group was given `1 × 2 × 3 × 4 × 5 × 6 × 7 × 8 × 9`. To rapidly answer such questions, people may perform a few steps of computation and estimate the full product by extrapolation or adjustment. Because people typically adjust insufficiently, this procedure leads to underestimation. Secondly, the result of the first few steps depends on the initial numbers and leads to very different anchors. Indeed, the median estimate from the group given the numbers in ascending order was 512, and the median estimate from the group given the numbers in descending order was 2250. The real value is 40,320.

### Countering the Heuristic

Anytime you are going to estimate a numerical value, stop and ask yourself: what is the last number you saw or heard. It is almost certainly behaving as your anchor. You can't get rid of the anchor. If you've made an estimate already, starting again with a different anchor won't help---you will be compelled to defend your first estimate. The only way to get an independent assessment is to ask someone else who has a different anchor.

Anytime you are adjusting quantities upwards or downwards to get a subjective feeling of "good enough", ask yourself---what is the basis of the magnitude of the adjustment. If there is not an objective answer, know that you are likely not adjusting enough.

Be wary when negotiating prices with vendors. Always do your own estimation first (you don't have to disclose it). Otherwise, the vendor's initial number will become your anchor over which you will haggle (downwards of course) and will adjust insufficiently.

In general, the only was to counter this heuristic is to not make intuitive estimates but use mechanical and scientifically sound procedures. If you don't have the time for that, know that your estimate is highly likely to be off the mark and don't be too proud to look for better numbers when you do have time.

# Closing remarks

There is much literature on the topic of [cognitive biases](https://en.wikipedia.org/wiki/List_of_cognitive_biases) and exhortations on avoiding them. There are a great many biases. It seems none of our mental faculties are free from problematic errors. While it is important to know about cognitive biases in general, and specific one in particular, to hopefully avoid and make better judgments, can anyone really remembers all of them and spot them when they are happening? There are just too many. Is there a more tractable way of improving decision making than carry a thick tome listing all our biases and neurotically thumbing them before every decision?

Heuristics are a better mental model for improving decisions. For one, they are fewer in number and easier to remember (I use the mnemonic **RAA** for **R**epresentativeness, **A**vailability, **A**nchoring and Adjusting). Secondly---and beware that this is just my speculation and I've not seen any peer reviewed evidence for this---it seems they can explain many biases. For e.g., the so-called [Survivorship Bias](https://en.wikipedia.org/wiki/Survivorship_bias) and [Frequency Illusion](https://en.wikipedia.org/wiki/Frequency_illusion) can be be explained by the Availability heuristic. [Agent detection](https://en.wikipedia.org/wiki/Agent_detection) can be explained by Representativeness.

I hope that knowing about these heuristics will help you to at least some extent, make better decisions. Or at least, take a healthily sceptical view of the solidity of your decisions.

# Further Reading

If you are interested in this topic and want to read more, here are a few sources:

* [Judgment under Uncertainty: Heuristics and Biases.](https://www.jstor.org/stable/1738360) by Daniel Kahneman and Amos Tversky, a landmark paper from 1973 which is the basis of the current article.
* [Thinking, Fast and Slow](https://www.amazon.com/Thinking-Fast-Slow-Daniel-Kahneman/dp/0374533555) by Daniel Kahneman. The concept of System 1 and System 2 is explained in this book from 2011.
* [Noise: A Flaw in Human Judgment](https://www.amazon.com/Noise-Human-Judgment-Daniel-Kahneman-ebook/dp/B08KSC11KQ/) by Daniel Kahneman, Olivier Sibony and Cass Sunstein. This book from 2021 goes beyond the topics explored in this article and talks about another source of errors in judgment, one not talked much about.
