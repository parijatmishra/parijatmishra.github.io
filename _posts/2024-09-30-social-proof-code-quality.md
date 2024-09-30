---
layout: post
title: The Social Psychology of Secure Software
---

Security breaches are no fun. There's much advice about how to improve
cybersecurity that boils down to: products, processes and priorities. No one
talks about _psychology_. Now, what on earth does psychology have to do with
cybersecurity?

Organizations are spending a lot of money on security products, to the tune of
hundreds of billions of dollars. This spend is growing faster than the average
growth in IT spend. [^idc-2023] Yet, losses due to cybercrime are growing even
faster, to the tune of tens of trillions of dollars. [^statista-2024]

Will increased security spending stop this trend? The Director of CISA doesn’t
think so. In her keynote at the mWISE Conference 2024, she stated:

> **We don’t need more security products — we need more secure products.**
> Technology vendors are building problems into their products, opening doors
> for attackers.” [^reg-cisa]

How can technology vendors stop "building problems into their products"? Much
has been written about how to get development teams to write secure software.
Most suggestions boil down to:

- Educating developers on secure coding.
- Automating security issue detection with mandatory quality thresholds.
- Elevating security as a CxO priority, at par with cost and speed of software
  delivery.

What is not written about much is that developing software is a social activity
and _social psychology_ of developers when they write code. Without
understanding that, tools, processes, education and prioritization will not make
software secure, because developers won't have been co-opted in that pursuit.

## Secure Software is Quality Software

According to NIST, 65% of reported security vulnerabilities were due to
"avoidable, ordinary programming errors", aka bugs. [^nist-2018]

That means we can reduce security risks by nearly two-thirds simply by
eliminating bugs!

What about the other 35% of issues? They'd be more subtle interactions between
pieces of code or even different programs, where an individual piece of code
does not have an obvious bug. To address those, we need a combination of:

1. Buying tools to automatically run static and dynamic security tests on
   software for known security issues, and importantly train developers on how
   to use the output of these tools.
1. Hire security focused testers and researchers who look for issues that are
   less well-known and not checked for automatically.
1. Educate developers about the subtler aspects of security, e.g. correct use of
   cryptography, secure secret handling, nuances of authentication and
   authorization protocols, and least-privilege principles and techniques.

I am convinced that if your codebase is low-quality, that is, has a lot of
technical debt, you won't be able to eliminate simple programming errors or take
more advanced steps to improve security.

If your codebase has a lot of technical debt:

1. Making changes to code will introduce bugs inadvertently;
1. It will take longer and longer to make changes to the codebase safely;
1. Your developers will be so busy fighting deadlines and fixing inadvertent
   breakages that they won't have any time to think about security.

**You cannot make software secure without _first_ making the codebase high
quality.**

## How to Fail at Improving Quality

Long ago, I set out to improve the quality of my company's codebase. I failed,
miserably. Don't be me.

Early in my career, after many years of mostly solo coding, I got invited to a
startup as the first techie. I whipped up a prototype, we demoed, got funded,
and things got real. I hired a small squad of geniuses, all smarter than me, and
we built an MVP.

We got some initial success. We added new team members. We added features almost
as quickly as we could imagine them. Our codebase grew quickly, and admittedly
somewhat haphazardly. After a while, the codebase started feeling as fragile as
a Jenga tower: new features would take forever, and surprise bugs kept crashing
the release party. I took a critical look at the monster I had helped create. 

I found that the quality of our codebase was in the dumps. My team was not at
fault: I was an equal contributor to the rot. Some code was so inscrutable that
it might as well have been encrypted. Rare was the comment that explained what
the code did. Some functions were so long that they would qualify as a PhD
thesis. Bugs got through because test coverage was inadequate. When we doubled
down on writing tests, we found it hard to do so because much of the codebase
was so convoluted that finding all the test scenarios was a major undertaking,
and disheartening. 

I had to rally the team to save the codebase before it toppled over! I tried a
few things, roughly in this order:

1. *Exhortations.* I called a team meeting, explained the problem, and showed
   some examples of problematic code. The team agreed and decided to do better.
   *Result.* Squat. Nothing changed. *Lesson*: Good intentions don't work; you
   need mechanisms. [^intentions-mechanisms].

