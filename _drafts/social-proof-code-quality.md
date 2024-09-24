---
layout: post
title: The Social Psychology of Code Quality
---

Long ago, I started an effort to improve the quality of my company's codebase. I
failed, miserably. I wish I knew about _social proof_ then. Don't be me.

Some context. After years of developing software as an individual contributor, I
was invited to join a startup as _first techie_. I wrote a prototype, we did
some demos, we got funding and we started in earnest. I recruiter a small team
of awesome people, each better than me, and we started building out our MVP.

Initially our focus was on adding new features as fast as we could imagine them.
We had some modest success. The business grew, we expanded the team, and it was
us against the world! Awesome days!

After a while, I started getting worried about the increasing technical debt in
our codebase. Implementing new features required increasing effort. Surprising
bugs popped up in production more often. I tried to get the team to improve the
quality of our codebase.

1/ I repeatedly explained the pain points and the value of good code in our team
meetings. People agreed. There was no real progress.

2/ I wrote the best code I could, documented it thoroughly, and smothered it
with tests. I showed my work to the team. People agreed this was the standard
everyone should aspire to. Still, there was no real progress.

3/ A senior engineer added a bunch of linters to our build process. The team
agreed to check its output before committing our code. Things looked good for a
few weeks, then we fell back to our old ways. Yup, there was no real progress.

4/ I proposed a per-developer code quality metric that I would track. The result
was a mini-rebellion. I beat a hasty retreat and never implemented the idea. The
mere suggestion still did damage: junior developers started avoiding gnarly
areas of the codebase and harder-looking bugs. It took many 1:1s to get them out
of that mode.

Nothing seemed to stick. At some point, I gave up. We did ship a product,
expanded it, and grew the userbase to millions. Still, technical debt hung over
our necks like the Sword of Damocles. Every new feature added was an uphill
struggle. It was... unpleasant. The exit was nice, though.

