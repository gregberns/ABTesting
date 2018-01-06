# PlanOut Paper - FaceBook

Paper Url: https://arxiv.org/pdf/1409.3174v1.pdf

## Abstract: 

How to design experiments to test different concepts. There are different quantifiers to focus on.

### PlanOut JS Implementation

https://github.com/HubSpot/PlanOut.js

Mixpanel / Amplitude for logging and I think analytics


## Notes

p1
Experiments may be used to explore a design space [[19]](ControlledExperimentsOnTheWeb.md), better attribute outcomes to causes [3, 14], and estimate effects that help decision makers understand how people react to changes and use their services [23, 35].

p2
Several papers by Kohavi et al. present recommendations on how to implement and instrument experiments [[19]](ControlledExperimentsOnTheWeb.md), as well as common pitfalls in analyzing experiments [12, 18].

The PlanOut language separates experimental design from application logic and focuses experimenters on the core aspect of an experiment: how units (e.g., users, items, cookies) are randomly assigned to conditions, as defined by parameters (e.g., settings for user interface elements, references to ranking algorithms). PlanOut promotes a mental model where every aspect of the site is parameterizable, and experiments are a way of evaluating user experiences defined by those parameters.

p4
In an influential application of social psychological theory to online systems, Beenen et al. [6] experimented with strategies for encouraging users to contribute ratings to the movie recommendation service and online community MovieLens.

4.2.2 Continuous-treatment encouragement design Encouragement designs [17] randomize an inducement to a behavior of interest so as to evaluate the inducement or study the behavior’s downstream effects. In online services, it is common to encourage users to engage with a particular entity, user, or piece of content. For instance, if having more ties on Facebook is hypothesized to increase long-term engagement, one could establish a causal relationship by randomizing whether or not some users receive recommendations for additional friends. Evidence suggests that users who receive more feedback on Facebook are more likely to become engaged with the site [10]. If there is a (forward) causal relationship between these variables, then changes to the site that affect how much feedback users receive can in turn affect user engagement and content production.

For example, the primary purpose of the social cues experiment described in Section 4.1.2 is not to decide whether it is better to show fewer social cues alongside ads (doing so was expected to and did reduce desired behaviors), but to estimate quantities that are useful for understanding an existing service, allocating design and engineering resources, and anticipating effects of future changes.

 Some of the most effective experiments directly inform decisions to set the parameters they manipulate, but other well-designed experiments can be effective through broader, longer-term influences on beliefs of designers, developers, scientists, and managers.