1. *Leading by Example.* I took up a complex feature, wrote the best code I
   could, documented it well with beautiful comments, and smothered the code
   with tests. The team agreed this should be the gold standard. *Result*.
   Diddly-squat. Nothing changed, just faster. *Lesson*: People don't value
   examples of behaviour from those unlike them very highly. [^mgr-vs-emp]

1. *Authority.* A senior engineer discovered <a
   href="https://www.sonarsource.com/products/sonarqube/"
   target="_blank">SonarQube</a>, a code analysis and quality reporting tool. He
   added it to our build process and showed its reports to the team. We liked
   it. I told the team to look at what SonarQube reported after every build, and
   fix the issues promptly. I started reviewing the reports in our regular team
   meetings. *Result.* Code quality crept up, as long as I was reviewing the
   reports. I could not review the reports for a few weeks due to a crisis and
   some crunch-time. When I went back to take a look, quality had gone down to
   original levels, presumably because the developers had decided the reports
   were no longer important to me, and therefore to them. *Lesson*: Authority
   doesn't translate into a self-sustaining movement.

1. *Simplistic Metrics.* Desperate, I proposed I'll track bug count per
   developer, hinting it might influence performance reviews. The team *hated*
   my proposal, and I beat a hasty retreat. Still, some junior developers began
   avoiding work that would involve the gnarlier parts of the codebase, to avoid
   inadvertently introducing bugs. I had to hold several 1:1s to rebuild their
   trust. *Result*: The damage to morale was so bad that "squat" felt like
   progress. *Lesson*: Avoid overly simplistic performance metrics, especially
   for measuring people. [^perf-pitfalls]

At some point, I could not sustain the effort, and gave up. We did ship a
product and grew the userbase to millions. Still, every new feature added was an
uphill struggle. It was... unpleasant.

Over time, I learnt more about human behaviour and did better at improving
quality. I want to share some principles and techniques with you.

## Principle: Social Proof

Social Proof is a discovery in social psychology: _people use the actions of
others to decide how to behave, especially when they view those others as
similar to themselves._

This is a very robust finding, backed by a lot of research. Some examples
follow.

1. A brewery-pub in London started placing a sign on the bar stating,
   truthfully, that its most popular beer that week was its porter; porter sales
   doubled almost immediately. [^choice-factory]

1. A restaurant chain partnered with researchers to boost sales of certain menu
   items. Instead of lowering prices or adding expensive ingredients, they
   simply labeled dishes as “most popular.” Sales jumped 13-20%. Other labels
   like "House Specialty" or "Chef's Recommendation" had little to no effect.
   Turns out, people love what’s already popular—an easy, ethical, and cost-free
   solution! [^resto-menu-pop]

1. Dutch high school students increased fruit consumption by 35 percent, when
   told their peers eat fruit to keep healthy, even though they had claimed no
   intention to change upon receiving the information. [^students-fruits]

1. During the COVID-19 outbreak, researchers studied the reasons Japanese
   citizens chose to wear face masks: only one reason made a major difference in
   mask-wearing frequency: seeing other people wearing masks. [^japan-covid]

1. Researchers sent messages to households in San Marcos, California, asking
   them to conserve energy. There were four variants: "The environment will
   benefit"; "It's the socially responsible thing to do"; "It will save you
   significant money on your next power bill"; and finally the _social proof_
   message "Most of your fellow community residents do try to conserve energy at
   home." The households getting the social-proof message saved 3.5 times as
   much energy as those getting any of the other messages. [^fornara-energy]

1. In a further twist, in the energy conservation study above, there were two
   control groups in the study. Group A got no message about conserving energy
   at all. Group B got a message simply urging them to save energy. The
   difference between the two control groups was negligible, showing that simple
   exhortatons don't work.

The science is clear. People react strongly to the message "others are doing
it", and very little to other messages like "you should do it", "it is good for
you", "it is good for the world", etc.

**Causes.** Why does this happen? One explanation is that humans find it harder
to defy other humans than impersonal information. A second one is that knowing
many others are doing something makes people believe that the thing is feasible
for them too.

