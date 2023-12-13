# Intersect Open Source Governance Policy

## Meta 

### Terminology

Each of these terms is defined in their respective sections, but we will want to talk about them in examples before they are defined.

* Project: a software project, one or more source repositories with a given set of committers
* Meta-project: a grouping of projects
* Technical Steering Committee (TSC): The Intersect committee that is responsible for the technical governance of Intersect projects
* Open Source Committee (OSC): The Intersect committee that is responsible for the open-source practices of Intersect projects
* Project Management Committee (PMC): the committee that governs a project
* Technical Oversight Committee (TOC): a delegated sub-committee of the TSC responsible for oversight of a particular project area

### Goals and Principles

This policy is principles-based. 
That means that the primary content of the policy is the set of goals and principles, and the rest of the policy attempts to describe how to follow them. 
However, the principles are the important part - if there are disagreements about the policy then they will ultimately be resolved by appeal to the principles. 
This provides a guide to action: if the policy is unclear or misguided, act in accordance with the principles.

The goals of this policy are those stated in the Open Source Committee Charter. 
Briefly re-stated, those are:

1. Legitimacy: maintaining the legitimacy of the Intersect projects in the eyes of the community
2. Quality: maintaining the quality of the Intersect projects
3. Sustainability: ensuring that the Intersect projects continue in a healthy fashion
4. Citizenship: being good open-source citizens

The principles are:

1. Merit: authority and voice should derive primarily from merit
2. Transparency: decisions and discussions should be public and transparent
3. Delegation: decisions should be made at the lowest level possible

### Following this policy

Because the heart of this policy is the principles, and in accordance with the principle of Delegation, projects and people working for Intersect are free to deviate from this policy, provided that they have a good reason and this action is in accordance with the principles. 
This policy aims to provide a sensible default.

Similarly, projects and people are encouraged to augment the policy if they think it appropriate.

There are a few exceptions, and these are indicated by the use of "must".
Policies stated with "must" are mostly non-negotiable, unless there is a very good reason.

<details>
<summary><b>Examples</b></summary>

* The PMC for a meta-project wants to give the person acting as release manager a veto on votes to perform a release.
   * This is perfectly logical and a good way to help ensure the quality of the release.
   * This is assuming that the release manager has merit - if they are simply posted into that role by a company, then it is much less clear that they have sufficient merit to deserve to be able to block a release.
* The PMC for a meta-project wants to form a group of technical experts to do design review for proposals.
   * This is again reasonable and a good way to make it easier for contributors to make substantial changes and be confident that their proposals will be accepted.
   * Again, the members of the group should be meritorious, and the selection process should reflect that.
* The PMC for a project wants to require reviews from specific experts on changes to certain parts of the codebase, using CODEOWNERS or otherwise.
   * This is good practice, and so long as appropriately meritorious reviewers are being chosen it should work well. 
   * This is a particularly sensible policy for large projects where individuals may prove themselves worthy of being a Committer, but only on certain parts of the codebase. The Committer role is too binary to accommodate this, so it is sensible to add a mechanism like CODEOWNERS on top.
* The PMC wants to give Maintainers veto rights on PRs.
   * This is fine: if a project wants to have more powerful Maintainers that’s not bad _a priori_.
   * Care should be taken that the Maintainers are not then more powerful than their Merit, and more scrutiny should be applied to giving people the role.
   * If this is part of a move towards increased centralization of authority then it might be bad from a Sustainability perspective.
* The PMC wants to use a communication channel that meets the requirements, but is different from the channel used by most other projects.
   * Having non-standard “interfaces” makes the project harder to work with, and makes it harder for contributors to know how to interact with it, so this is mildly damaging to Sustainability. It may nonetheless be a good decision if there are other reasons to do it.
* The PMC wants to elect a “Benevolent Dictator For Life” (BDFL) and then have them make final decisions without recourse to the TSC.
   * This is problematic: without the TSC as part of the escalation chain we cannot be sure that we maintain the Legitimacy of the project. Having a BDFL is also bad for Merit (in the future other contributors may be more meritorious) and Sustainability (better to have a wider set of competent contributors)

</details>

## Decision-making

Decision making should generally be done in a consensus-seeking manner. 
That is, decisions should be made by consensus, and only if that fails is a more structured method used.

The general decision-making process is:

