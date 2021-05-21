---
layout: post
title: On Using Metrics Judiciously
---

The intended audience for this article is the business or technology leader who
is considering using quantitative metrics to measure and improve the performance
of their individuals or groups of individuals. Quantitative metrics are powerful
tools but, when applied to human work, can easily cause lasting and deep damage.
This article's purpose is to help the reader use metrics usefully, and be able
to identify and avoid their pitfalls.

In a [previous blog article], I wrote how great CTOs use metrics judiciously to
measure the health of a technology function and to drive change. On re-reading,
I believe while I did not say anything incorrect *per se*, I understated the
potential problems with using metrics, and made it look like that it is easy to
get them right. An analogy for what I wrote would be "If you enter this forest,
you **might be** bitten by a **mosquito**". I should have written something more
along the lines of "If you enter this forest, you **will be** attacked by
**several deadly animals**." See the difference?

There are powerful and seductive calls to use metrics more widely and deeply.
Proponents of metrics highlight successful applications. Failures, if discussed
at all, are attributed to generic "mis-management" or a failure of execution.
What is not highlighted are there are more ways to use metrics incorrectly than
productively. While there are cautionary tales and examples of metrics gone
amok, they conclude with "don't use metrics this way", or "just be careful".
*Systematic* guidance on avoiding the pitfalls of metrics is sparse. 

This article tries to synthesize information from many sources and present them
in a logical structure. I will be providing some anecdotes from personal
experience; these opinions are entirely mine and do not reflect the opinion of
my employer, past or present.

To be clear: I *won't be* talking about using metrics to monitor the health or
performance of *technology systems* (e.g., measuring CPU utilization, request
latency etc.). Instead, I am talking about things that purport to measure the
performance of humans; i.e. things like sprint velocity, ticket resolution time,
Net Promoter Score (NPS), number and size of sales made, etc.

I will be using the term "group" very broadly to refer to all kinds of
organizational units: departments, specialist functions, cross-functional teams,
etc. I will also use the terms "accuracy" and "precision" distinctly, as
described [here][accuracy-good] (the [Wikipedia definition][accuracy-wiki] is
useless).

**Aside**: I was inspired to write this article after reading the books [*The
Delicate Art of Bureaucracy*][schwartz-bureaucracy] by [Mark Schwartz][schwartz]
and [*The Tyranny of Metrics*][tyranny-metrics] by [Jerry Muller][muller-1].
While I draw from these sources, all mistakes are mine.

## Why Use Metrics?

Metrics (and associated targets or goals) are often created without a discussion
of why a metric had to be created in the first place.  In this section I will
explore a few common reasons organizations and leaders look to implementing
quantitative metrics.  If you know the likely motive, you will be better
positioned to ask if the metric is going to meet the underlying motivation.

Destructive Motives          | Productive Motives
-------------------          | ------------------
1. To Appear Smart           | 6. To Motivate Change
2. To Wish Complexity Away   | 7. To Discover
3. To Replace Human Judgment | 
4. To Reward and Punish      | 
5. To Improve Focus          | 

### 1. Destructive Motive: To Appear Smart (by Copying Smart People)

Many business and management consultants advise us to use metrics. Some pieces
of advice have become dictums. They seem to provide simple, absolute guidance on
how to improve things and get things done. However, these adages are not what
they seem: they are often incomplete statements of reality or downright
misunderstood.  It is not wise to adopt them without understanding their full
implications.  Let's look at a few of the saying floating around.

**"If you can't measure it, you can't improve it."**

The above saying is [attributed to Lord Kelvin][kelvin-wrong]. Perhaps
mis-attributed. I can't find the source for this. More reliably, it seems what
Lord Kelvin *actually* wrote was:

> I often say that when you can measure what you are speaking about, and express
> it in numbers, you know something about it; but when you cannot measure it,
> when you cannot express it in numbers, your knowledge is of a meagre and
> unsatisfactory kind; it may be the beginning of knowledge, but you have
> scarcely in your thoughts advanced to the state of Science, whatever the
> matter may be.
> 
> --- Lord Kelvin, [PLA, vol. 1, "Electrical Units of
> Measurement"][kelvin-right]

Note that Kelvin did not say there is *no* knowledge without numbers, but that
numerical measurement brings *more* knowledge. He was also talking about
physical quantities. Somehow, this saying has been extrapolated to support the
idea that systems of human work must be measured numerically to improve their
performance.

**"What gets measured, gets managed."**

The above saying is sometimes attributed to [Peter Drucker], the great
management guru ([e.g. 1][drucker-attrib-1], [e.g. 2][drucker-attrib-2]). Some
people say there's no evidence that Drucker actually ever said this
([e.g.][drucker-noattrib]). And some people are not sure Drucker would agree
with this statement. For example, the journalist [Simon Caulkin][caulkin-1]
wrote:

> If there's one management platitude that should have been throttled at birth,
> it's 'what gets measured gets managed'. It's not that it's not true---it is---
> but it is **often misunderstood, with disastrous consequences.**

> The full proposition is: 'What gets measured gets managed - even when it's
> pointless to measure and manage it, and even if it harms the purpose of the
> organisation to do so.'

**"What gets measured, gets done."**

This is [attributed to Tom Peters][tom-peters-1986] from 1986 and unlike the
previous two quotes, the source of this seems reliable, coming as it does from
the author's own website. Like the previous two quotes, it can be criticized
that it is an exaggeration and can be interpreted as "*only* what gets measured
gets done, and therefore things that are not measured, even if they are
important, tend not to get done." This adage is a self-fulfilling prophecy.

As you can see, some of these sayings, supposedly by very smart people, are not
what they seem to be, and for others, there are reasons to doubt their
completeness. Don't use metrics just because someone said so.

### 2. Destructive Motive: To Wish Complexity Away

When an organization becomes complex, leaders create metrics to make measuring
and comparing the performance of multiple groups easier, in a standardized and
objective way.

Consider these situations:

  1. A new external leader has just joined a large organization, with many
     functions, products, geographies, and/or market segments;
  2. An internal leader leading one group has been promoted to lead a larger
     group consisting of multiple functions or geographies.
  3. The leader is tasked to improve the performance of the collection of
     groups.

The leader's challenge is that each group creates different kinds of value, and
has different inputs, outputs and processes.  Sometimes groups that are doing
the same function in different geographies work quite differently. Even
co-located groups which seem to have the same mission and function (e.g.,
different application development teams) seem to be speaking in different
languages, when the beleaguered leader tries to fathom out what they do and if
they are doing those things well. How is the leader going to measure and improve
the performance of many very different groups? The leader can treat each of them
uniquely and try to understand their context and the value they bring deeply.
This requires time and effort. The leader may decide that, at least for similar
looking groups, standardized metrics of performance can make her job easier.
The leader finds or invents lowest common denominator inputs, activities and
outputs across them and defines metrics for them.

Sometimes the metrics become very abstract in a valiant effort to create a
standardized measure for very different activities. For example, different kinds
of outputs may be converted to notional dollar values via some formula, and a
$/person/month metric created to measure productivity across different
individuals and teams.  The formulas create extra work, in terms of calculating
them. They do not improve the accuracy of measured productivity, due to all
kinds of assumptions baked into the formulas that either don't apply or have to
be subjectively interpreted in the majority of individual cases. Standardization
therefore leads to more work without providing the looked-for insight.

Unfortunately, the standardization is illusory or too abstract to account for
real differences. The objectivity of the metrics is also suspect, as it may not
be measuring real value.

### 3. Destructive Motive: To Replace Human Judgment

Human judgment is subject to biases. Metrics are used to replace human judgement
for measuring performance. If people are asked to judge how well they are doing,
they are likely to over-estimate their performance. When asked to judge how well
someone else is doing, confirmation bias, recency bias and just plain old
misunderstanding will introduce errors in their judgement. Good judgment is a
learnt skill, takes time, is not available everywhere, and even when available
is subject to errors. Metrics are objective.

In most organizations, there are some functions whose value few people
understand. When most business stakeholders do not understand what a function
does and how it does it, and trust between groups is low such that they are
blaming others when they are not achieving their objectives, calls to measure
the functions' contributions increase. The person accountable for a function may
opt for using simple quantitative metrics to expose its contributions or
performance, over the exhausting alternative of educating others on the value of
the function.

Instead of metrics, it is preferable that leaders and stakeholders either
understand the function, and have reliable and trustworthy leaders to lead that
function so they don't have to go into details. When problems between different
business units arise, instead of using metrics to make the units accountable for
each other, it is preferable to create a culture where the units try to resolve
problems at their own level. If a business unit has a problem with another, its
members should feel it normal and *necessary* to have a conversation with the
other unit, quickly. As much as possible they should try to reconcile their
objectives, discover if there are gaps in their understanding, try to resolve as
many differences as possible by exploring their shared goals, and bring any
remaining irreconcilable differences to their leaders.

Sometimes, teams depend on each other but have goals that are inadvertently
mis-aligned with each other, leading to friction. Mis-alignment in *given goals*
is always the groups leaders problem and responsibility. The leaders' job is to
design an organization with functions or business units that are working
harmoniously.  The leaders should not allow themselves to get away with using
metrics to paper over such problems.

In some cases, there are functions whose goals, or at least KPIs, are
*deliberately* not aligned. This can be necessary for implementing
checks-and-balances.  In such situations, leaders should repeatedly and
constantly explain the reasoning behind this situation.

In rare cases, this may not work, as I described in the section "Money Talks!"
in my [previous blog article]. In such cases, abstract metrics are needed  to
justify *some aspects* of the performance of a *part of* the organization. Your
only recourse is to not make them onerous on your team and distract them from
creating value, and to insist that these metrics show only part of the overall
value.

### 4. Destructive Motive: To Reward and Punish

Some organizational units or entire organizations require specialized knowledge
and skills to operate. External stakeholders may feel the need to assert control
over them. However, they lack the knowledge to tell the subject organization
what to do. To assert control, the stakeholders create metrics and associate
them with goals. They then reward or punish the organizational units based on
whether they meet these numeric goals.

One example is American legislation related to improving performance of the
American school system. Teaching, and administration of schools is a specialized
domain of knowledge and expertise. Schools operate in very diverse conditions.
One problem was: there were persistent differences in school performance among
ethnic groups, despite substantial government efforts to equalize spending
across schools. The culprit was assumed to be a lack of professionalism amongst
public school teachers. "Governors, corporate executives, the first Bush
administration, and the Clinton administration agreed: They wanted measurable
results; they wanted to know that the tax dollars invested in public education
were getting a good return" (Diane Ravitch, erstwhile Department of Education
official, writing in the book *The Death and Life of the Great American School
System*). The *No Child Left Behind* (NCLB) act was passed in 2001 by the Bush
administration. It provided for, amongst other things, a regime of testing of
students' academic proficiency, with targets on improvement of scores. An
escalating series of penalties and sanctions on schools in which designated
groups of students did not make adequate progress.

The important thing to notice is that a broad group was convinced that the
school system needed performance goals, and that numeric metrics (student
scores) and setting hard goals for the improvement of those metrics was the way
to improve performance. Regarding whether this worked or not, I will just
briefly state that there is ample evidence that the testing and performance
measurement regime seems to have not led to any significant improvement and have
had several inadvertent negative effects. Ironically, the act's provisions that
are not-metric related seemed to have had more positive impact. (Ref: [*The
Tyranny of Metrics*][muller-1] by Jerry Muller, Chapter 8, p 91.)

### 5. Destructive Motive: To Improve Focus

Sometimes, organizations take on too many different kinds of work, and lose
focus on what is truly important. People may be spending time on "shiny objects"
at the cost of making sure the basics are being done right. Leaders can bring
clarity and focus by articulating a few, clear objectives to tell the
organization what the true north is. However, it is difficult for people to
change their behavior and they may continue to do what they are doing, and
objectives don't get met. In this case, the leader may be forced to define
quantitative goals for every objective and use metrics and targets to get the
organization to focus.

For example, in the book [*Measure What Matters*][measure-book] author John
Doerr describes a "proven approach to operating excellence: Objectives and Key
Results". He writes (highlights mine):

> In this goal-setting system, objectives define what we seek to achieve; key
> results are how those top-priority goals will be attained with specific,
> measurable actions within a set time frame. Everyone's goals, from entry level
> to CEO, are transparent to the entire organization. 