1. Researchers found that participants were less likely to conform to
   information from computers than from humans, even when they rated both as
   equally reliable. FMRI scans showed that defying humans activated the brain's
   negative emotion center (the amygdala), causing what researchers called "the
   pain of independence." Defying computers didn’t trigger the same emotional
   response, as there were no social consequences. [^neuro-conformity-1],
   [^neuro-conformity-2]

1. Researchers studied households' willingness to recycle waste when given
   different reasons to do so, in the Italian cities of Rome, Cagliari, Terni,
   and Macomer. They concluded that households were most willing to recycle if
   they believed that _many_ of their neighbours recycled at home, in part
   because they saw recycling as less difficult to manage. [^feasibility-1]

**Similarity.** This effect is stronger when the perception is
that the others are people like them and weaker if they are different, somehow.
Sometimes, only the message "other people _like you_ are doing it" works.

1. Some physicians routinely overprescribe some medicines, such as antibiotics.
   Of the several attempts to get them to change their behavior, only one method
   brought about lasting change: comparison of their presription rates to peers.
   Researchers sent different messages about antibiotic prescribing guidelines
   to 248 registered clinicians about antibiotic prescription guidelines. The
   most effective message was one that compared their antibiotic prescribing
   rates with those of "top performers" (those with the lowest inappropriate
   prescribing rates). [^physician-overprescription]

1. Universities want their students to behave in a more inclusive manner towards
   marginalized groups. Researchers conducted six randomized controlled trials
   at a large public university in the United States, and tried several
   "interventions" that targeted participants perception of social norms (i.e.,
   what are acceptable ways of behaviour towards marginalized groups). The
   interventions that worked best simply communicated to non-marginalized
   students that their peers hold pro-diversity attitudes and engaged in
   inclusive behaviours. What worked less well were interventions that tried to
   raise awareness about implicit biases, or how subtle discriminations are
   widespread. [^uni-diversity]

1. Researchers found that employees are more likely to engage in information
   sharing if they saw this behaviour modeled by fellow coworkers rather than by
   managers. [^mgr-vs-emp]

**Backfiring.** When informed that only a minority performs one of a
desired action, people are reluctant to perform it themselves. If we implore
people to stop doing something bad and let it slip that regrettably many others
_are_ doing that bad thing, we might increase the undesirable behaviour. This
finding is also robustly supported by research and obervation.

1. Despite guards, fences, warning signs, and the threat of fines, about 2.95%
   of visitors steal an estimated 11 tons of fossil wood every year from the <a
   href="https://en.wikipedia.org/wiki/Petrified_Forest_National_Park"
   target="_blank">Petrified Forest National Park</a>. Researchers conducted an
   experiment in which they alternated a pair of signs in high-theft areas of
   the park. The first sign urged visitors to not take the fossil wood, with a
   picture depicting three thieves in action. It nearly tripled theft, to 7.92%
   of visitors. The second sign also urged visitors not to take the fossil wood,
   but had a picture depicting a lone thief. This reduced theft to 1.67%.
   [^petrified-forest-theft]

1. The US IRS announced that many citizens were cheating on their returns, so
   the agency was going to strengthen penalties for tax evasion. Tax fraud went
   *up* the following year. [^irs-tax]  There are innumerable examples of public
   service announcements that deplored bad behaviour and asked people to improve
   have failed to have a positive impact and in fact increased the undesirable
   behaviour.

**Social proof of the future.** The "trend continuation" cognitive bias is
another quirk of human cognitiion, where when people see a change or trend, they
expect the change or trend to continue. Suppose we cannot truthfully say that
many others are doing something. We might be able to say something about the
trend. Because we assume they will continue in the same direction, trends make
us think about where others’ behaviors _will be_. Thus, trends give us access to
_future_ social proof.

1. To study the effects of different messages on water conservation, researchers
   invited university students to participate in a study, where they asked them
   to brush their teeth with a "new" toothpaste over a sink in the lab and rate
   the toothpaste. the  The sink was equipped with a hidden water consumption
   meter. Before the "test", students were made to wait their turn and given
   some liteture to read. The control group read nothing about water
   conservation. The first test group read that only a _minority_ of their peers
   conserved water; this group used _more_ water than the control group! The
   second group read the same thing, but also that this minority was growing.
   This group used the _least_ water. [^trending-norms]

## Software Development is a Social Activity