1. Lazy consensus: just act based on what you think people will want. If nobody objects then everything is fine.
2. Consensus-building: seek indications of consensus from the relevant group
   1. Voting: the relevant group votes explicitly (this is an example of consensus-building since it aims to get the group to come to a more explicit consensus)
3. Escalation: the issue is raised to a higher decision-making body

<details>
<summary><b>Rationale</b></summary>

Consensus-seeking decision-making lets us mostly use the consensus-based methods that are common in open-source projects, which tend to operate smoothly and with low overhead the majority of the time. 
But in cases where consensus cannot be found, or where there are fundamental conflicts with the principles, we have an explicit escalation path that allows us to still make decisions.

</details>

<details>
<summary><b>Examples</b></summary>

* An established committer makes a PR, and…
   * Merges it themselves
      * For uncontroversial things, using lazy consensus like this is fine. This does require people to use their judgement about what things are likely to be controversial and so need more discussion.
      * Projects may well want to add additional guidelines saying that people should not do this, or should require a review before merging. That’s also fine.
   * Gets a review from a fellow committer before merging
      * This is generally a good idea. This is also a small example of consensus-building by seeking input from another contributor on whether the idea is good or not.
   * Brings it to the PMC meeting for discussion before merging
      * This is a good idea if the contributor feels unsure about whether the change is going to be agreeable or not. Discussion might also happen on other communications channels.

</details>

### Voting

Voting is a simple way to build consensus, by asking each member of the group to explicitly state their preference.

The standard voting process is for every voter to issue one of the following votes: 

* +1: positive vote
* 0: abstention
* -1: negative vote

Normally, a majority should be sufficient to decide in favour of a motion, but in some circumstances it may be appropriate to treat any negative vote as a veto. 
This is because the point is to elicit a group consensus: if the vote does not seem like enough for the group to settle on the outcome, then it may be necessary to escalate.

<details>
<summary><b>Rationale</b></summary>

Voting is a standard and easy way of building consensus.
It is also flexible: it can be used to make a hard decision, or just used as way of gauging consensus.

</details>

<details>
<summary><b>Examples</b></summary>

* A project wants to adopt an auto-formatter. Much discussion is had and there is no consensus, but nobody is going to be that put out by not getting their favourite outcome, so the PMC just votes and takes the majority option.
* The PMC votes on whether to accept a controversial patch. There is a majority, but several of the most knowledgeable committers vote against, citing security concerns. The PMC does not feel like they have consensus despite the majority and decides to escalate.

</details>

### Escalating issues

Issues that a group cannot resolve themselves should be escalated so that we can continue to make progress. 
These can be technical problems, social problems, or conflicts between principles.

The default escalation pathway is:

1. The Project Management Committee
2. The meta-project Project Management Committee, if there is one
3. A relevant Technical Oversight Committee, if there is one
4. The Technical Steering Committee

Anyone can escalate an issue. 
Issues raised by Committers should be considered by the relevant body, issues raised by other people may be considered at the discretion of that body. 

<details>
<summary><b>Rationale</b></summary>

In order to maintain Legitimacy, projects *must* remain accountable to the Technical Steering Committee (TSC).
That means that the TSC has to operate as the final decision-making body also for disputes.
But the TSC cannot arbitrate everything, so we have to have a sensible chain of decision-making bodies between an individual contributor and the TSC.

</details>

<details>
<summary><b>Examples</b></summary>

* Two contributors disagree about whether a patch should be accepted or not.
   * This may just be a simple disagreement that should be escalated to the PMC, but might go further than that depending on how tricky the issue is.
* A contributor makes a significant contribution, which is rejected by the PMC for not being good enough quality. The contributor thinks that this is incorrect, and it is good enough. They appeal to the relevant TOC.
   * This is a more serious problem. They might also want to appeal to the OSC if they think the PMC is actually behaving badly, not just mistakenly.
* There is a proposal to implement a CIP that was accepted and planned for by the TSC. A highly respected contributor believes that there is a problem with the proposal and refuses to accept it.
   * This is a conflict between Legitimacy and Quality
* Security issues are sensitive, and so must not be disclosed publicly
   * This is a conflict between Quality/Sustainability and Transparency
* A well-regarded contributor is a member of the PMC but consistently behaves badly
   * This is a conflict between Merit and Sustainability

</details>

## Projects

A project is the unit of organization of software development at Intersect. 
A project is organized around some number of source code repositories and the people who work on them. 
Every source code repository in the Intersect organization must be owned by a project.

