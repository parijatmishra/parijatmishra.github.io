---
layout: post
title: On Metrics
---

The intended audience for this article is the business or technology leader who
is considering using quantitative metrics to measure and improve the performance
of their organization, teams and individuals.

In a [previous blog article], I wrote how great CTOs use metrics judiciously to
measure the health of a technology function and to drive change. I did add a
word of caution to go along with it. I believe that I understated the potential
problems with using metrics, and made it look like that it is easy to get them
right. I believe my advice was badly written.

An analogy for what I wrote would be "If you enter this forest, you *might be*
bitten by a *mosquito*".

I should have written something along the lines of "*When* you enter this
forest, you *will be* attacked by *several deadly animals*. It is not certain
what order they will attack in, or when they will attack. However, it is certain
is that you will be attacked. You should prepare yourself by..."

See the difference?

So, with apologies for what I wrote earlier, I want to elaborate upon metrics in
this article. I will try to persuade you that using metrics in the way described
above is always dangerous and sometimes useful in a narrow context. I will
describe the issues that will arise when you try to use metrics. Then, I will
list the situations when metrics should be used, and what precautions to take
when using them.

## A Myth About Metrics

An oft quoted saying is "[only] what gets measured, gets managed." With respect
to running a business, the saying is interpreted as "if you want to change
something, start my measuring it", or alternatively, "if you are not measuring
some aspect of your business, you are not managing it." An implication is that
one should metrics, a lot. The saying is sometimes attributed to [Peter
Drucker], the great management guru ([e.g. 1][drucker-attrib-1], [e.g.
2][drucker-attrib-2]). If Drucker said this, it must be wise and right.

Sounds legit?

Some people are not sure. There does not seem to be evidence that Drucker
actually ever said this ([e.g.][drucker-noattrib]). More importantly, the phrase
is misleading. The journalist [Simon Caulkin][caulkin-1], wrote:

> If there's one management platitude that should have been throttled at birth,
> it's 'what gets measured gets managed'. It's not that it's not true---it is---
> but it is often misunderstood, with disastrous consequences.

> The full proposition is: 'What gets measured gets managed - even when it's
> pointless to measure and manage it, and even if it harms the purpose of the
> organisation to do so.'

Caulkin refers to this [paper][ridgway-1] from 1956, titled "Dysfunctional
Consequences of Performance Measurements", which says:

> There is today a strong tendency to state numerically as many as possible of
> the variables with which management must deal. ... The cure is sometimes worse
> than the disease.

The paper warns against "indiscriminate use and undue confidence and reliance"
on quantitative measures of performance, and cautions that "judicious use of a
tool requires awareness of the full effects and consequences."

## How Bad Can the Effects of Metrics Be?

There are many dangers with using metrics. I will talk about them in a while,
but first let us examine how bad can things be, if metrics are not used well.

Let me describe just one of the issues with metrics here: *surrogation* or goal
displacement. Metrics are often initially implemented to measure some aspect of
a business, as a *partial* representation of progress towards an ultimate
objective.  However, humans being humans, managers, teams and individuals have a
tendency to focus on improving the metric itself rather than meeting the
objective.  If you think this is the exception and rare, consider the cautionary
articles above--they would not be writted if this was uncommon. But what about
the consequences? Are they serious?

An article from 2019 in the Harvard Business Review, titled "[Don't Let Metrics
Undermine Your Business][hbr-2019-1]", the authors describe an extreme example
of the consequences of surrogation at the bank [Wells Fargo][wells-fargo-1]. The
authors of the paper write:

> In other words, Wells Fargo had—--and still has—--a strategy of building
> long-term customer relationships, and management intended to track the degree
> to which it was accomplishing that goal by measuring cross-selling. With
> brutal irony, a focus on the metric unraveled many of the bank’s valuable
> long-term relationships.

This is my summary of what happened:

  * Wells Fargo has a *strategic focus* of long-term retail banking relationships;
  * They already had a *metric* of *cross-sell*--when a customer buys one
    product and the sales person is able to convince to buy more products. Of
    course, this should only be done with the customers' interest at heart--the
    customer must genuinely need, want and benefit from the additional product.
  * Wells-Fargo decided to *align* the cross-sell *metric* with the *strategy*.
  * Employees started believing that improving the cross-sell metric was meeting
    a strategic goal. They acted, at a large scale and over a long period of
    time, as if cross-selling *was* the strategy.
  * To meet this "goal" under pressure, employees fradulently opened millions of
    deposit and credit accounts without customer consent. Due to sales pressure
    and a lack of desire to look under the hood of where the higher cross-sell
    numbers were coming from and why, managers and senior leaders did not detect
    fradulent behavior early.
  * Since the misbehavior came to light, Wells-Fargo has had to spend billiions
    on reimbursing customers, paying damaages and fines, and for litigation.
    They've had regulatory limitations slapped on them. And, besides losing
    money, the bank has also lost customer trust. Pretty consequential effects.

The authors examine the underlying causes and conclude that the root cause was a
pervasive culture of measuring performance by measurement of metrics. They caution:

> The mental tendency to replace strategy with metrics can destroy company
> value.

## The Perils of Metrics

[Mark Schwartz][schwartz-amzn], an IT leader and a "inveterate purveyor of
lucubratory prose", writes about bureaucracy in his book [*The Delicate Art of
Bureaucracy*][schwartz-bureaucracy]. In the chapter "Bureaucracies of Metrics",
he points out several issues with the use of metrics and gives examples for
each. Briefly, they are:

  * *Inefficiency*: metrics have a cost associated with them

 * *Hidden Inefficiency.* There is a cost associated with not only gathering
   them, but then organizing them, reviewing them, and formulating action plans
   to address them. Organizations can become metric fixated.  He says, "the
   problem is that they're often collected across the board, even in places
   where they won't lead to actionable insights." When there are more metrics,
   there is more effort spent on reporting them, disseminating them, and
   discussing them in meetings.
  
  * *Surrogation.* Metrics often come with a target. Too often, once a metric
    and a target for it is introduced, managers and leaders start looking at
    them at the cost of looking at the ultimate objective. This almost always
    leads to people accountable for the metrics to game them by finding creative
    ways of getting them closer to the target, and to even decline or avoid work
    that would not improve the metric.
  
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
[Peter Drucker]: https://en.wikipedia.org/wiki/Peter_Drucker
[drucker-attrib-1]: https://www.resultsjunkies.com/revisiting-drucker-what-gets-measured-gets-managed/
[drucker-attrib-2]: https://link.springer.com/chapter/10.1057/9781137375469_7
[drucker-noattrib]: https://athinkingperson.com/2012/12/02/who-said-what-gets-measured-gets-managed/
[caulkin-1]: https://www.theguardian.com/business/2008/feb/10/businesscomment1
[ridgway-1]: https://www.jstor.org/stable/2390989?origin=crossref&seq=1
[wells-fargo-1]: https://en.wikipedia.org/wiki/Wells_Fargo_account_fraud_scandal
[hbr-2019-1]: https://hbr.org/2019/09/dont-let-metrics-undermine-your-business
[schwartz-amzn]: https://www.amazon.com/Mark-Schwartz/e/B01AHGEC2I
[schwartz-bureaucracy]: https://www.amazon.com/gp/product/B086XM4WCK/
[measure-book]: https://www.amazon.com/Measure-What-Matters-Google-Foundation-ebook/dp/B078FZ9SYB/

[selinger-1]: https://www.entrepreneur.com/article/237326
