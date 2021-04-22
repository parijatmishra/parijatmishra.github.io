---
layout: post
title: On Using Metrics Judiciously
---

## Introduction

The intended audience for this article is the business or technology leader who
is considering using quantitative metrics to measure and improve the performance
of their organization, groups, teams or individuals. This article is not about
using technical metrics to improve technology systems (e.g., using metrics like
request throughput and latency, or CPU and RAM utilisation to monitor system or
application performance).

By "metrics", I do not mean raw data; I refer to things that are
quantitative--either cardinal or ordinal--that are used to measure the
performance of something. One man's metric is another man's data--it depends on
the context.  What is important is how the quantitative data is intended to be
used.

To put it in conrete terms: imagine you have a number of engineering teams (some
infra and ops oriented, some application development oriented).  They all work
off a work tracking system, like Jira.  The Jira tickets themselves and
associated metadata about them are just data.  If you now take some data like
"tickets cloed per week" or "average duration tickets are open" and use them to
*measure* something, I call that a "metric".

## Context

In a [previous blog article], I wrote how great CTOs use metrics judiciously to
measure the health of a technology function and to drive change. On re-reading,
I believe while I did not say anything incorrect *per se*, I understated the
potential problems with using metrics, and made it look like that it is easy to
get them right.

An analogy for what I wrote would be "*If* you enter this forest, you *might be*
bitten by a *mosquito*". I should have written something more along the lines of
"*When* you enter this forest, you *will be* attacked by *several deadly
animals*." See the difference?

Aside: I had this realization after reading the book [*The Delicate Art of
Bureaucracy*][schwartz-bureaucracy] by one of my favorite authors, Mark
Schwartz, where he devoted an entire chapter to *The Bureacracies of Metrics*. I
highly recommend picking up the book if you are a technology or business leader
in an organization that is growing large, or if you just landed in a large one.
Schwartz is a veteran IT leader, and though he describes himself as an
"inveterate purveyor of lucubratory prose" I don't find his prose lucubratory at
all. I find it humorous, light, yet insightful. *J'accuse* Mark, *j'accuse*!

So, with apologies for what I wrote earlier, I want to elaborate upon metrics in
this article, mostly to educate myself, and partly in the hope it will be
useful.  In the rest of the article, I will try to:

- **Warm you** up with an understanding of common motivations behind
  introducing metrics for performance management;
- **Warn you** about some myths about quantitative metrics so we don't end
  up doing the wrong things for the right reasons;
- **Alarm you** about the lasting damage incorrectly applied metrics could
  do so we are careful when using them next time;
- **Calm you** by examining the (few) scenarios where we will really need metrics;
- **Arm you** with a checklist of questions to ask and check if there are better
  ways of achieving our objectives, before reaching out for a metric.

## Why Use Metrics?

TODO:
- Motivations
  - DONE: Complexity
  - DONE: Low-trust of human judgment
  - Overcoming Human biases
  - Information sharing
- Myths
  - What gets measured, gets managed
  - What gets meaured, gets done
  - If you can not measure it, you can not improve it
- Core Problems

Metrrics (and associated targets) are often created without a discussion of why
a metric had to be created in the first place.  In this section I will explore a
few common reasons organisations and leaders look to quantitative metrics.  If
you know the likely motive, you will be better positioned to ask if the metric
is going to meet the underlying motivation.

### Taming Complexity

Consider these situations: (a) a new external business or technology leader has
just landed in a large organization, with many functions, product, geographies,
or market segments; (b) an internal leader leading one function is now leading a
larger team of many functions; (c) an internal leader leading a function in a
particular geography or market segment has now taken over a larger geography or
multiple market segments.

The organization will have multiple functions, geographies or market segments.
For convenience, let's call them "business units". The leaders challenge is that
each business unit creates different kinds of value, and has different inputs,
outputs and processes.  Sometimes business units nominally doing the same
function in different geographies will work differently. The leader is faced
with a lot of complexity. Understanding the unique nature of each business unit
is hard work and consumes time. How is the leader going to measure and improve
the performance of these units? Each unit seems to have its own language. Even
units which seem to have the same mission and function--e.g., different
application development teams--seem to be speaking in tongues, when the
beleaguered leader tries to fathom what they do.

The leader may decide that, at least for similar looking groups or teams,
standardized metrics of performance can make their job easier.  The leader finds
or invents lowest common denominator inputs, activities and outputs across them.
E.g., for application development teams: number of user stories completed in a
time period (or more sophisticatedly user *story points* per period, aka sprint
velocity). Sometimes the metrics become quite abstract in a valiant effort to
measure very different activities with a standardized metric. E.g.,
"value/person/month" where productivity is usually some notional dollar-value,
laboriously calculated with shaky assumptions.

