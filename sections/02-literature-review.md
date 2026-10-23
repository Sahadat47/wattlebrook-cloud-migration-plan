<!-- Owner: Malmika Sandagomi -->

# 2 Literature Review

There are four bodies of work that influence the plan: cloud migration strategies, cloud migration as a process, cloud adoption in banking and the Australian regulatory context. The review ends with the project management frameworks that have been employed and a summary of the ways the literature was used in the decision making of the plan.

## 2.1 Cloud Migration Strategies

Gartner's original framework identified five ways to take an application to the cloud: rehost, refactor, revise, rebuild, or replace with software as a service. Gartner emphasized that there is no "silver bullet" and that the choice depends on employees' expertise, value of current investments, and the architecture of the application [@gartner5rs]. AWS would later go on to expand upon this to the "7 Rs": retire, retain, rehost, relocate, repurchase, replatform and refactor [@aws7rs]. The two frameworks are broadly compatible – Gartner's "replace" is broadly the same as AWS' "repurchase," although AWS includes two additional options that are important for a bank: *retire*, for systems that are no longer needed, and *retain*, for systems that are too risky to move, have unresolved dependencies, or simply must stay on-premises for compliance reasons.

The AWS guidance is also more prescriptive in terms of trade-offs. It suggests rehosting, replatforming, relocating and retiring for large migrations and suggests that refactoring is the most complex and expensive solution for large migrations, and that it is better to modernise after migrating, not during migration [@aws7rs]. This plan is based on the following five of the seven recommendations: document management is rehosted, the CRM and data warehouse and loan system are replatformed, payroll is repurchased as SaaS, the old reporting server is retired and the core banking ledger is left in place. An intentional exception is the internet banking portal. One of the key reasons for the project (BO3) is that the portal cannot scale at the end of the month—so this wouldn't be solved by replatforming. The plan takes the additional risk of refactoring and balances it: The refactor is in the last wave of the schedule and has the biggest float in the schedule and is covered under fixed-price milestones (risk R07). There isn't anything wrong with refactoring, it's just that it's costly and dangerous. The plan should demonstrate that the benefit outweighs the risk and that the risk is controlled.

## 2.2 Cloud Migration as a Process

Research interests have been less on the choice of strategy and more on *how* to migrate. The authors of the systematic review of 23 studies found that the cloud migration research is still in its infancy, with still not much tool support and no general migration framework [@jamshidi2013]. The activities, techniques and concerns that appear in many migrations were identified in a later survey of migration process models and a framework was proposed for comparing the models [@gholami2016]. The authors of [@gholami2017] surveyed 104 experts and discovered that migrating legacy applications to the cloud is expensive and challenging, challenging problems are technical as well as non-technical, and that many migrations fail because of lack of understanding and preparation. Interviews and a survey of practitioners corroborate this and confirm that legacy systems are highly valued by interviewees' organisations and that challenges of modernising these systems are, apart from technical, also organisational and business oriented [@khadka2014].

The sources are all in agreement: preparation and people are just as important as technology. There is one caveat: much of this research is about 10 years old, and predates the more sophisticated migration tooling of today. Its central message, however, of understanding the systems in place and their interdependencies, following a structured process, and of managing the human element is echoed in existing provider guidance [@aws7rs] and in regulatory guidance [@apracloud] and therefore is still current. The plan reflects them: it invests in discovery and dependency mapping (WBS 2.0), repeats the same structured pattern in each wave, and has a specific work package dedicated to training and change management (WBS 8.0).

## 2.3 Cloud Adoption in Banking

## 2.4 Regulatory Context in Australia

## 2.5 Project Management Frameworks

## 2.6 Implications for the Plan