Programming looks like something done in isolation. A developer puts on her
headphones, picks up a task from the company's tracking system, and starts
coding. No one would call this "social". However, when coding, the developer is
having a conversation, not in real-time, but asynchronously, with the rest of he
organization. New code almost always interacts with existing code---the quality
and style of the that code is informing and affecting the developer's own
actions. The developer's code may change existing code---the developer makes
decisions about where and how much. The developer's code will often be used by
others in the future---what is the right trade-off between readability and
performance?

When a developer picks up a problem to solve, she makes many trade-offs where
they must use intuition aka "gut feel". When should a long function be
refactored? What is the right approach when encountering a novel problem: (a)
research the problem and all potential solutions thoroughly until she
understands them well, regardless of how much time it takes, and selecting a
solution; (b) research as before, but timebox the effort, and make the best
possible decision based on whatever was learnt in that time; (c) or, search for
solutions and just use the first one that seems likely to work.

**Software development is a collaborative effort, done under uncertainty. The
principle of social proof affects the decisions developers are making. It can be
used to encourage good behaviour, or it might encourage bad behaviour.**


## Use Social Proof to Improve Software Quality Sustainably

To improve software quality, one must of course start with the basics: (1)
explain why, (2) get some tools to automate what we can---like static code
analysis; (3) provide training and make the tools easy to use; (4) add some
checks, like a go/no-go checkpoint in your CI/CD pipeline.

This is not enough. It is very likely that developers will do the bare minimum
to get through the process. The organization will need to make a large
investment in risk and compliance to keep quality up.

There is a better way. We can co-opt the principle of _social proof_ to motivate
developers and teams across the organization to improve code proactively and
reinforce good practices.

After doing the basics, ensure that there is a standard measure of quality
across teams. Establish team-level reviews, where the quality of code owned by
the team is reviewed. Ensure the chosen tool or dashboard is capable of showing
metrics for a given team but also for other teams and overall organization.

Initially, authority and inspection are needed to get some positive
improvements. Code quality will creep up, with some effort. Find one or two
teams that are making progress.

To the teams not making progress, point out the ones that are. Emphasize that
while the teams making quality improvements are in a minority right now, the
number of such teams is growing.

At some point, enough teams would be engaged such that a lot of code is now high
quality. You can now switch to the message that a majority of teams keep code
quality high while meeting their deadlines.

Watch the laggard teams absorb and internalize this information, and change.

For even better results, create forums where developers and teams can ask the
high performers "how did you do that!?", and watch your development organization
teach itself how to balance speed and quality well.

## References

