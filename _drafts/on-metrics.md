---
layout: post
title: On Metrics
---

The audience of this post is the technology leader who is thinking of using
quantitative measurements (metrics) to drive organizational change or to improve
the performance of individuals or teams. I am going to argue that there is
widespread misunderstanding of when and how to use metrics. Using metrics to
measure organizational performance and drive change is extremely dangerous. I
summarize common issues that can arise when introducing metrics. I then offer
advice on when one should introduce metrics and how to avoid the negative
effects.

**Aside**: In a [previous blog article], I wrote how great CTOs use metrics
judiciously to measure the health of a technology function and to drive change.
I also cautioned readers about a problem with metrics. I wrote: "Establishing a
metric and tasking a team to improve it gets people narrowly focused on
improving the metric itself. This can inadvertently lead to *undesirable
behavior*...". I realize now that my advice was badly written. First, my
phrasing understates the danger of people focusing on improving a metric versus
achieving the true objective. Second, this is not the only danger when using
metrics.

An analogy would be that I wrote "If you go into this forest, you *might be*
bitten by a *mosquito*", whereas I should have written "If you go into this
forest, you *will be* attacked by *5 deadly animals*. Specifically, a bear, a
lion, a python, a wild boar and a randomly selected poisonous animal. It is not
certain what order they will attack in, or when they will attack. However, it is
certain is that you will be attacked." See the difference? You may prepare for
your post-prandial forest walk very differently depending on which sentence you
read.

## The Perils of Metrics

One of my favorite authors, [Mark Schwartz][schwartz-amzn], an IT leader and a
"inveterate purveyor of lucubratory prose", cautions against metrics in his book
[*The Delicate Art of Bureaucracy*][schwartz-bureaucracy]. In the chapter
"Bureaucracies of Metrics", he points out several issues with the use of metrics
and gives examples for each.

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

## Questions to Ask of Your Metrics

  * Is a metric worth the cost?

  * Are you examining the ultimate objective and not just the metric?

  * Are your employees motivated to do things that are right but not captured in a metric? How do you know?
  
  * Do you have a metric and an aggressive target but use it to motivate people to innovate instead of measuring their performance?

[previous blog article]: {% post_url 2021-03-30-what-i-learnt-from-ctos-business %}
[schwartz-amzn]: https://www.amazon.com/Mark-Schwartz/e/B01AHGEC2I
[schwartz-bureaucracy]: https://www.amazon.com/gp/product/B086XM4WCK/
[measure-book]: https://www.amazon.com/Measure-What-Matters-Google-Foundation-ebook/dp/B078FZ9SYB/
[drucker-1]: https://athinkingperson.com/2012/12/02/who-said-what-gets-measured-gets-managed/
[drucker-2]: https://www.resultsjunkies.com/revisiting-drucker-what-gets-measured-gets-managed/
[ness-1]:    https://nesslabs.com/what-gets-measured-gets-managed
[caulkin-1]: https://www.theguardian.com/business/2008/feb/10/businesscomment1
[selinger-1]: https://www.entrepreneur.com/article/237326
