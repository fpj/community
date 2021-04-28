# Pravega Project Governance
Pravega is an code repository organization hosted by CNCF comprising repositories supporting and forming an ecosystem for streaming data. All repositories under the Pravega organization are driven by the bylaws described in this document. This document covers the structure of the various groups that form Pravega and the processes used to govern the organization.

## Mission
Pravega targets the development of software for streaming data, with a focus on storage. It is core to our mission to develop and grow a thriving community of software developers. The community drives the technical direction of Pravega via open discussions and votings. By design, very few actions are private. It accepts contributions from any interested party as long as such a contribution is performed according to the project Code of Conduct. The Pravega community praises diversity and inclusion.

## Code of Conduct
Pravega follows the CNCF Code of Conduct:

https://github.com/cncf/foundation/blob/master/code-of-conduct.md

## Structure
The project comprises two main groups of contributors:

1- **Steering Committee**. The Steering Committee is responsible for general project oversight and for representing the project. They are owners of the `pravega` Github org. The committee responsibilities include interacting with the CNCF board, voting on new committers and members, and interacting with various CNCF bodies.

2- **Committer Team**. The repositories under the `pravega` Github org are split into four groups, each associate to a team: core, operators, ecosystem, and integration and tools. A committer is a member with write permission in one or more teams. Being a committer for a given team gives the member write permission to all repositories associated to the team. Members of the Steering Committee are committers in all teams.

## Communication
The primary way of communicating within the project is email. Contributors are free to discuss offline issues, e.g., using slack, but any resolution needs to be communicated by email. Voting in particular must happen on the appropriate mailing list.

The following are email lists available to the project:

- cncf-pravega-dev@lists.cncf.io : this list is used to discuss topics related to development. It is common across all teams.
- cncf-pravega-user@lists.cncf.io : this list is for users to ask questions about how to use Pravega software. It is common across all teams.
- cncf-pravega-private@lists.cncf.io : this is a list reserved to the members of the steering committee. It should be used only for private topics, such as discussion on new committeers and voting of the same.
- cncf-pravega-security@lists.cncf.io : security issues should not be disclosed openly. We prefer that uncovered vulnerabilities and related security issues are first reported to this list. The committers subscribed to the list have the obligation to respond to security reports acknowleding them and communicating with the reporter. 
- cncf-pravega-conduct@lists.cncf.io : any violation of the project code of conduct should be communicated to this list. The project will investigate reports and take appropriate measures. 

Any topic that requires discussion should use the prefix `[DISCUSS]` in the email subject. For example, say that the release manager of an upcoming release wants to discuss what is going to be in that release. The release manager starts an email thread with subject `[DISCUSS] Issues to be included in version x.y.z`. Vote email threads should be prefixed with `[VOTE]` as discussed below.

It is good practice to put deadlines for contributors to respond. We use a minimum of 72 hours, but it can be longer depending on the matter. The email must clearly say what the deadline is to close the thread.

## New Committers and Steering Committee members 
New committeers and Steering Committee members are voted by the Steering Committee. The Committer Teams are free to propose new committers to the Steering Committee. Proposals must provide evidence of the contributions of the proposed developer to justify the committership offer. The Steering Committee will discuss and vote such proposals privately.

If a Steering Committee member wants to propose Joe as a new committer and wants to discuss Joe's merits before calling a vote, the member can start an email thread in the private list with title `[DISCUSS] Joe as new committer of Core Team`. Once it 

## Decision making

Different actions require voting. In this section, we discuss the different approval and action types, along with how to conduct a vote.

### Approvals

We use different approval types depending on the action being voted on. This section describes the approval types, and the next section presents the different action types.

Approval type| Explanation
----------|----------------
Consensus |	For this to pass, all voters with binding votes must vote and there can be no binding vetoes (-1). Consensus votes are rarely required due to the impracticality of getting all eligible voters to cast a vote.
Lazy Consensus |	Lazy consensus requires 3 binding +1 votes and no binding vetoes.
Lazy Majority |	A lazy majority vote requires 3 binding +1 votes and more binding +1 votes that -1 votes.
Lazy Approval |	An action with lazy approval is implicitly allowed unless a -1 vote is received, at which time, depending on the type of action, either lazy majority or lazy consensus approval must be obtained.
2/3 Majority |	Some actions require a 2/3 majority of active committers or Steering Committee members to pass. Such actions typically affect the foundation of the project (e.g. adopting a new codebase to replace an existing product). The higher threshold is designed to ensure such changes are strongly supported. To pass this vote requires at least 2/3 of binding vote holders to vote +1.

### Vetoes

A valid, binding veto cannot be overruled. If a veto is cast, it must be accompanied by a valid reason explaining the reasons for the veto. The validity of a veto, if challenged, can be confirmed by anyone who has a binding vote. This does not necessarily signify agreement with the veto - merely that the veto is valid.

### Actions

The following table lists the actions that require voting and the necessary condition for the vote to pass. Note that anyone can vote on public votes, which in fact helps to gain more confidence on the direction of the vote

Action | Approval | Binding | Visibility | Min. time (days) 
-------|--------|---------|--------|-----------
New committer | Lazy Consensus | Steering Committee | Private | 3
New Steering Committee member | Lazy Consensus | Steering Committee | Private | 3
Removal of Committer | 2/3 Majority | Steering Committeee | Private | 7
Removal of Steering Committee member | 2/3 Majority | Steering Committee | Private | 7 
Change to bylaws (this document) | Lazy Consensus | Steering Committee | Public | 7
Change to Code of Conduct | 2/3 Majority | Steering Committee | Public | 7
Change to release process | 2/3 Majority | Steering Committee | Public | 7
Create a new repository | 2/3 Majority | Steering Committee | Public | 7
Release | Lazy Majority (must include a Steering Committee vote) | Committer + Steering Committee | Public | 3
Release plan | Lazy Majority | Committer | Public | 3
Code change | Lazy Approval | Committer | Public | 1

### Conducting a vote

To start a vote, send a message to the appropriate email list and prefix the subject with `[VOTE]`. For example, if contributors are expected to vote on a release candidate, then the subject should be `[VOTE] Release x.y.z Candidate 0`. Votes for new committers and Steering Committee must also be prefixed accordingly.

The initial vote message must contain the deadline for contributors to vote. Once the dealine has passed, the initiator can decide to conclude or extend it as needed. One reason for extending is not having enough votes.

Once the vote completes, the initiator should send a message with a subject prefixed with `[RESULT][VOTE]` that states the result of the vote and summarizes the votes cast.
