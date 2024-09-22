---
layout: post
title: Improve Code Quality Using Social Proof
---

bla bla [good intentions don't work](#good-intentions-dont-work)

## Random thoughts

**Goal**: I want to demonstrate that using SQ EE portfolios is the best way to increase
code quality in an enterprise.

**Takeaway**: The portfolios feature of SQEE / SCE is the best way to get teams to benchmark against each other.

**Why**: Sets social norms. You improve one/two teams, rest will follow.

**Audience**: those with SQ CE/DE licenses and reluctant to buy SQ EE.

**Story**: Improving code quality across an org is not simple because:

- Telling devs to improve code quality doesn't work
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

Jeff Bezos---founder and long-time CEO of Amazon---observed that the
exhortations "do better" or "try harder" don't solve recurring problems. People
are _already_ doing their best. At best, people will pull in extra hours and
heroically rescue a bad situation. Ask them to do this too often, and your best
get burnt out and the remaining become cynical.

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
Randomized Natural Field Experiment_ by Cai _et al_, 2009, American Economic
Review](https://www.aeaweb.org/articles?id=10.1257/aer.99.3.864).

A brewery-pub in London started placing a sign on the bar stating, truthfully,
that its most popular beer that week was its porter. Porter sales doubled almost
immediately. See [_The Choice Factory: 25 behavioural biases that influence what
we buy_ by Richard Shotton,
2018.](https://www.amazon.sg/Choice-Factory-behavioural-biases-influence/dp/085719609X).

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

Researchers studied what encourages employees to increase knowledge sharing
more: seeing their (unit) managers share information, or their peers? Their
conclusion was that employees are more likely to engage in information sharing
if they see it modeled by fellow coworkers than by managers. See [_Managers
versus co-workers as referents: Comparing social influence effects on within-
and outside-subsidiary knowledge sharing_ by Boh and Wong, 2015, in
_Organizational Behavior and Human Decision
Processes_](https://www.sciencedirect.com/science/article/abs/pii/S0749597814000739)

Physicians who overprescribe certain drugs, such as antibiotics, are unlikely to
change this behavior in a lasting fashion unless informed that their
prescription rate exceeds the norm of their peers. Researchers sent different
messages about antibiotic prescribing guidelines to 248 participants (who were
all registered clinicians, i.e., qualified doctors) about antibiotic
prescription guidelines. The most effective message was emails to clinicians
that compared their antibiotic prescribing rates with those of "top performers"
(those with the lowest inappropriate prescribing rates). See [_Effect of
Behavioral Interventions on Inappropriate Antibiotic Prescribing Among Primary
Care Practices: A Randomized Clinical Trial_ by Meeker _at al_, 2016, in the
_Journal of the American Medical
Association_](https://jamanetwork.com/journals/jama/fullarticle/2488307).


### Emphasizing What?
- rate of change?
- small percentage of delinquets
- outsize impace?



within the lament “Look at all the people who are doing this undesirable thing” lurks the undercutting message “Look at all the people who are doing it.”