A project is governed by a committee of its committers, the Project Management Committee (PMC).

A project can have multiple repositories, but it is assumed that the set of committers is the same across all of them. 
This keeps things simpler since governance participation is tied to commit access.

### Project Management Committee

The PMC is a committee of the Committers of the project. 
The PMC is responsible for making project-level decisions and electing Committers.

The PMC has two administrative roles associated with it, the Chair and the Secretary. 
The Chair is responsible for organizing and running meetings, and the Secretary for keeping written material in order. 
The Chair and the Secretary are elected by the PMC. The Chair and the Secretary need not be Committers. 
If there is no Chair or the PMC is failing to appoint a Chair, then Intersect may appoint an interim Chair.

PMC meetings should be held regularly, be public, and be advertised on the public communications channel. 
Committers have a right to speak, others may be allowed to speak at the discretion of the Chair.

The PMC should make decisions in the usual consensus-seeking manner. 
If it needs to vote, the Committers are the voters. 
Votes should be held via the public communications channel to ensure that Committers are notified.

### Roles

Roles are per-project. 
All roles are non-exclusive, an individual may hold any number of roles.

The role assignments for a project should be listed in a discoverable way. 
For the roles which are associated with membership of a GitHub Team, it is enough to say that the team exists.

#### Development

There are three primary roles associated with doing development work.

1. Contributors are anyone who contributes to the project in any way. There is no formal requirement to be a contributor, but it is useful to have a way to refer to them.
2. Committers are people who have been given commit access to the project. Committers are also required to participate in the project governance process - the two go together.
3. Maintainers are individuals who have contributed in a sustained and substantial way to the project, and who commit to keeping the project healthy. Maintainers mostly have additional responsibilities and little additional power. They are likely to be influential, but this is because influential people should be made Maintainers, rather than vice versa.

<details>
<summary><b>Rationale</b></summary>

* Maintainers
   * We know there are likely to be paid maintainers, it is helpful to recognize this in some official way.
   * The Maintainer role exists primarily as an honorary one. This gives us a way to recognize the people who are in practice giving lots of time and attention to maintenance (and likely being paid for it).
   * The Maintainer role doesn’t come with powers: individuals should be influential in proportion to merit anyway.
* Project leads
   * We do not have a concept of a single project lead. 
      * In the future we will hopefully have many groups of contributors, all of whose voices should be heard. This is somewhat incompatible with having a single nominated project lead.
      * We could have elected project leads. However, this adds a possibly-unnecessary additional power structure, and we have to define what their powers are.
   * This does not mean that there may not be more traditional team structures associated with the project contributors. 
      * For example, IOI may have a team working on `cardano-ledger` and that team will probably have a team lead and be organized in typical company fashion. But the IOI-appointed `cardano-ledger` team lead does not have any special status when it comes to making decisions for the `cardano-ledger` Intersect project.
      * As an example of how this works today, consider GHC. IOG has a GHC team, with an appointed team lead. But the IOG GHC lead doesn’t have any particular sway in the leadership of GHC-the-OSS-project, which is led by its major contributors and its BDFL. In practice, as a good contributor the IOG GH Clead does have some voice, especially in areas where he works a lot, but this is more about his history of contribution than the fact that he is the IOG GHC lead.

</details>

#### Administrative

There are two administrative roles associated with the PMC, Chair and Secretary, which are described in the PMC section.

Individuals may occasionally be given the Administrator role.
This is a very powerful role and should only be used for a few highly trusted staff at Intersect who can implement dangerous actions when necessary.

#### Role and Team Summary

| Role          | Rights                                                                                | Responsibilities                                                                                                         |                                                                                                                  |
|---------------|---------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| Contributor   | Open issues; attend PMC meetings; make code contributions                             |                                                                                                                          |                                                                                                                  |
| Committer     | As Contributor; speak at PMC meetings; member of `<project>-committers`               | Attend PMC meetings; vote on PMC motions                                                                                 |                                                                                                                  |
| Maintainer    | As Committer; member of `<project>-maintainers`; maintainer of `<project>-committers` | As Committer; ensure that pull requests and issues are reviewed in a timely fashion; maintain the health of the codebase |                                                                                                                  |
| Administrator | Member of `<project>-admins`; maintainer of all the `<project>-*` teams               | Should only take action when directed to by the appropriate authority.                                                   |                                                                                                                  |
| Chair         |                                                                                       | Organize PMC meetings; report on the PMC’s activities to Intersect                                                       |                                                                                                                  |
| Secretary     |                                                                                       |                                                                                                                          | Take minutes during PMC meetings; ensure that minutes are published publicly; send out votes and tally responses |
	

