---
layout: post
title: On Metrics
---

The intended audience for this article is the business or technology leader who
is considering using quantitative metrics to measure and improve the performance
of their organization, teams and individuals.

In a [previous blog article], I wrote how great CTOs use metrics judiciously to
measure the health of a technology function and to drive change. On re-reading,
I believe while I did not say anything incorrect *per se*, I did write it badly.
I understated the potential problems with using metrics, and made it look like
that it is easy to get them right.

An analogy for what I wrote would be "If you enter this forest, you *might be*
bitten by a *mosquito*".

I should have written something more along the lines of "*When* you enter this
forest, you *will be* attacked by *several deadly animals*. It is not certain
what order they will attack in, or when they will attack. However, it is certain
is that you will be attacked. You should prepare yourself by..."

See the difference?

So, with apologies for what I wrote earlier, I want to elaborate upon metrics in
this article.

I will try to persuade you that while metrics are sometimes useful, metric
fixation is always dangerous. I will describe the issues that will arise when
you try to use metrics. Then, I will list the situations when metrics should be
used, and what precautions to take when using them.

## Some History

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
*more* knowledge.

Somehow, over the centuries, this got distorted into the idea that the *only*
knowledge that matters is that which can be measured numerically.  In 1956, V.F.
Ridgway wrote in [an article in Administrative Science Quarterly][ridgway-1]
about the *Dysfunctional Consequences of Performance Measurements*:

> There is today a strong tendency to state numerically as many as possible of
> the variables with which management must deal.... This has led to the
> development of quantitative performance measurements for all levels within
> organizations,...
> 
> Quantitative measures of performance are tools,... Judicious use of a tool
> requires awareness of possible side effects and reactions.  Otherwise,
> indiscriminate use may result in side effects and reactions outweighing the
> benefits...The cure is sometimes worse than the disease.

An oft quoted saying is "[only] what gets measured, gets managed." The saying is
sometimes attributed to [Peter Drucker], the great management guru ([e.g.
1][drucker-attrib-1], [e.g. 2][drucker-attrib-2]). Another variant of the saying
is "What Gets Measured Gets Done", [attributed to Tom Peters][tom-peters-1986]
from 1986.

If Drucker said this, it must be wise and right, right?  Some people are not
sure. There does not seem to be evidence that Drucker actually ever said this
([e.g.][drucker-noattrib]). More importantly, the phrase as quoted is
misleading. The journalist [Simon Caulkin][caulkin-1], referring to Ridgway's
article and other sources, wrote:

> If there's one management platitude that should have been throttled at birth,
> it's 'what gets measured gets managed'. It's not that it's not true---it is---
> but it is **often misunderstood, with disastrous consequences.**

> The full proposition is: 'What gets measured gets managed - even when it's
> pointless to measure and manage it, and even if it harms the purpose of the
> organisation to do so.'

At this point, we should be skeptical. As Lord Kelvin said, being able to
express some quantity numerically adds to our knowledge. So how can measuring
something be pointless? Even if we assume that some numbers could be pointless,
how could their existence harm the purpose of the organization?

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
warnings about using metrics.

## The Curious Case of The Metric Replacing The Strategy

Are the warnings merited?  How bad can things get, even if it were possible to
somehow misuse our humble servant, the number?  Perhaps the authors are
over-reacting.

In an article from 2019 in the Harvard Business Review, titled [*Don't Let
Metrics Undermine Your Business*][hbr-2019-1], the authors describe an extreme
example of the consequences of surrogation at the bank [Wells
Fargo][wells-fargo-1]. The authors of the paper write:

> In other words, Wells Fargo had—--and still has—--a strategy of building
> long-term customer relationships, and management intended to track the degree
> to which it was accomplishing that goal by measuring cross-selling. With
> brutal irony, a focus on the metric unraveled many of the bank’s valuable
> long-term relationships.