> (As prize pupil Marissa Mayer would say, "It's not a key result **unless it has
> a number**.") You either meet a key result's requirements or you don't; there is
> no gray area, no room for doubt.

In this case, clear objectives are defined to tell the organization what is
important. Metrics (numeric measurements of results) are used to tell the
organization how well the objectives are being met. Defining clear objectives is
essential to bring people together in an organization.

Why have I classified this motivation as a destructive one? There are two
problems. First, in my experience, metrics can leave plenty of room for doubt
about whether objectives are bring met, and I will give examples below. The
second, more sinister problem is that high-level objectives do not capture
everything the organization does. People do work that is essential outside the
OKR framework, and such work is below management's threshold of perception. This
motivation is destructive because it tempts management to believe only the
objectives and results, and work related to them, matter. Objectives and key
results do not cover every situation. It is very tempting to start thinking and
behaving as if metrics *are the only way* to measure if people are achieving
results, and then some part of work for almost everybody will not count. Not
looking at and rewarding good work being done outside the OKR framework can
cripple an organization's ability to make decentralized decisions and use the
judgment of the people who are at the coal face.

If management persists with the idea that OKRs are the only good way to run an
organization, they will try to expand the scope of objectives and results and
bring more work under the ambit of metrics. In his book, *The Delicate Art of
Bureaucracy*, Mark Schwartz quotes another author:

> Although Google became famous for its “20% time,” by which employees were
> encouraged to spend one day a week working on new ideas outside their normal
> tasks, that time is now increasingly subject to audit and performance
> measurement, and their ideas must be entered into a shared database.

Does this version of "20% time" feel like time that is meant for people to feel
free and creative?

### 6. Productive Motive: To Motivate Change

Organizations undertake changes to improve some outcome. People resist change.
One common objection is that the change won't improve the outcome significantly
or at all. By implementing metrics to measure the outcome, getting some
progressive groups to implement change, and then widely sharing the effects on
outcomes (assuming they were positive), leaders can convince conservative groups
that the effect on outcomes is real and significant and convince them to adopt
the changes.

For example, [Peter Pronovost][pronovost], a previous intensive care specialist
physician and professor, concluded that a simple 5 item check-list protocol
would reduce infections in a particular, common, medical procedure. Surgeons are
not fans of checklists. Pronovost managed to convince a large group of hospitals
to participate in 2003 ("Keystone Initiative"), and in 2006 reported that they
were able to reduce infections up to 66%, and save an estimated 1500 lives and
$100 million over 18 months. In 2008 [Time named Pronovost][pronovost-time] one
of the 100 most influential people in the world.

An important aspect of the initiative was that the participants did not just
implement the new protocol, but used metrics. In the original [2006
paper][keystone] on the initiative and in a follow-up [10-year
analysis][keystone2], Pronovost wrote (highlights mine):

> In addition to the intervention ... the ICUs implemented the use of a **daily
> goals sheet** to improve clinician-to-clinician communication within the
> ICU...

> Active involvement of hospital leaders and the Keystone Center as well as
> **ongoing monitoring and feedback of performance** were important in sustaining
> results.

However, Pronovost also wrote (highlights mine):

> The Keystone ICU project demonstrated the potential of **voluntary efforts**
> that rely on **intrinsic motivation** through peer norms and professionalism.

If the physicians were participating voluntarily and had intrinsic motivation to
reduce infection rates, why did the initiative need metrics?  Pronovost's
interpretation is that the improvements came about primarily via:

> a shift in clinicians' belief---by showing them that the rate of infection was
> not inevitable and could be controlled, **in a way that appealed to their
> professional ethos** as doctors and nurses.

In other words, the metrics were used to *inform* and *direct* intrinsic
motivation, not override it. The initiative did not just give clinicians a
metric to improve; they were given training via ongoing calls and coaching, and
data on which interventions seemed to be effective and which not, and so on. The
initiative appealed to the existing motivation amongst doctors and nurses to
provide good care for their patients, and then provided them with support to do
so, including using metrics to show what worked and what did not. 

### 7. Productive Motive: To Discover

Metrics can be used as data to inform decisions. David Selinger, founder and CEO
of RichRelevance, and an ex-Amazon employee [gives two examples][selinger-1].
The first example is about improving something:

> While I was at Amazon, my team proved (65 pages of proof, in fact!) the impact
> of website load times on sales, and identified the metrics that mattered.
> Without hesitation, Bezos and Amazon reorganized around a new, even more
> aggressive method of measuring website performance, changing hundreds of jobs
> to obsess about these very metrics.

The second example is about overcoming blind spots and biases:

> Bezos had a rare ability to set opinions aside in favor of data. At Amazon,
> one of my proposals was to sell advertising on the homepage, and Bezos’s
> initial response wasn’t positive: “It is one of the stupidest ideas I’ve ever
> heard.” Yikes.

> Nonetheless, when I showed data to prove the opportunity, I had approval.
> Bezos told me to run a live test, and from that simple decision we found a
> billion dollars.

Notice that this way of using metrics is quite different from the one espoused
in the "Objectives and Key Results" (OKRs) approach. OKRs are top down and
restrictive. What I described above, in Selinger's words is (highlights mine):

> an approach to business that institutionalizes the **finding, questioning and
> testing** of data ... (it) requires that everyone, regardless of seniority, have
> access to data and tools to test their ideas and intuitions.

**Caution**: Selinger writes "More than anyone I’ve ever met, Bezos knew that
things don’t improve unless they’re measured." However, there is another side to
it. Bezos [also looks at real-life anecdotes][bezos-anecdotes] and not *only*
data:

> The thing I have noticed is that when the anecdotes and the data disagree, the
> anecdotes are usually right. There is something wrong with the way that you
> are measuring it.

> You do need the data, but then you need to check that data with your intuition
> and your instincts.

## Definitions: Metrics, Targets, Goals

For clarity, I will be using some terms with the following meanings:

 * A **metric** is a numerical measurement of some aspect of work. By itself, it
   is devoid of a judgment of value. For e.g., let's consider a software
   development team that is practicing an agile development methodology called
   Scrum. Scrum teams measure their work in terms of *story points*.  During a
   fixed time-internal, called *sprint*, the team attempts to do as much work as
   possible without compromising quality. The amount of work done, measured in
   story points completed per sprint, is called *sprint velocity*. Let's say
   that a team finds average sprint velocity was 40 story points last month. By
   itself, this metric is neither good nor bad. It just tells the state of
   affairs.
 * A **target** is some value for a metric that is considered good.  Let's say
   our software development team feels they could do more work. They set
   themselves a target to raise their sprint velocity from 40 to 45 story
   points.
 * A **goal** is a target that has consequences for not meeting it. Let's say
   that the engineering manager of several application development teams sets
   each team a goal of achieving a sprint velocity of 45 story points. If a team
   exceeds this goal, they are rewarded somehow (team dinner, performance bonus,
   salary increments, etc.).
 * **High stake** goals vs **low stake** goals: how do individuals perceive the
   importance of meeting goals versus the underlying non-numeric objective.
   Let's say the objective of our software development team is to produce high
   value software, with adequate quality, as fast as possible. Sprint velocity
   purports to measure the quantity of features delivered, but not quality. If
   the goal of 45 story points per sprint is perceived to be high stakes, the
   team may assume that the correct behavior expected from them is to increase
   the velocity even if quality drops.

## Is There A Problem? Yes: Metric *Fixation*.

In 1956, in [an article][ridgway-1] in the journal Administrative Science
Quarterly, the author, V.F. Ridgway wrote:

> There is today a strong tendency to state numerically as many as possible of
> the variables with which management must deal.... This has led to the
> development of quantitative performance measurements for all levels within
> organizations,...

This should be good, right? If more people are using quantitative measurements
for performance, as Lord Kelvin said, their knowledge should no longer be "meagre
and unsatisfactory" and should be approaching Science. For some reason, Ridgway
was not happy and went on to write:

> Quantitative measures of performance are tools,... Judicious use of a tool
> requires awareness of possible side effects and reactions.  Otherwise,
> indiscriminate use may result in side effects and reactions outweighing the
> benefits...The cure is sometimes worse than the disease.

As you can see, the author was not positive about quantitative measurements.  In
fact, the title of the article was: *Dysfunctional Consequences of Performance
Measurements*.

At this point, we should be skeptical. As Lord Kelvin said, being able to
express some quantity numerically adds to our knowledge. Further, how can
metrics have "side effects and reactions"?

In the previous sections we looked at some adages promoting metrics. We also
looked at potential motivations behind using metrics and saw some good and some
not so good motivations. To generalize, it seems that many people think that the
*only* way to run an organization well is to use *only* metrics to measure
performance, and to set *goals* against metrics to improve performance.

I will call this phenomena **metric fixation**, borrowing from [Jerry Muller's
book, *The Tyranny of Metrics*][tyranny-metrics]. (I use the term with a broader
definition.)

So the solution would be to promise ourselves that we will not overuse or misuse
metrics. Problem solved? Not so easy. There are many traps to avoid when using
metrics. In this section, I will describe the traps waiting for you when you use
metrics.

There are scholarly papers, books, and articles on the internet that talk about
either a specific failure mode of metrics, or a laundry list of things that can
go wrong. To think about problems with metrics in a structured way, here is a
mental model:

{% include figure.html url='/assets/img/Metrics-Model.png'
description='Metrics Lifecycle' %}

In this model:

  1. Employees do work, that produces some value.
  2. A decision maker needs to measure their performance. The decision maker
     tells employees what will be measured.
  3. Almost always, employees need to do some data entry for the measurement. A
     system of record and allied tooling is needed to capture the data.
  4. The data needs to be curated, aggregated and reported on.
  5. The decision maker looks at the reports and interprets the metrics.
  6. Employees bring unusual situations to attention via emails, calls, ad-hoc
     meetings, escalations, etc., outside the data entry system. This is not
     systematic data yet. Let's call them "anecdotes".
  7. Employees in a position to observe many anecdotes (middle managers), use
     their judgment to see if there are anomalies not captured via metrics, and
     if they do, send a "signal" to decision makers. An anomaly could be
     something going wrong, or an opportunity to potentially take advantage of.
  8. The decision maker needs to decide what to do with the signal, especially
     when it conflicts with metrics.
  9. Decision makers make decisions about what people should be doing. They also
     decide how groups and individuals are performing and give them feedback.
     The decisions and feedback lead to changes in the work being done, data
     being entered, and anecdotes being shared.
  10. While all this is going on, collecting data, reporting it, and discussing
      it involves some time and resources, incurring cost.

These processes are not linear but a in a positive feedback loop. Each area or
topic is impacted by other areas or topics. I will now describe the pitfalls in
each area.

## Pitfalls in Deciding What to Measure

In a business system, there are *inputs*: things we do and the resources we
have; and there are *outputs*: things we produce that others can consume.
Finally, there are *outcomes*: the desired results. Corresponding to each, we
can have input metrics, output metrics and outcome metrics. Outcome metrics give
the most information about the state of a business. However, usually input and
output metrics are easier to measure.

Metrics can be more or less *precise*: precise metrics can be captured as
unambiguous numbers or a narrow range, and they can be compared across different
individuals or groups. Metrics can be more or less *accurate*: more accurate
metrics are closer to the true state of what we want to know. Precise metrics
need not be accurate, and accurate metrics need not be precise. Precise metrics
are often easier to measure and standardize than accurate ones.

The pitfalls in deciding what to measure arise from the temptation to measure
what is easy rather than difficult, and preferring what looks precise over what
is fuzzy.

### Precise but Inaccurate Metrics

There is a strong tendency to prefer precise looking metrics even if their
accuracy is low. This phenomenon has been satirized as the [Streetlight
Effect][wiki-streetlight]:

> A policeman sees a drunk man searching for something under a streetlight and
> asks what the drunk has lost. He says he lost his keys and they both look
> under the streetlight together. After a few minutes the policeman asks if he
> is sure he lost them here, and the drunk replies, no, and that he lost them in
> the park. The policeman asks why he is searching here, and the drunk replies,
> "this is where the light is".

**Example.** In my current role, my team and I advise customers on how to
improve their system architecture to, say, increase reliability or security. The
*inputs* are our activities, viz., meetings we hold with customers and research
we do in between meetings. The *outputs* are the solutions or recommendations we
create for our customers. The *outcomes* are actual improvements in customers'
systems and the impact of those improvements. We find outcomes hard to measure.
A customer may take weeks or months to implement our recommendations and many
sub-groups lack the time and resources to continuously follow-up with customers.
The impact itself may be hard to measure: how do you measure increased security
via a metric? Outcomes are also not easily standardized. A recommendation that
increases the page load speed of a website will have different kinds of value if
it is for an e-commerce website (increased sales) vs an internal tool (staff
productivity and satisfaction).

Note that I used the term "hard" and not "impossible". We *can* measure these if
we really wanted to. We could set time aside to follow-up with customers (or
hired people to do so). We can also get *accurate* though *imprecise* estimates
for the value of increased reliability and security by using methods described
in [*How to Measure Anything*][measure-book] and [*Thinking in
Bets*][bets-book].

However, our functional group has adopted easier to measure and more precise
looking, but less accurate metrics and adopted goals against those metrics. We
simply measure an input: how many meetings we did. The effort behind the
activities and their impact is not measured. This metric can be easily
standardized across teams: after all, we all do meet our customers. We find we
can easily meet the targets associated with this metric; we have enough meetings
with customers and almost any meeting can be considered to be a "customer
advisory engagement". By simply entering a sufficient number of meetings in our
system or record, we can achieve the goal. However, we know a meeting is not
actual impact. We have historically treated this metric and goal as misleading
and just focus on doing the right thing for our customers, measurable or not. We
are somewhat dissatisfied at having to do data entry for no discernible benefit
but treat it as part of the job.

**Avoiding the Pitfall.** The best way to avoid this pitfall is to consciously
prefer accurate metrics over less accurate ones and expending the time and
effort to measure them. When this is not possible, use less accurate metrics but
treat them with a pinch of salt. In my example, we do understand that our metric
is not accurate and focusing on it over doing the right thing for customers
would be participating in the Streetlight Effect.

### Measuring Only Inputs and Outputs, Not Outcomes

This is a specific case of the previous pitfall, because measuring inputs is
easier. Outcomes are often hard to measure.

Consider the desired outcomes of a university or college. A university strives
to educate it's students to: (a) be able to earn money, (b) participate
productively in society and economy, (c) understand how the world works, (d)
make better decisions, and, perhaps also (e) develop an ability to appreciate
art, music and literature, that improves the quality of our lives. All outcomes
except students' starting salaries after graduation are hard to measure.
Universities publish metrics on inputs (graduation diversity, cutoff scores for
admissions, faculty to student ratio, etc.) and outputs (graduation rates,
research papers published and cited).

This is not a problem if the metrics (and goals) are treated with a pinch of
salt and the organization focuses on outcomes, poorly measured though they may
be.  However, if the goals were to become high stakes, resources would be
diverted away from actual work to meeting goals.

**Example.** In many customer organizations that my group works with, software
development teams run as autonomous agile teams working with product managers to
decide what to build. The desired outcomes of such a team are multi-dimensional:
(a) the work should lead to increase in revenue; (b) the software should meet
the needs of end users and seek to delight them; (c) the system should be
performant, reliable and secure; (d) operation individuals should find it easy
to operate the software; (e) it should not cost more than necessary to run.

Measuring performance, reliability and security are hard. It is also hard to
attribute what portion of incremental revenue to attribute to a single
application or feature. Most product managers therefore care about how many
features are delivered---their measurable input metrics, in other words. The
impact of technical work to improve reliability, operability and security is
hard to measure. Product managers seldom prioritize such work.  As a result I
find that organizations have systems that have the needed functionality, but at
the cost of a lot of technical debt. Improvements to system architecture is
undertaken only when there is a problem in production and an engineering manager
or VP steps in to over-ride the product manager and prioritize the reduction of
technical debt. However, by this time, much damage has already been done.

**Avoiding the Pitfall.** The first remedy is to insist on looking at all
desired outcomes, even if they cannot be measured precisely, and consider them
along with input and output metrics. If decision makers regularly consider
outcomes as well as input/output metrics, the groups under them will be less
likely to ignore the unmeasured but important outcomes.  The second remedy is to
create a culture of excellence, substituting the lack of metrics with pride in
one's work. A technical team that understands the important of reliable systems
and is respected by the product manager for their judgment will be able to
negotiate time to reduce their technical debt along with producing features.
Creating a culture is much harder than to invent a metric and goal people
against it, but is the only way to ensure metric fixation does not destroy the
organization.

### Over-Standardization

Decision makers often conceive of a metric and apply it as a "standard" across
many groups whose work is considered to be similar for the purposes of the
metric.  The motivations behind standardization is to assert control (by making
groups' performance objectively comparable to each other) and to reduce
complexity. We run into the pitfall of over-standardization when the metric is
in fact not that standard.

Standardization of metrics almost always loses valuable local context and
encourages measuring everyone with the same yardstick when their circumstances
may be different. Even when leaders acknowledge that two teams are dealing with
somewhat different situations, human beings being human, there is a great
temptation to start a conversation with "why is your metric X much lower than
that other team?" The team now needs to explain that, well, things are
different. Sometimes a team may not even know about that other team's
circumstances, which makes the explanation more difficult and forces the team to
clutch at straws. At best this wastes time re-explaining something that is
already known; at worst, people give up trying to explain and meet the yardstick
via gaming the metric.

**Example.** When I was working for a fast growing startup, at a certain point
the (few) engineering managers could no longer be personally acquainted with all
of them and be familiar with their work. We decided we needed a more formal
performance review system with metrics. We considered a metric: number of
commits to our central version control system. Now, a person may be committing
code less frequently if they were working on a hard task, and more frequently if
they were solving a sequence of easier problems. But since everyone did the same
kinds of work on the same codebase, everyone should get a fair share of hard and
easy problems. The number of commits therefore should reflect employee
productivity. In other words, it would be a "standard" metric that could apply
to everyone. I did a quick check and found that an engineer whose work I was
personally familiar with and held in high regard was pushing far fewer commits
than other engineers. I spoke to the engineer and discovered that the engineer
had a personal workflow on his local system. He'd make several small commits
locally and only when code, tests and documentation were all done, he'd clean up
local commits and push a single logical commit to the central repository. In
contrast, other engineers would commit code as soon as it was compiling,
regardless of whether the overall task was fully completed. This engineer was,
in fact, making effort on making sure his commits were easily comprehensible and
helping his peers and organization. If we had adopted this metric as an input
into performance ratings, we would have mis-classified a high-performing
engineer to be a low performer. In my current organization, a functional group
is facing a similar situation; not exactly code commits, but a similar recording
of work is being measured and goaled globally. One manager with a poor
achievement on the metric spoke to his counterpart in another geography to learn
how their numbers were much higher and discovered they were simply reporting
"work" in fine-grained installments and not on completion of the overall
engagement. This was not malicious: they had always done so as a local best
practice. The problem was that a global "standard" metric and goal was being
adopted when different groups had very different interpretations of the metric.

**Example.** My team members get work requests on an ongoing basis,
unpredictably. The incoming work and associated timelines are dependent on
external customer demands and out of our control. Often, individuals and the
team itself finds demand outstrips supply and have to prioritize work. They do
so primarily on a first-come-first-serve basis. Last year, I decided to make
prioritization more scientific by creating an "impact" score for work requests.
The problem? We do work of different types and only one of them comes with
information about impact in terms of revenue. The impact of other kinds of work
is not easily measured. Still, in a mis-guided attempt to reduce the impact of
different kinds of work to a common metric, I invented formulas to estimate the
value of different kinds of work in notional "dollars". My team, somewhat
bemusedly, went along. We found that the formulas were at the same time too
complicated to do quickly and yet full of assumptions and therefore highly
subjective. After persisting for some time to refine and use our formulas, I
finally took the hint and officially abandoned this misguided attempt to measure
the value of very different kinds of work with a "standard" metric.

**Avoiding the Pitfall.** Overly-standard metrics may seem to save time but in
effect they will waste everyone's time by creating errors in the system that
will later need to be fixed. The first remedy is that before trusting a metric
to be standard, we must investigate it thoroughly by checking in with all (or a
representative sample) of people who actually do the work. The second remedy is
not introduce a standard at all but continue to deal with complexity as it is
instead of trying to paper over it. 

## Pitfalls in Data Input

### Faulty Data: Inadvertent Distortion of Data

Metrics that depend on humans entering data are subject to data entry errors.
Some errors are one-offs (e.g., someone entered 40 instead of 4) and we can
either be caught easily in case of glaring discrepancies. When not every error
can be caught, an inspection can be done to estimate what the error rate is and
account for it in future. For example., agile software development teams know
that estimates of *story points* for tasks are just that: estimates. They expect
tasks to take longer or shorter than they originally estimated, and account for
this uncertainty. However, some errors occur due to ambiguity or
misinterpretation of a metric's meaning and will lead to systematic, cumulative
and growing error in the metric.

**Example.** In my current organization, a peer functional group meets with
customers to find out what they need, and enter a record for each customer
engagement/need in our CRM. They have been asked to "tag" records by one of a
set of "type" of customer need so we can use this data to decide where to invest
more effort. A program manager analyzed three months of data and concluded that
there is high customer demand to run "Business Apps" on the cloud. The term
"business app" was not defined anywhere, but instinctively the program manager
and I both understood it to be Common Off The Shelf (COTS) software that our
customers purchase from software vendors. The program manager asked my help to
see which business apps were popular and if we could do something to make the
process easier for our customers.  I went through all records tagged with
"#BusinessApp" and discovered that at least 50% of customer engagements were not
about COTS software. The people who had been applying the tags were not very
technology minded and if a customer said "web app" they interpreted it to be a
business app. The metric was based on flawed data.

**Avoiding the Pitfall.** The first remedy is to define, communicate and get
feedback about the interpretability of a metric *before* implementing it.
Getting feedback is important to detect your own blind spots. The people who
actually do the work will tell us of situations where the definition is
ambiguous. The second remedy is to do occasional inspection of the data to check
whether the metric is really being interpreted as it was meant to be. Both of
these are much work, so consider the effort before implementing the metric.

### Gaming: Deliberate Distortion of Data

When a metric-based goal is imposed on a group or individual to assert control
over their work, people are tempted to "game" the metrics. The higher-stakes the
goal, the greater the temptation. Due to this, the metric fails to achieve it's
objective of improving performance, diverts resources away from real work to
beating metrics, and incurs significant additional costs in trying to control
the gaming.

Donald T. Campbell, a psychologist and social scientist made a statement that is
now referred to as [Campbell's Law][campbell-law]:

> The more any quantitative social indicator is used for social decision-making,
> the more subject it will be to corruption pressures and the more apt it will
> be to distort and corrupt the social processes it is intended to monitor.

**Example.** Campbell was writing in 1976 about a growing pressure to use
student achievement tests to measure the performance of teachers and schools.
Indeed, the US adopted high-stakes testing, via legislation (e.g., Bush
administration's *No Child Left Behind* act and Obama administration's *Race to
the Top* act). There have been numerous reports of teachers and schools, under
pressure to survive, distorting test scores via either teaching to the test or
outright cheating.

**Example.** ["Sandbagging" in sales][sandbagging-sales] is a rampant phenomenon
in sales organizations where sales representatives are expected to meet goals
for sales *uniformly* through the year, month on month or quarter after quarter.
A sales person who has already met the goal for a particular quarter is tempted
to slow an ongoing deal to the next quarter instead of closing it as quickly as
possible.

**Avoiding the Pitfall.** The first remedy is to not make goals high-stakes but
informational. An environment where metrics are thought of providing information
and not to be used to reward or punish will be one where there is less
temptation to distort metrics. The second remedy, where the goal is indeed
high-stakes, is to not impose the metric and goal but to motivate those who will
actually do the work to adopt the goal as a mission. This is what Pronovost did
in the Keystone Initiative that I wrote about above. 

## Pitfalls in Reporting

Most organizations, when implementing metrics and goals, start with a relatively
few metrics. Starting from nothing, even a few metrics offer insights previously
unavailable. Decision makers realize the power of metrics and start adding more
metrics.

Initially, when the metrics are few, the decision maker is able to retrieve the
metrics and create reports for themselves. More importantly, the decision maker
is able to distinguish between more and less important metrics and also decide
what would indicate a healthy organization and what would indicate a problem,
and choose a representation or visualization that brings these aspects out more
or less clearly (depending on their skill with the reporting tools). Soon
though, the organization and the number of metrics grow beyond the ability of
the decision maker to do the reporting themselves. The organization then hires
resources whose job it to create reports. This leads to several pitfalls.

### Too Many Metrics

Resources hired for reporting do neither the actual work behind the metrics, nor
carry the responsibility of making decisions. Since their job is to report, soon
reports become larger and dashboards proliferate. Seldom is a report trimmed
pro-actively to present the most relevant data. Misunderstandings about metrics
and how to present them creep in. An increasing amount of time is now spent in
finding the signal amidst the noise.

**Example.** An organization I am familiar with invested in resources for
creating self-service dashboards collecting various metrics, to aid senior
decision makers, middle managers and field employees. Starting with a few
dashboards, the system grew as different stakeholders asked for different
reports or asked for more data to be included in existing ones. Soon, there were
too many dashboards to click through, and it took too much time to filter
relevant data across dashboards. Now there is a system on top that captures
visualizations from multiple different dashboards and creates a static weekly
report with all possible information that anyone might ask for---a one size fits
all approach. The report has more metrics than can be reviewed in a group
meeting. What is absent is any discussion of which metrics are most relevant for
discussion in a time-bound meeting.

**Avoiding this Pitfall.** The first remedy is to have people who do the work
and make decisions do reporting their own reporting, as long as possible. When a
reporting reporting resources must be hired, the tendency of metrics and
dashboards to drown the signal amidst the noise has to be compensated. The
remedy for that is to allocate time to get clear on (a) how many metrics can be
discussed in the time available; (b) which metrics are the most important ones;
and (c) what sequence to follow when looking at them, for greatest efficiency;
(d) which metric costs more in reporting and reviewing than the benefit it
provides and remove it from the the agenda of the meeting.

### Precise But Inaccurate Aggregates

Reports show aggregates of individual values---count, sum, average, standard
deviation---as precise numbers. The problem is, some aggregates are misleading.

**Example.** The sales group at at a particular organization looks at the metric
of *average deal size*. The intuition is that larger deals are a better use of
time than doing several small deals. The problem is that a few large deals can
move the average up significantly, and make the metric look better superficially
even when the majority of the deals are small. What is required is metrics like
median, 75th and 90th percentile that give some idea about the distribution of
deals. Even a median as a starting point would prevent a single large deal from
skewing the metric. Since the BI tool does not provide that, it is easier to
stick to a misleading metric.

**Example.** An internet user who works in technical support
[writes][slashdot-support-SLA] that he has a metric of what percentage of
support cases assigned to him are resolved within SLA. His variable pay over
basic pay is tied to the metric. If he resolves 9 cases within SLA and 1 fails
SLA his metric is 90% and he gets 90% of variable pay. So far, so good? The
problem is, the percentage seems to be calculated as a snapshot at certain
moments in time by looking at *only open cases*, not based on past history. So,
for e.g., yesterday he has 10 open cases, 9 within SLA, and 1 breaching SLA, and
their metric was 90%. Today, he closes 5 of the tickets under SLA. He has now 5
tickets remains, 4 under SLA, 1 breaching SLA, and looking only at open cases,
their metric drops to 80%. The metric looks worse even after doing good work. He
explained that this is not a fair way to calculate the metric but management did
not get it. Now it is against his interest to resolve cases as quickly as
possible. He is incentivized to keep cases open as long as possible and resolve
them just on or before the due date, so that anyone looking at their open cases
anytime will see a lot of cases that have not exceeded SLA with only a few
breaching SLA.

A more accurate metric would be to look at both open and closed cases over a
period of time, say last 12 months, and determine what percentage of them were
closed within SLA. This calculation is a bit more complex and costly as it
requires doing business logic on historical data. Most self-service BI tools may
not allow this calculation easily. It is far easier to look at open tickets,
filter their age by SLA and make a quick calculation. Easy, precise and unfair.

**Avoiding the Pitfall.** When using metrics to measure human performance,
accuracy, i.e. measuring something that is a fair representation of work or
results, is important. An approximation that looks "good enough" to decision
makers may have a devastating impact on those doing the work. If you are going
to measure humans with metrics, accepting limitations in measurement, when we
are not accepting limitations of the human, is just unfair. To be sure you are
being accurate instead of just precise, explain the metric to those who will be
measured by it in great detail, and get candid feedback from them, before
implementing the metric.

### Normal Variance vs Significant Variance

## Pitfalls in Interpreting Metrics

### Over-Simplification

In a bid to compress information into a simple to understand metric, we
inadvertently lose a lot of information that is critical to good decision
making. At best, these metrics waste time by making us discuss them. At worst,
they can lead to incorrect decisions.

**Example.** Consider the [CSAT score] used to measure customer satisfaction in
a variety of situations. Customers are asked to rate something between 1
(extremely dissatisfied) to 5 (extremely satisfied). An average over several
responses is computed. Let's say you held a marketing event attended by 50
people, measured CSAT for it by asking attendees to provide feedback, and got an
average of 4.25. What does this mean? At first glance, it looks like you are
doing well, with some areas of improvements. But what improvements?  Let's dig
deeper.  One possibility is that only 4 people responded, with 1 response at 5/5
and another 4 at 4/5. Then the CSAT is probably meaningless since so few people
responded. In fact, the more important metric is the response rate. If too few
people are responding, either the survey tool is broken, or people are just very
disinterested in providing feedback---which might be a cause for concern by
itself. You should improve the survey tool or find out via other means if the
topic was of interest to the vast majority of your customers at all. Now let us
imagine that enough people responded and the CSAT is representative. Now the
question is whether (a) most responses were clustered around 4 with a few
responses at 3 or 5, or (b) Most responses were clustered at 4 and 5, but a
small minority responded with 1? If the situations was (a), you would conclude
that the event was well received and to continue to do what you are doing with
some small improvements to the content, If the situation was (b), you would want
to find out why the small minority was *extremely dissatisfied*. They could be
on Twitter right now venting about their poor experience and tanking your
organization's reputation! You may find out that the event did not describe the
target audience well enough and some people who attended were expecting a
completely different treatment of the topic. You would then fix your event's
marketing rather than the event's content. The point is that the precise looking
number, 4.25, tells you very little. (What is actually useful are response rates
and a histogram of scores.) At best, the CSAT can tell you whether you are doing
extremely poorly, so you can investigate further.

**Avoiding the Pitfall.** The first remedy is to be suspicious of simplified
metrics and ask if they are providing you with the right information; for
example, don't accept averages where you need a percentile, range or histogram.
The second remedy is to not make decisions based on metrics with limited
accuracy without a deep investigation. Beware of averages. They are a good
indicator when two conditions are met: (a) the underlying data has a gaussian
distribution; and (b) the data range is not *clipped* at either end of the
range. If you are not sure your data follows this distribution, look deeper.

### Knee-jerk Improvement

## Pitfalls of ignoring non-metric anecdotes, anomalies and signals

## Pitfalls in Making Metric-based Decisions and Providing Feedback

### Rewarding Luck

Outcomes partially out of control... circumstances... penalties for bad results discouraging ... rewards for things outside control lead to opportunism

### Decisions Based on Partial Information

Metrics capture only part of the information... overly relying on metrics and not looking at signals, judgment... counterexample (Amazon advertising) ... example ... Lehman?

### Punishing Good Performers for a Few Bad Actors

When metrics are used to assert control....  More metrics on those doing good work... may not be worth it to improve precision or gather additional metrics.... instead, dive into specific areas.

### Dehumanizing

People hate being reduced to a set of numbers.

## Pitfalls in Changing Work Based on Metric-based Goals

### Ignoring Work That is Hard to Measure

### Creaming

Not doing essential work that would have a negative impact on metrics.

### Short-Termism

Not doing things that won't bear results in goal period.

### Avoiding Risk

All innovative work comes with risk of failure.

### Undertaking Non-value Generating Work

University ranking improvement via advertisement.... (Muller)

## Pitfalls of ignoring the cost of using metrics

### The Hidden Cost of Metrics

- data entry
- reporting
- discussing, oppt cost

### Quantity over Quality

Measuring things because they are easy, not necessarily meaningful

# Rough notes

## Traps for Work

Knowledge work produces value of several different types. Individuals and groups
need to balance the different kinds of value, and often need to make trade-offs.
Metrics often measure only some aspects of their work.  When the organization
imposes goals on some of these metrics, the individuals and groups change their
behavior. The higher the stakes for a goal, the greater the impact. The impact
is not always positive with respect to the value of the work.

### Metric-Based Goals Prevent Long-term Thinking

Metrics measure performance of work over a period of time, such as a month or
year. Some kinds of value of work can be seen quickly, others take a long
time to become visible (longer than...

### Metrics prevent employees from innovating and taking risks

Innovation, almost by definition, means undertaking work that is not
standardized already, and therefore not being measured by an existing metric. In
a metric-fixated organization, discussing metrics takes time away from
discussing innovative work qualitatively and therefore innovation is
discourages.  Innovative work is risky and may fail. It may not improve metrics.
When metrics are used to measure performance, and when the downsides of not
meeting metrics is high, people play safe and work to improve the metrics
incrementally, instead of thinking and acting on bold initiatives that could
produce outstanding results.

### TODO Creaming: Avoiding Work That Would Lower Metrics



### Goal displacement: Metrics Replace Objectives

Goal displacement or *goal surrogation* is the phenomenon where people start
working to meet a metric as target, instead of the underlying intent. This can
have devastating consequences.

**Anecdote:** In an article from 2019 in the Harvard Business Review, titled
[*Don't Let Metrics Undermine Your Business*][hbr-2019-1], the authors describe
an extreme example of the consequences of surrogation at [Wells
Fargo][wells-fargo-1] bank. This is my summary of what happened: Wells Fargo had
and continues to have a *strategy* of building long-term retail banking
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

Perhaps this is an isolated case?  No. Muller and Schwartz, let alone legions on
the internet, give many other examples of metrics replacing the actual goal, as
far as people's behavior is concerned.


- Work: Metrics prevent employees from innovating and taking risks
  - Problem: Innovating
    - Anecdote: Security engagement enhancement, Conor asking how to measure this (innovating)
    - Anecdote: SUP vs MMY
- What to measure: Problems with defining metrics and goals (or comparisons):
  - Problem: Goal displacement
    - Anecdote: Wells-Fargo
  - Problem: Incorrect metrics set hastily
    - Anecdote: TODO
  - Problem: Standardization of data that is not comparable
    - Anecdote: (Copy scrum anecdote from Reason 2: To Tame Complexity)
  - Problem: Standardization leading to comparison without context
    - Anecdote: Affle - YC - formatting changes; Venkat - SVN commits
  - Problem: Measuring what is easy, not what is meaningful
    - Anecdote: Zero touch - new sign ups, missing: investment $ -- easy to measure #1, not easy to get #2 -- time wasted debating -- needed effort to give good metric missing, leading to misleading metric
  - Problem: Measuring inputs, not outcomes
    - Anecdote: WARs at AWS
- Data Input:
  - Problem: When stakes are high, people will game or cream the metrics
    - Anecdote: Gaming: Sandbagging of oppts
    - Anecdote: Creaming: Surgeons refusing difficult cases - TODO find reference
  - Problem: Subjective data
    - Anecdote: AWS - "Value $" for engagements
  - Problem: Misunderstanding from the employee
    - Anecdote: Affle - logs criticality
    - Anecdote: SMB Business Apps metric
- Reporting:
  - Problem: Too much info
    - Anecdote: AWS weekly data dump -- too much data, complicated to find out what is really needed, overwhelming
  - Problem: Lack of context
    - Anecdote: Security HRIs - outcome: is the customer secure (subjective, many factors); metric: tool report; issue - no way to add context (e.g., Kirsten asking)
- Interpretation
  - Problem: Missing context
    - Anecdote: AWS NAWS host reporting - no reference to risk
  - Problem: over simplification
    - Anecdote: CSAT scores - Summit 2019 with Silent Disco - low scores - no qn about the format
    - Anecdote: CSAT scores - average vs distribution - different conclusions depending on distribution
- Loss:
  - Problem: McNamara Fallacy: *only* looking at metrics, or looking at metrics before anecdotes
    - Anecdote: McNamara fallacy from Schwartz book - 
  - Problem: no time left to look at other things besides metric
    - Anecdote: my team meeting - discussed metrics - left with no time for sharing
  - Problem: when metrics and anecdotes conflict
    - Anecdote: unable to give personal experience. Royal Mail example "thermocline of truth"
  - Problem: Gresham's Law -- bad money drives out good money; Wilson's corollary “Work that produces measurable outcomes tends to drive out work that produces unmeasurable outcomes.” -- Schwartz, Mark. The Delicate Art of Bureaucracy (p. 207). IT Revolution Press. Kindle Edition. 
- Cost
  - Problem: "It just takes 2 mins"
    - Anecdote: TODO
  - Problem: hiring people to report - resource cost - insufficient understanding + moral hazard
    - Anecdote: Moral Hazard: HRIs 2020
- Decisions and feedback
  - Problem: Incorrect decisions - taking metrics at face value - waste of time/money
    - Anecdote: SMB Migrate 2.0 - incorrect tagging
    - Anecdote: SUS vs MMT? - this happened because people need to be measured on revenue - high cost
  - Problem: No decisions. Can you make a decision?
    - Anecdote: TODO
  - Problem: Knee-jerk reaction to improve a number
    - Anecdote: Schwartz - blog popularity - metric without context
  - Problem: demotivating/dehumanizing people - reducing them to a score
    - Anecdote: TODO find reference to "I not stupid" and recent MOE secondary school entry criteria
  - Problem: rewarding luck
    - Anecdote: TODO


#### TODO Measuring inputs rather than outcomes

#### TODO Gaming and Creaming

Goodheart's law

Lowering standards

Gaming

Creaming

#### TODO Hidden costs

Hidden cost of not just collection, but aggregating, reporting, discussing

Diversion of resource from doing to measuring

Unmeasured cost of people entering data

#### TODO Diminishing returns

Accurate but imprecise metrics -> inability to accept fuzzy metrics -> effort to get more precise data -> more effort -> worth it? (When you have a giant spreadsheet of many fine grained metrics, can you understand it and take action?)

Some metrics good, more will be better?

#### TODO Knee-jerk reactions

Just because we have a metric, we must improve it

### TODO Human Cost

- Rule cascades due to bad actors - impact on good performers and rule followers
- Rewarding luck
- Discouraging risk-taking
- Discouraging innovation
- Discouraging co-operating, teamwork
- Anti "purpose" - degrading quality of work


## Benefits of Metrics

- Illustrative: Amazon, Bezos: Website load time, Advertisements
- Diagnostic: pronovost, ???? personal experience?
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
[kelvin-wrong]: https://www.azquotes.com/author/7873-Lord_Kelvin
[kelvin-right]: https://thefutureorganization.com/lord-kelvin-on-measurement/
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
[bets-book]: https://www.amazon.com/Thinking-Bets-Making-Smarter-Decisions-ebook/dp/B074DG9LQF/
[pronovost]: https://en.wikipedia.org/wiki/Peter_Pronovost
[pronovost-time]: http://content.time.com/time/specials/2007/completelist/0,29569,1733748,00.html
[keystone]: https://www.nejm.org/doi/full/10.1056/NEJMoa061115
[keystone2]: https://journals.sagepub.com/doi/10.1177/1062860614568647
[selinger-1]: https://www.entrepreneur.com/article/237326
[bezos-anecdotes]: https://medium.com/the-bridge/at-amazon-despite-all-the-data-anecdotes-still-winning-arguments-875ddaac3f3f
[wiki-streetlight]: https://en.wikipedia.org/wiki/Streetlight_effect
[accuracy-good]: https://www.cuemath.com/measurement/accurate-vs-precise/
[accuracy-wiki]: https://en.wikipedia.org/wiki/Accuracy_and_precision
[CSAT score]: https://www.qualtrics.com/experience-management/customer/what-is-csat/
[campbell-law]: https://en.wikipedia.org/wiki/Campbell%27s_law
[sandbagging-sales]: https://blog.hubspot.com/sales/sandbagging-sales
[slashdot-support-SLA]: https://slashdot.org/comments.pl?sid=18878152&cid=61376762