| GitHub Team             | Permissions                         | Notes                                                         |
|-------------------------|-------------------------------------|---------------------------------------------------------------|
| `<project>`             | Parent team for other project teams |                                                               |
| `<project>-committers`  | Write                               |                                                               |
| `<project>-maintainers` | Maintain                            |                                                               |
| `<project>-admins`      | Admin                               | Only appropriately vetted Intersect staff can be in this team |

### Communications

Projects should therefore have a primary public, durable, and asynchronous public channel. 
Meeting minutes and votes should be sent out on this channel. 
This *must* be on a standard Intersect platform (TBD).

Projects should also have a public, real-time chat channel for discussions. 
This *must* be on a standard Intersect platform (TBD).

Projects should also have another public and durable location for recording information about governance (e.g. project-specific policies), such as a wiki.

<details>
<summary><b>Rationale</b></summary>

Following the principle of Transparency and to enable voting, projects need to have a communication channel that is accessible and public. 
In order to ensure that discussion remains available for the long term, it should also be durable (i.e. no message expiry, ideally not reliant on ephemeral hosted or paid services).

It is quite beneficial for all the projects to use the same communications platforms.
This minimizes friction between projects, and makes it easier for people to know how to contact them.
That is why the choice of platform is specified as a "must".

</details>

## Meta-projects

A meta-project is a grouping of projects. 
Meta-projects exist to facilitate cross-project collaboration where that is necessary. 

<details>
<summary><b>Rationale</b></summary>

Intersect owns some large, complex projects such as Cardano, and so some framework for cross-project coordination and decision-making is essential.

</details>

<details>
<summary><b>Examples</b></summary>

* Project X has three dependencies Y, Z, and Q. In addition, there is project R which provides tools for deploying X, and some individuals who act as full-time release managers for X. In this instance it would be appropriate to form a meta-project to collect all of this work.

</details>

### Project Management Committee

A meta-project has a PMC, which functions similarly to a project PMC. 

The members of each sub-project should nominate a member of their PMC to be a member of the meta-project PMC. 
The meta-project should not otherwise elect PMC members.

A project joins a meta-project by its PMC requesting to join and the meta-project’s PMC accepting. 
A project can leave a meta-project if its PMC decides to do so. 

The meta-project PMC acts as the next step up in the escalation chain above the PMC of its sub-projects. 
Decisions made by the meta-project PMC are binding on the sub-projects (of course, they can leave the meta-project or escalate the issue).

### Technical Oversight Committees

A Technical Oversight Committee (TOC) is a sub-committee of th Technical Steering Committee (TSC) which is delegated to make decisions on a particular subject area as part of a meta-project.

The members of a TOC are appointed by the TSC.

A TOC should be associated with a meta-project; a meta-project may have multiple TOCs with different scopes. 

The meta-project PMC may escalate issues to a TOC as appropriate in lieu of escalating to the TSC.

<details>
<summary><b>Rationale</b></summary>

The Technical Steering Committee (TSC) is ultimately responsible for the technical direction of Intersect projects, and as such is the final point of escalation for issues.
However, the TSC may not be equipped to handle all such issues, either because it lacks expertise or simply because they require too much attention. 
In such situations the TSC can create a sub-committee to which it delegates this work. 
The particular case of delegating technical oversight over a particular topic area is common, so we describe it here. 

TOCs are particularly necessary for complex meta-projects like Cardano: we need a technically strong group of people who know what they’re talking about (probably several) to arbitrate difficult technical disagreements, review designs, etc.

TOCs are scoped to a meta-project mostly just to reduce clutter and have meta-projects as the top-level unit of organisation.

TOC members are appointed by the TSC because the TOC is operating as delegated representative of the TSC. Nonetheless, they should still be chosen following the principles, notably Merit.

</details>

<details>
<summary><b>Examples</b></summary>

* The Cardano project will probably need at least one TOC to handle cross-cutting design issues, decide on issues with CIPs that become apparent during implementation, etc.

</details>

### Communications

Meta-projects should follow the same communication policies as projects.