This is my summary of what happened: Wells Fargo had and continues to have a
*strategy* of building long-term retail banking relationships with customers.
They already had a *metric* for cross-selling activities. Wells-Fargo decided to
*align* the *metric* with the *strategy*. Unfortunately, employees started
acting, at a large scale and over a long period of time, as if cross-selling
*was* the strategy. To meet this non-existent "strategic goal", employees
*fraudulently* opened millions of deposit and credit accounts without customer
consent. For some reason, managers and senior leaders did not detect that the
increasing number of accounts from so-called "cross-selling" were created in a
fraudulent manner. Initially, when some customer complained about fees and
charges related to accounts they had never consented to creating, or unexpected
credit cards and mortgages they did not sign up to, the incidents were blamed on
a few, over-zealous employees; no one thought to check whether this was a
wide-spread occurrence.

Since the misbehavior came to light, Wells Fargo has had to spend billions on
reimbursing customers, paying damages and fines, and for litigation. Regulators
stopped them from growing their assets for a while (meaning, Wells Fargo could
not get new business, even legitimately, while they continued to pay damages and
fines). And, besides losing money, the bank has also lost customer trust: the
issue came to light in 2016, and the bank is reporting a fall in new customer
sign-ups even in 2021. The damage to the bank has been extensive and persistent.

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

Are we done? Are there other problems?  You bet.

## The Perils of Metrics

As you can see, warnings against overuse or misuse
Muller, who I quoted above, gives a list of the various problems that can arise
when trying to use metrics.

  1. People tend to measure what is more easily measurable at the cost of
     measuring what is truly important (but is difficult to measure).
  2. People tend to measure only one or two aspects of an outcome that is
     complex and multi-dimensional, again because it is easier to do so.
  3. 

[Mark Schwartz][schwartz-amzn], an IT leader and a "inveterate purveyor of
lucubratory prose", writes about bureaucracy in his book [*The Delicate Art of
Bureaucracy*][schwartz-bureaucracy]. In the chapter *Bureaucracies of Metrics*,
he points out several issues with "metric fixation" and gives examples for each.

(*I highly recommend reading the whole book, and other books from Mark, as Mark
writes insightfully and humorously on topics relevant to technology leaders.*)

An over reliance on metrics leads to:

  1. **Surrogation**, or **Goal Displacement.** Metrics are often confused with
     objectives, with very bad consequences.
  1. **Inefficiency.** Widespread use of metrics is surprisingly inefficient.
  1. **Calcification.** Metrics can prevent people from innovating and
     experimenting.
  1. **Over-confidence.** Metrics can lead to people ignoring other relevant
     information.
  1. **Over-simplification.** A tendency of humans to simplify metrics more than
     is scientifically tenable, resulting in incorrect conclusions.
  1. **Recklessness.** There is a tendency to believe that if a metric exists,
     it must be "improved", without considering its context.
  1. **Robotization.** People dislike their multi-dimensional contributions
     being measured only by a smattering of metrics, or their performance being
     reduced to a number or score.

### TODO: Surrogation

### TODO: Inefficiency

### TODO: Calcification

### TODO: Over confidence

... incorrect conclusions

### TODO: Recklessness

... knee-jerk tendency to improve the metric