*(I speak from personal experience. I tried to do this last year. It was an
ignominious failure. The only thing I am proud of was that I acknowledged the
hare-brained thing for what it was, eventually. I apologise to my team members
who bemusedly tried to cooperate with me.)*

Standardization of metrics almost always loses valuable local context and
encourages measuring everyone with the same yardstick when their circumstances
may be different.  Even when leaders acknowledge that two team are dealing with
somewhat different situations, human beings being human, there is a great
temptation to start a conversation with "why is your metric X much lower than
that other team?" The team now needs to explain that, well, things are
different. Sometimes a team may not even know about that other team's
circumstances, which makes the explanation more difficult and tempts the team to
clutch at straws. At best this wastes time re-explaining something that is
already known; at worst, people give up trying to explain and meet the yardstick
via *gaming* the metric, which I will elaborate on later.

### Substituting Human Judgment

In most orgnisations, there are some functions whose value few people
understand. This can happen, for instance, when the functions are needed for
external and not internal needs (e.g. the "Risk and Compliance" functions in
regulated organisations); or when the functions are highly specialiazed (e.g.
"Legal"). When most business stakeholders do not understand what a function does
and how it does it, and trust between groups is low such that they are blaming
others when they are not achieving their objectives, calls to measure the
functions' contributions increase. The person accountable for a function may opt
for using simple quantitative metrics to expose its contributions or
performance, over the exhausting alternative of educating others on the value of
the functio.

This may not work as I described in the section "Money Talks!" in my [previous
blog article]. In such cases, metrics are needed. Your only recourse is to not
make them onerous on your team and distract them from creating value.

It is preferable that leaders and stakeholders either understand the function,
or have reliable and trustworthy leaders to lead that function so they don't
have to.  It is even better to have a culture where if function A has a problem
with function B, the team members of A feel it necessary and normal to have a
conversation with the team B quickly, try to reconcile their objectives,
discover if there are gaps in understanding, try to resolve them by increasing
understanding if possible, and bring any irreconciliable differences to their
leaders. Sometimes, dependent teams have goals that are mis-aligned, leading to
friction. Mis-alignment in self-determined processes can be fixed by the teams
themselves if their goals are aligned (or they can seek advice on the right
compromise from leaders). Mis-alignment in *goals* is always the team's common
leader's problem and responsibility (their job is to design an organisation with
functions or business units that are workinng harmoniously, after all).  The
common leader should not allow themselves to get away with using metrics to
paper over such problems.

In some cases, there are functions whose goals, or at least KPIs, are
*deliberately* not aligned. This can be necessary for implementing
checks-and-balances.  In such situations, it is necessary to explain the
reasoning behind this repeatedly and constantly over implementing superficial
performance metrics to demonstrate that the dependee function is satisfying the
goals of the dependent function. **TODO**

**TODO: personal anecdote -- SA goals vs Sales goals**

### Metrics to Offset Human Biases and Blind Spots


### TODO: Metrics vs Data

- Data: exploratory
- Metrics: information
- Metrics: diagnostic
- Metrics: control

## Review: Myths about Metrics