[^idc-2023]: [Double-Digit Revenue Growth for Security Products in 2023 is Forecast to Continue Through 2028, According to IDC](https://www.idc.com/getdoc.jsp?containerId=prUS52392924)

[^statista-2024]: [Statista: Cybercrime Expected To Skyrocket in Coming Years](https://www.statista.com/chart/28878/expected-cost-of-cybercrime-until-2027/)

[^reg-cisa]: [CISA Boss: Makers of insecure software must stop enabling today's cyber villains](https://www.theregister.com/2024/09/20/cisa_software_cybercrime_villains/).

[^nist-2018]: See [NIST: What Proportion of Vulnerabilities can be Attributed to Ordinary Coding Errors](https://tsapps.nist.gov/publication/get_pdf.cfm?pub_id=925468)

[^intentions-mechanisms]: Jeff Bezos, founder of Amazon---observed that asking
    people to try harder doesn't solve recurring problems. People are _already_
    doing their best. They have good intentions. At best, people will put in
    extra hours and heroically rescue a bad situation. The solution is a change
    to the system that is preventing people from solving the problem
    permanently. He coined the term "mechanism" to describe the criteria for
    acceptable solutions. To learn more, see: (1) [AWS Well Architected
    Framework: Operational Readiness Review: Building
    mechanisms](https://docs.aws.amazon.com/wellarchitected/latest/operational-readiness-reviews/building-mechanisms.html).
    (2) [How we leverage mechanisms at Amazon? - Zak Islam, Director of
    Engineering at AWS](https://www.youtube.com/watch?v=rIxFHQJhJ2Y).

[^perf-pitfalls]: KPIs, OKRs, quantitative metrics, targets, and other
    quantitative metrics are powerful tools, but when applied to knowledge work
    requiring high judgment, they can easily cause lasting and deep damage. The
    key is to use them _judiciously_. I wrote at length about this topic in a
    [previous article]({% post_url
    2021-05-26-avoiding-pitfalls-metrics-performance %}).

[^choice-factory]: See [_The Choice Factory: 25 behavioural biases that
    influence what we buy_ by Richard Shotton,
    2018.](https://www.amazon.sg/Choice-Factory-behavioural-biases-influence/dp/085719609X).

[^resto-menu-pop]: See [_"Observational Learning: Evidence from a Randomized
    Natural Field Experiment_ by Cai _et al_, 2009 in _American Economic
    Review_](https://www.aeaweb.org/articles?id=10.1257/aer.99.3.864).

[^students-fruits]: See [_Don't tell me what I should do, but what others do:
    the influence of descriptive and injunctive peer norms on fruit consumption
    in adolescents_ by Stok FM, et al, 2014, in _National Library of Medicine_,
    National Institutes of Health](https://pubmed.ncbi.nlm.nih.gov/23406475/).

[^japan-covid]: See [_Why Do Japanese People Use Masks Against COVID-19_ by
    Nakayachi _et al_, 2020, in _Frontiers in
    Psychology_](https://www.frontiersin.org/journals/psychology/articles/10.3389/fpsyg.2020.01918/full).

[^fornara-energy]: See [_Normative social influence is underdetected_ by Nolan
    _et al_, 2008, in _Peronality and Social Psychology
    Bulletin_](https://pubmed.ncbi.nlm.nih.gov/18550863/).

[^physician-overprescription]:  See [_Effect of Behavioral Interventions on
    Inappropriate Antibiotic Prescribing Among Primary Care Practices: A
    Randomized Clinical Trial_ by Meeker _at al_, 2016, in the _Journal of the
    American Medical
    Association_](https://jamanetwork.com/journals/jama/fullarticle/2488307).

[^uni-diversity]: See [_Exposure to peers’ pro-diversity attitudes increases
    inclusion and reduces the achievement gap_ by Murrar, Campbell & Brauer, 2020,
    in _Nature Human Behavior_](https://www.nature.com/articles/s41562-020-0899-5).

[^mgr-vs-emp]: See [_Managers versus co-workers as referents: Comparing social
    influence effects on within- and outside-subsidiary knowledge sharing_ by
    Boh and Wong, 2015, in _Organizational Behavior and Human Decision
    Processes_](https://www.sciencedirect.com/science/article/abs/pii/S0749597814000739)

[^neuro-conformity-1]: See [_Neurobiological correlates of social conformity and
    independence during mental rotation_ by Berns _et al_, 2005, in _Biological
    Psychiatry_](https://pubmed.ncbi.nlm.nih.gov/15978553/)

[^neuro-conformity-2]: See [_Neuroscience
    and the social origins of moral behavior: How neural underpinnings of social
    categorization and conformity affect everyday moral and immoral behavior_ by
    Ellemers & van Nunspeet, 2020, in _Current Directions in Psychological
    Science_](https://psycnet.apa.org/record/2020-75764-013).

[^feasibility-1]: See [_Distinguishing the sources of normative influence on
    proenvironmental behaviors: The role of local norms in household waste
    recycling_ by Fornara _et al_, 2011, in _Group Processes & Intergroup
    Relations_](https://journals.sagepub.com/doi/10.1177/1368430211408149).

[^irs-tax]: See [_Social Influence, Social Meaning, and Deterrence_ by Kahan,
    1997 in _Virginia Law
    Review_](https://www.ojp.gov/ncjrs/virtual-library/abstracts/social-influence-social-meaning-and-deterrence).

[^petrified-forest-theft]: See [_Crafting Normative Messages to Protect the
    Environment_ by Cialdini, 2003, in _Current Directions in Psychological
    Science_](https://journals.sagepub.com/doi/10.1111/1467-8721.01242).

[^trending-norms]: See [_Trending Norms: A Lever for Encouraging Behaviors
    Performed by the Minority_ by Mortensen _et al_, 2017, in _Social
    Psychological and Personality
    Science_](https://journals.sagepub.com/doi/abs/10.1177/1948550617734615).