### TODO: Robotization


  * *Stifling Innovation.* In theory, the existence of a metric does not prevent
    teams and individuals from doing things that are innovative. In practice,
    metrics make this harder. Consider the two cases:

    * An employee is doing something whose effects will be captured by a metric.
      Let's assume that the target for that metric is reasonable and
      extrapolated from past performance. In this case, the incentive to
      innovate (that is, do things radically differently) is low. The best
      strategy to do more of what was already being done. There can be
      improvements in productivity and efficiency, but one should not expect
      people to be thinking out of the box. Innovation is risky and may fail.
      Trying something innovative may cause a temporary dip in a metric. Someone
      who fears missing their target and knows failure will not be rewarded has
      no incentive to try something new and different.
    
    * An employee is trying to do something whose results will not be captured
      in any metric they are accountable for. Are they motivated to do so? Do
      they believe they will get recognition for it? Do leaders have time to
      talk about innovations or are they buried under mountains of
      pre-determined metrics?

  * *Creation of Blind Spots*. We are tempted to choose metrics that are easy to
    measure even if they are less informative or relevant over metrics that may
    be harder to measure but closer to what we care about. This constant
    temptation leads to an increasing amount of time being devoted to work whose
    outcomes are easily measured over work whose outcomes are hard to measure or
    cannot be measured. Pretty soon organizations start ignoring important work
    that takes a great deal of effort to justify. All is well for a while as the
    metrics are looking good, when suddenly the organization is blindsided by a
    crisis.
  
  * *Treating People as Robots.* This is especially true when (a) meeting metric
    targets is used to evaluate people's performance, and (b) when performance
    evaluation is presented as a metric.
    
    * (a) A metric-target based performance evaluation system is supposed to
      bring about fairness and objectivity in large organizations. However,
      because of all the issues above, a metric is less than faithful
      representation of the value of people's work. Hence, in most cases,
      measuring someone's performance by only looking at whether they hit their
      targets (or even making this the dominant criteria) is not really fair. It
      *could* be objective if not fair, but only in those cases where it is
      impossible for anyone to game the metric and the metrics are a
      comprehensive, total, reflection of value. Are there any such cases?
    
    * (b) In some organizations, employees are given a precise-looking score or
      grade as part of their performance appraisal. This almost always leads to
      questions like "why did I get a score of X and not Y", "how did you arrive
      at this score". What the employees really want to know is two things: (a)
      am I doing well overall against expectations; (b) what am I doing well,
      and which areas should I improve in. Good managers should be addressing
      these topics with their employees.  If they are doing so, the precise
      score is irrelevant. Performance scores or grades only serve to make
      people feel as if they are not people but a piece of machinery.
  
  * *Over-simplification.* As organizations grow larger, it becomes harder for
    leaders to understand everything in full detail, and metrics are created to
    provide a summary.  These metrics are a necessarily simplified
    representation of the state of affairs. They can give directional
    information about where things are going. When making everyday decisions,
    over-simplified metrics are less useful. Two problems occur when people try
    to make everyday decisions based on simplified metrics that are easy to
    convey, but do not tell the full story.

    * The first problem is a tendency for people get hypnotized by the metric
      itself and jump to the conclusion that it must be "improved" without
      looking deeper into it. This happens because simplified metrics come
      without surrounding context in which to interpret them. An aggravating
      factor is when someone is "accountable" but "responsible" for a metric.
      This could happen in the context of a project or program where a program
      manager is looking at the metrics and presenting them to senior
      leadership, but is not the one doing the actual work that could change the
      metric. In such cases, there is a temptation to try to "improve the
      metric" and this can be counter-productive unless the context for the
      metric has been somehow obtained (by picking "old timers" brains, for
      e.g.).

    * The second problem is a metric that has been over-simplified to the point
      where it is meaningless or misleading. For e.g., the average of a set of
      scores is used very widely because it is simple to calculate and present.
      There are many situations where the average is not the right aggregation
      and it is not telling you what you *think* it should be. Taking actions
      based only on or designed to "improve" such metrics is dangerous and can
      be counter-productive to the actual objective.

## Using Metrics "Judiciously"

### Fighting Surrogation

Quoting the previously referenced paper in *Harvard Business Review*:

> Nobel prize winner Daniel Kahneman and Yale professor Shane Frederick
> postulate that three conditions are necessary to produce the type of
> substitution we see with surrogation:
>
>   1. The objective or strategy is fairly abstract.
>   2. The metric of the strategy is concrete and conspicuous.
>   3. The employee accepts, at least subconsciously, the substitution of the metric for the strategy.


  * Is a metric worth the cost?

  * Are you examining the ultimate objective and not just the metric?

  * Are your employees motivated to do things that are right but not captured in a metric? How do you know?
  
  * Do you have a metric and an aggressive target but use it to motivate people to innovate instead of measuring their performance?

[previous blog article]: {% post_url 2021-03-30-what-i-learnt-from-ctos-business %}
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
[schwartz]: https://www.amazon.com/Mark-Schwartz/e/B01AHGEC2I
[schwartz-bureaucracy]: https://www.amazon.com/gp/product/B086XM4WCK/
[measure-book]: https://www.amazon.com/Measure-What-Matters-Google-Foundation-ebook/dp/B078FZ9SYB/

[selinger-1]: https://www.entrepreneur.com/article/237326