A quote [attributed to Lord
Kelvin](https://thefutureorganization.com/lord-kelvin-on-measurement/) from 1883
goes like this:

> I often say that when you can measure what you are speaking about, and express
> it in numbers, you know something about it; but when you cannot measure it,
> when you cannot express it in numbers, your knowledge is of a meagre and
> unsatisfactory kind; it may be the beginning of knowledge, but you have
> scarcely in your thoughts advanced to the state of Science, whatever the
> matter may be.

Lord Kelvin was writing about *Electrical Units of Measurement*. He did not say
there is *no* knowledge without numbers, but that numerical measurement brings
*more* knowledge. Over the centuries, the idea got repeated and embedded into
things that were not electrical in nature.  Apparently, people were doing this a
lot because in 1956, V.F. Ridgway wrote [an article in Administrative Science
Quarterly][ridgway-1]:

> There is today a strong tendency to state numerically as many as possible of
> the variables with which management must deal.... This has led to the
> development of quantitative performance measurements for all levels within
> organizations,...

This should be good, right? If more people are using quantitative measurements
for performance, as Lord Kelvin said, their knowledge should no longer be meagre
and unsatisfactory and should be approaching Science. For some reason, Ridgway
was not happy and went on to write:

> Quantitative measures of performance are tools,... Judicious use of a tool
> requires awareness of possible side effects and reactions.  Otherwise,
> indiscriminate use may result in side effects and reactions outweighing the
> benefits...The cure is sometimes worse than the disease.

As you can see, the author was not positive about quantitative measurements.  In
fact, the title of the article was: *Dysfunctional Consequences of Performance
Measurements*. I wonder if he did well in maths in school.

Let's look elsewhere.

An oft quoted saying is "[only] what gets measured, gets managed." The saying is
sometimes attributed to [Peter Drucker], the great management guru ([e.g.
1][drucker-attrib-1], [e.g. 2][drucker-attrib-2]). Another variant of the saying
is "What Gets Measured Gets Done", [attributed to Tom Peters][tom-peters-1986]
from 1986.

If Drucker said this, it must be wise and right, right?  Some people are not
happy and insist that there's no evidence that Drucker actually ever said this
([e.g.][drucker-noattrib]). And some people are not happy on general principle.
For e.g., the journalist [Simon Caulkin][caulkin-1], referring to Ridgway's
article and other sources, wrote:

> If there's one management platitude that should have been throttled at birth,
> it's 'what gets measured gets managed'. It's not that it's not true---it is---
> but it is **often misunderstood, with disastrous consequences.**

That's a bit extreme, don't you think?  I mean, maybe Drucker did not say this,
but that doesn't make the saying wrong.  Sadly, Simon has more to say:

> The full proposition is: 'What gets measured gets managed - even when it's
> pointless to measure and manage it, and even if it harms the purpose of the
> organisation to do so.'

At this point, we should be skeptical. As Lord Kelvin said, being able to
express some quantity numerically adds to our knowledge. So how can measuring
something be pointless? Even if we assume that some numbers could be pointless,
how could their existence harm the purpose of the organization?

(E.g.: We could find the tensile strengths of a specimen of my cranial hair,
assuming you could find said speciment.  It would be a number.  If someone could
be bothered to measure it, it would be very scientific, because I assume some
scientific instruments would be required to do so.  But it may not be very
pointy---I mean, it would be pointless. (Is "pointy" an antonym of pointless?))

How can using numbers have "side effects and reactions"?  Perhaps it is not the
numbers themselves but how we used them in the past?  Surely we are wiser now.
Surely, today, we all have a good handle on the "possible side effects and
reactions" of using metrics, right? We would not be using them indiscriminately,
would we? We must have learnt something between 1956 and 2021. After all, we
have DevOps now!

And yet the warnings keep coming with depressing regularity. [Jerry Z.
Muller][muller-1] wrote an entire book in 2018 titled [*The Tyranny of
Metrics*][tyranny-metrics]. [Mark Schwartz][schwartz], an IT leader and author
of several books on technology leadership, devoted an entire chapter titled
*Bureaucracies of Metrics* in his book [The Delicate Art of
Bureaucracy][schwartz-bureaucracy]. These are just two of many examples of
warnings about using metrics. I stopped looking for more, because I got, well,
depressed.

### The Curious Case of The Metric Replacing The Strategy

Are the warnings merited?  How bad can things get, even if it were possible to
somehow misuse our humble servant, the number?  Perhaps the authors are
over-reacting.

In an article from 2019 in the Harvard Business Review, titled [*Don't Let
Metrics Undermine Your Business*][hbr-2019-1], the authors describe an extreme
example of the consequences of surrogation at the bank [Wells
Fargo][wells-fargo-1]. This is my summary of what happened: Wells Fargo had and
continues to have a *strategy* of building long-term retail banking
relationships with customers. They already had a *metric* for cross-selling
activities. Wells-Fargo decided to *align* the *metric* with the *strategy*.
Unfortunately, employees started acting, at a large scale and over a long period
of time, as if cross-selling *was* the strategy. To meet this non-existent
"strategic goal", employees *fraudulently* opened millions of deposit and credit
accounts without customer consent. For some reason, managers and senior leaders
did not detect that the increasing number of accounts from so-called
"cross-selling" were created in a fraudulent manner. Initially, when some
customer complained about fees and charges related to accounts they had never
consented to creating, or unexpected credit cards and mortgages they did not
sign up to, the incidents were blamed on a few, over-zealous employees; no one
thought to check whether this was a wide-spread occurrence. Since the
misbehavior came to light, Wells Fargo has had to spend billions on reimbursing
customers, paying damages and fines, and for litigation. Regulators stopped them
from growing their assets for a while (meaning, Wells Fargo could not get new
business, even legitimately, while they continued to pay damages and fines).
And, besides losing money, the bank has also lost customer trust: the issue came
to light in 2016, and the bank is reporting a fall in new customer sign-ups even
in 2021. The damage to the bank has been extensive and persistent.

The authors examine the underlying causes and conclude that the root cause was a
pervasive culture of measuring performance by measurement of metrics. Further,
they caution:

> The mental tendency to replace strategy with metrics can destroy company
> value.

Hmmm.  Perhaps this is an isolated case?  No. Muller and Schwartz, let alone
legions on the internet, give many other examples of metrics replacing the
actual goal, as far as people's behavior is concerned.  Okay, maybe this is not
isolated, and it could happen to you.  You will not let metrics replace
strategy. Problem solved.

Are we done? There aren't any other problems with using metrics, are there?

## The Perils of Metrics


3.1 Information Distortion

- Easily measurable even it is not valuable
- Simple measures for complex problems
- Measuring inputs rather than outcomes
- Inappropriate standardization
- Over-simplifcation
    - Incorrect conclusions

3.2 Gaming

Goodheart's law

- Creaming
- Omission of data
- Lowering standards
- Gaming, cheating

3.3 Orgnisational Cost

- Goal displacement
- Short-termism
- Cost in time, effort, people
- Diminishing returns
- Knee-jerk reactions

3.3 Human Cost

- Rule cascades due to bad actors - impact on good performers and rule followers
- Rewarding luck
- Discouraging risk-taking
- Discouraging innovation
- Discouraging co-operating, teamwork
- Anti "purpose" - degrading quality of work


## Benefits of Metrics

- Illustrative: Amazon, Bezos: Website load time, Advertisements
- Diagnostic: Provonost, ???? personal experience?
- TOOD: look at amazon builder's library

WIP: How to Measure Anything

- Concept of measurement -- approximation -- is this useful?

"Although this may seem a paradox, all exact science is based on the idea of
approximation. If a man tells you he knows a thing exactly, then you can be safe
in inferring that you are speaking to an inexact man." -- Bertrand Russell,
British mathematician and philosopher.

## How to Use Metrics

Use metrics to augment experience and knowledge based judgement, not replace it.
Don't use metrics to avoid understanding the nature of something.


Then (Muller):
- What kind of information? Inanimate or human?
- How useful is it?
- Are more metrics more useful?
- Are there alternative metrics? Is a new standardized metric needed? What would be the cost of *not* using the standardized metric?
- What is the cost of collecting it? Is it higher than the benefit (useful)?
- Who will interpret (what is the purpose)? The purpose is always that someone will use this metric to make a decision
    - Are they capable of interpreting the metric?
    - Is this a performance and pay related metric and should it be used in this way?
- If you are being asked for a metric
    - Why?
    - Who developed the metric and how?
    - Will this be gamed?
    - Do people know why?
    - Is it aligned to people's sense of mission/professional ethic?

## Conclusion



[previous blog article]: {% post_url 2021-03-30-what-i-learnt-from-ctos-business %}
[schwartz]: https://www.amazon.com/Mark-Schwartz/e/B01AHGEC2I
[schwartz-bureaucracy]: https://www.amazon.com/gp/product/B086XM4WCK/
[muller-1]: https://history.catholic.edu/faculty-and-research/faculty-profiles/muller-jerry/index.html
[tyranny-metrics]: https://www.amazon.com/Tyranny-Metrics-Jerry-Z-Muller/dp/0691191913/
[Peter Drucker]: https://en.wikipedia.org/wiki/Peter_Drucker
[drucker-attrib-1]: https://www.resultsjunkies.com/revisiting-drucker-what-gets-measured-gets-managed/
[drucker-attrib-2]: https://link.springer.com/chapter/10.1057/9781137375469_7
[drucker-noattrib]: https://athinkingperson.com/2012/12/02/who-said-what-gets-measured-gets-managed/
[tom-peters-1986]: https://tompeters.com/columns/what-gets-measured-gets-done/
[caulkin-1]: https://www.theguardian.com/business/2008/feb/10/businesscomment1
[ridgway-1]: https://www.jstor.org/stable/2390989?origin=crossref&seq=1
[wells-fargo-1]: https://en.wikipedia.org/wiki/Wells_Fargo_account_fraud_scandal
[hbr-2019-1]: https://hbr.org/2019/09/dont-let-metrics-undermine-your-business

[measure-book]: https://www.amazon.com/Measure-What-Matters-Google-Foundation-ebook/dp/B078FZ9SYB/

[selinger-1]: https://www.entrepreneur.com/article/237326