I wish I knew then what I know today. (Don't we all?) In particular, I did not realise that building and maintaining systems is

In a later stint as a tech leader, I inherited a complex sprawl of a tech estate
and a skeleton team. I managed to grow the team, build squads, get the code
quality improved, reduce tech debt, and reduce costs. I used my hard-earned
lessons of social psychology. I did the following:

1/ In team meetings, I asked what causes them pain. Some team members called out
bad code quality as the chief source of pain. (I might have prepped them in my
1:1s.).

2/ When the team agreed that code quality was lacking, I got them to identify a
few quality related metrics that they would agree to track. (I might have had
them handy and proposed these would be easy to start with.) I created squads
with areas of responsibility.

3/ In subsequent meetings, when a squad's quality metrics were improving,
someone from another squad would ask them why and how. There would be a
discussion, with new insights on ways of doing things. (I might have initially
privately nudged someone to ask such questions; soon I did not have to.)

4/ The team members competed with themselves on improving code quality without
sacrificing timely delivery. They taught each other. They had heated debates on
what the balance was. They learnt to respect each other's judgment even when
they disagreed. They agreed to disagree for the time being. They put up their
hands to own the quality of some areas.

Why did this work better? Would this work for you? Would this work better than
other things you could think of?

## What Does Not Work

1/ **Exhortations.** When I exhorted my team to improve code quality, I was
mistaking a system problem as an individual one. When it comes to repeated
problems in a complex system with conflicting priorities, [good intentions
don't work](#good-intentions-dont-work), we need good processes.

2/ **Outsiders.** When I tried to lead by example, I forgot that
their perception was that my circumstances were different from theirs. I
could pick the problems to work on and take my own time to write exemplary
code. Could they? They didn't believe so. So my examples didn't translate
into action.

3/ **Authority.** When I _dictated_ to them that they look and resolve the
issues thrown by the linters we had introduced in the build process, things
improved. Partly, I was in a position of authority and I was obeyed.
Additionally, people knew they were trusted and could explain to me why they
disregarded some warnings from the linter. A crisis, followed by a hectic
delivery meant that for several weeks I didn't review the metrics, and after
that I didn't get back to it (I'm human and fallible). When that happened,
things soon went back to the previous ways.

4/ **Simplistic Targets.** There was a mini-rebellion when I proposed that the
number of code issues per developer should be a performance metric. This was a
good thing. Metrics to measure human performance are very hard to get right.
[Simplistic metrics encourage bad behaviour](#pitfalls-of-performance-metrics)
instead of good judgment. I might have destroyed the team if I had gotten my
way.

## Quality is a Social Norm

While writing code is usually a solitary activity, building and maintaining a
system is a group activity. A system has many stakeholders: business leaders,
product managers, scrum masters, team leads, peers. They have different
interests, and differing ideas of what is important. They must constantly
communicate and negotiate their priorities with each other. When working on an
individual piece of work, a programmer has to balance two opposing forces---time
available (aka speed of delivery) and quality.

This is similar to society at large. At an individual level, we need to make
decisions for ourselves, that also impact society. How much effort should we put
in recycling waste? In conserving energy? In conserving water? In conservation
of natural habitats? In eating healthier food? In driving carefully?

In writing code, choosing food, and driving, there is a great deal of
uncertainty on what the right thing to do is. And so we come to one of the core
principals of human behaviour. To wit:

1. "Uncertainty: In Its Throes, Conformity Grows"
2. "When people are free to do as they please, they usually imitate one another."

## Random thoughts

**Goal**: I want to demonstrate that using SQ EE portfolios is the best way to increase
code quality in an enterprise.

**Takeaway**: The portfolios feature of SQEE / SCE is the best way to get teams to benchmark against each other.

**Why**: Sets social norms. You improve one/two teams, rest will follow.

**Audience**: those with SQ CE/DE licenses and reluctant to buy SQ EE.

**Story**: Improving code quality across an org is not simple because:

- Telling devs to improve code quality doesn't work. [good intentions don't work](#good-intentions-dont-work)
- Showing a dev/team their code quality doesn't work
  - There's always a tradeoff between speed and quality
  - We tried our best and our score is X.
  - What is "good"? Whatever manager says?
- Portfolios:
  - Compare across teams and over time
  - Both managers and teams have same view
  - Teams can compare with each other
    - Teams can bitch about each other -- "that team had it too easy/are different"
  - You can motivate teams to learn from each other
- How to get started: get one team onboard; show their work
- amplify: when we are unsure of what is best to do (uncertainty); when the evidence of what is best to do comes from numerous others (the many); and when that evidence comes from people like us (similarity).

Principle of social proof: The greater the number of people who find any idea correct, the more a given individual will perceive the idea to be correct.

Optimizers: when we are unsure of what is best to do (uncertainty); when the evidence of what is best to do comes from numerous others (the many); and when that evidence comes from people like us (similarity).

**Anecdotes**:

- Advise _and_ help: every internal doc page in AWS had a feedback link while in JP they didn't
- _Learned helplessness_ - when people don't know how to debate/ask advice <-- forcing SQ reports on devs/teams; not giving them SonarLint
- Getting-started: get one team onboard, show their work -- my trip to Phuket with a friend, low season, empty restaurants, when we entered, a lot of others did too

## Notes and References

### Good Intentions Don't Work

During my tenure at Amazon, I learnt about a particular philosophy of solving
problems.

> “Good intentions never work, you need good mechanisms to make anything
> happen." -- Jeff Bezos (paraphrased)

Jeff Bezos, founder of Amazon---observed that asking people to try harder doen't
solve recurring problems. People are _already_ doing their best. They have good
intentions. At best, people will put in extra hours and heroically rescue a bad
situation. This is not a permanent solution.

A recurring problem---as opposed to a one-off problem---is by definition a
_system_ problem. The solution is a change to the system. He coined the term
"mechanism" to describe the criteria for acceptable solutions.

You will find many descriptions and interpretations of Bezos' "mechanism"
concept on the internet. I can't vouch for their fidelity or correct
interpretation of the concept. Here are two links that are somewhat
authoritative.

- [AWS Well Architected Framework: Operational Readiness Review: Building
  mechanisms](https://docs.aws.amazon.com/wellarchitected/latest/operational-readiness-reviews/building-mechanisms.html):
  This particular page of an otherwise highly technical document contains a
  short description of a "mechanism" as used in Amazon.
- [How we leverage mechanisms at Amazon? - Zak Islam, Director of Engineering at
  AWS](https://www.youtube.com/watch?v=rIxFHQJhJ2Y): This ~30m YouTube video
  goes into more detail about mechanisms and how they are used within Amazon.

### Pitfalls of Performance Metrics

KPIs, OKRs, quantitative metrics, targets, and other quantitative metrics are
powerful tools, but when applied to knowledge work requiring high judgment, they
can easily cause lasting and deep damage. The key is to use them _judiciously_.

I wrote at length about this topic in a [previous article]({% post_url
2021-05-26-avoiding-pitfalls-metrics-performance %}).

### Popularity Begets Popularity

Managers of a restaurant chain in Beijing partnered with researchers to figure
out how to get customers to choose certain menu items. Since they made and sold
more of these, it would be profitable for them to sell even more of them.
Instead of lowering prices, adding expensive ingredients or bringing in a
top-tier chef, they added the label “most popular” to those dishes. Sales of
those dishes shot up by 13 to 20 percent. Other labels like "Specialty of the
house" or "Chef's Recommentation" did not work as well or at all. Turns out,
people love what’s already loved. This cost them nothing, was totally ethical,
and as simple as reading a label! See [_"Observational Learning: Evidence from a
Randomized Natural Field Experiment_ by Cai _et al_, 2009 in _American Economic
Review_](https://www.aeaweb.org/articles?id=10.1257/aer.99.3.864).

A brewery-pub in London started placing a sign on the bar stating, truthfully,
that its most popular beer that week was its porter. Porter sales doubled almost
immediately. See [_The Choice Factory: 25 behavioural biases that influence what
we buy_ by Richard Shotton, 2018.](https://www.amazon.sg/Choice-Factory-behavioural-biases-influence/dp/085719609X).

Healthy eating: Dutch high school students increased fruit consumption by 35
percent—even though when told their peers eat fruit to keep healthy. They also
had claimed no intention to change upon receiving the information. See [_Don't
tell me what I should do, but what others do: the influence of descriptive and
injunctive peer norms on fruit consumption in adolescents_ by Stok FM, et al,
2014, in _National Library of Medicine_, National Institutes of
Health](https://pubmed.ncbi.nlm.nih.gov/23406475/).

Science-based recommendations: During the COVID-19 outbreak, researchers studied
the reasons Japanese citizens chose to wear face masks: only one reason made a
major difference in mask-wearing frequency: seeing other people wearing masks.
See [_Why Do Japanese People Use Masks Against COVID-19_ by Nakayachi _et al_,
2020, in _Frontiers in
Psychology_](https://www.frontiersin.org/journals/psychology/articles/10.3389/fpsyg.2020.01918/full).

### Social Acceptance

Researchers hooked participant to FMRI scanners, who then received information
that conflicted with their opinion. The participants had to rate the reliability
of the information, and agree or disagree to conform to it. Group A were given
the information on a computer screen. Group B were given the information by
humans. For participants that rated the reliability of the information as the
same, the ones in the group receiving it from computers agreed to conform less
often than the ones in the group receiving the information from humans. _If the
information was rated equally reliably, why did it matter whether it came from
computers or humans?_ It seems that defying other people produced a painful
emotional state: the sector of their brains associated with negative emotion
(the amygdala) became activated, reflecting what the researchers called “the
pain of independence.” Defying a set of computers didn’t have the same
behavioral consequences, because it didn’t have the same social-acceptance
consequences. See [_Neurobiological correlates of social conformity and
independence during mental rotation_ by Berns _et al_, 2005, in _Biological
Psychiatry_](https://pubmed.ncbi.nlm.nih.gov/15978553/).

See [_Neuroscience and the social origins of moral behavior: How neural
underpinnings of social categorization and conformity affect everyday moral and
immoral behavior_ by Ellemers & van Nunspeet, 2020, in _Current Directions in
Psychological Science_](https://psycnet.apa.org/record/2020-75764-013).

### Feasibility

Researchers studied households' willingness to recycle waste when given
different reasons to do so, in the Italian cities of Rome, Cagliari, Terni, and
Macomer. They concluded that households were most willing to recycle if they
believed that _many_ of their neighbours recycled at home, in part because they
saw recycling as less difficult to manage. See [_Distinguishing the sources of
normative influence on proenvironmental behaviors: The role of local norms in
household waste recycling_ by Fornara _et al_, 2011, in _Group Processes &
Intergroup
Relations_](https://journals.sagepub.com/doi/10.1177/1368430211408149).

Researchers sent messages to households in San Marcos, California, asking them
to conserve energy. There were four variants: "The environment will benefit";
"It's the socially responsible thing to do"; "It will save you significant money
on your next power bill"; and finally the _social proof_ message "Most of your
fellow community residents do try to conserve energy at home." The households
getting the social-proof message saved 3.5 times as much energy as those getting
any of the other messages. In a further twist, there were two control groups in
the study. Control group A got no message at all. Control group B got a message
simply urging them to save energy. The difference between the two control groups
was negligible, giving credence to the idea that simply exhorting people does
not work. See [_Normative social influence is underdetected_ by Nolan _et al_,
2008, in _Peronality and Social Psychology
Bulletin_](https://pubmed.ncbi.nlm.nih.gov/18550863/).

### Similarity

Some physicians routinely overprescribe some medicines, such as antibiotics. Of
the several attempts to get them to change their behavior, only one method
brought about lasting change: comparison of their presription rates to peers.
Researchers sent different messages about antibiotic prescribing guidelines to
248 registered clinicians about antibiotic prescription guidelines. The most
effective message was one that compared their antibiotic prescribing rates with
those of "top performers" (those with the lowest inappropriate prescribing
rates). See [_Effect of Behavioral Interventions on Inappropriate Antibiotic
Prescribing Among Primary Care Practices: A Randomized Clinical Trial_ by Meeker
_at al_, 2016, in the _Journal of the American Medical
Association_](https://jamanetwork.com/journals/jama/fullarticle/2488307).

Universities want their students to behave in a more inclusive manner towards
marginalized groups. Researchers conducted six randomized controlled trials at a
large public university in the United States, and tried several "interventions"
that targeted participants perception of social norms (i.e., what are acceptable
ways of behaviour towards marginalized groups). The interventions that worked
best simply communicated to non-marginalized students that their peers hold
pro-diversity attitudes and engaged in inclusive behaviours. What worked less
well were interventions that tried to raise awareness about implicit biases, or
how subtle discriminations are widespread. See [_Exposure to peers’
pro-diversity attitudes increases inclusion and reduces the achievement gap_ by
Murrar, Campbell & Brauer, 2020, in _Nature Human Behavior_](https://www.nature.com/articles/s41562-020-0899-5).

Researchers studied what encourages employees to increase knowledge sharing
more: seeing their (unit) managers share information, or their peers? Their
conclusion was that employees are more likely to engage in information sharing
if they see it modeled by fellow coworkers than by managers. See [_Managers
versus co-workers as referents: Comparing social influence effects on within-
and outside-subsidiary knowledge sharing_ by Boh and Wong, 2015, in
_Organizational Behavior and Human Decision
Processes_](https://www.sciencedirect.com/science/article/abs/pii/S0749597814000739)

### Social Proof can be Mispurposed

The force of social proof can be mispurposed. If we try to mobilize people
against an undesirable activity, pointing out that it is regrettably frequent,
the message can backfire: it can _increase_ the frequency of the underirable
activity.

> Within the statement “Many people are doing this undesirable thing” lurks the powerful and undercutting normative message “Many people are doing this.” -- Cialdini, 2003

Despite a guard force of seven National Park Service rangers, fences, warning
signs, and the threat of a $325 fine, an estimated 11 tons of the fossil wood is
stolen from the [Petrified Forest National
Park](https://en.wikipedia.org/wiki/Petrified_Forest_National_Park) every year.
The percentage of visitors who do so is small (less than 3%) but since the park
receives a large number of visitors, the theft adds up. Researchers conducted an
experiment in which they alternated a pair of signs in high-theft areas of the
park. The first sign urged visitors to not take the fossil wood, with a picture
depicting three thieves in action. It nearly tripled theft, to 7.92% of
visitors. The second sign also urged visitors not to take the fossil wood, but
had a picture depicting a lone thief. This reduced theft to 1.67%. See
[_Crafting Normative Messages to Protect the Environment_ by Cialdini, 2003, in
_Current Directions in Psychological
Science_](https://journals.sagepub.com/doi/10.1111/1467-8721.01242).

When the IRS announced that, because so many citizens were cheating on their
returns, the agency was going to strengthen penalties for tax evasion, tax fraud
went up the following year. See [_Social Influence, Social Meaning, and
Deterrence_ by Kahan, 1997 in _Virginia Law
Review_](https://www.ojp.gov/ncjrs/virtual-library/abstracts/social-influence-social-meaning-and-deterrence).

### Social Proof of the Future

Rather than relying only on evidence of existing social proof, a communicator
can do at least as well by relying on evidence of future social proof.

Because we assume they will continue in the same direction, trends don’t just
tell us where others’ behaviors have been and are now; we think they also tell
us where others’ behaviors will be. Thus, trends give us access to a special and
potent form of social proof—future social proof.

When informed that only a minority performs one of these desired actions, people
are reluctant to perform it themselves. However, if they learn that within the
minority, more and more others are engaging in it, they jump on the bandwagon
and begin enacting the behavior too.

Researchers invited university students to participate in an experiment,
ostensibly about consumer-preference of a new brand of toothpaste. The real goal
was to study the impact of different kinds of messages on their water
conservation. The control group was told nothing about water conservation. The
first test group was given information indicating that only a minority of their
peers conserved water at home. The second test group was given information that
while only a minority of their peers conserved water, the percentage of the
minority was increasing recently. All students were asked to rate the toothpaste
after brushing their teeth over a sink in a laboratory. Unknown to them, the
sink had a water consumption meter attached to it. Compared to the control
group, the first test group students used _more_ water. The second test group
used the least water. See [_Trending Norms: A Lever for Encouraging Behaviors
Performed by the Minority_ by Mortensen _et al_, 2017, in _Social Psychological
and Personality
Science_](https://journals.sagepub.com/doi/abs/10.1177/1948550617734615).
