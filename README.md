# A/B Testing

[Read an introduction to AB Testing](IntroductionToABTesting.md)

AB Testing at first appears to be a simple task. Group users into a bucket and measure whether they click on a red or green button.

But once you dive into the details, it becomes much more complex.

The objective of this repository is to provide knowledge to new comers to understand the complexities and nuances of A/B teting and resources to learn from.

## Terms

* [Overall Evaluation Criterion](Term-OverallEvaluationCriterion.md)

## Papers to Read and Videos To Watch

In no partucular order:

* [Best Practices From Optimizely (Talk)](BestPracticesFromOptimizely.md)
* [Controlled Experiments On The Web (Paper)](ControlledExperimentsOnTheWeb.md)
* [Experiments At Airbnb (Article)](ExperimentsAtAirbnb.md)
* [Focusing On The Long Term (Paper)](FocusingOnTheLongTerm.md)
* [How Not To Run An A-B Test (Article)](HowNotToRunAnA-BTest.md)
* [Online Controlled Experiments (Video)](OnlineControlledExperiments.md)
* [PlanOut Framework (by Facebook) (Paper)](PlanOut-Facebook.md)
* [Statistics For The Internet Age](StatisticsForTheInternetAge.md)
* [Tools For A/B Testing](ToolsForABTesting.md)
* [Startup Metrics for Pirates (Talk)](PirateMetrics-AARRR.md)

Tools

* [Optimizely - The New Stats Engine (White Paper)](Optimizely-TheNewStatsEngine.md)



## Objectives

Based on several identifiable attributes, group a customer, and run tests against those groups to determine what indicators work best on which groups. Are groups valid? Are attributes valid: do they signal what we think they’ll signal.

Through testing can we identify our best customers, and drive them to sales? How do we best focus on these desirable customers and understand their wants and needs, so we can deliver what the customer is looking for. 
Can we focus on a small portion of the sales ‘funnel’ and drive more growth from it? Can we identify Salmon customers, define tests and refine based on outcomes: leads or sales?

Gather identifiable attributes
* Set up tests against small set of indicators and run tests
* If tests succeed, refine further
* Can we look at historical attributes gathered and identify bucket customer should go into


Need to split testing into different objectives. How do we get them further through the lead process?
Get person to give us info so we can specialize their responses
Get them to ask questions on chat

Items to test:
Do users want to figure out their down payment
In search do they want to see the top priced cars? Can we display a modal to show them the cars they want? Like Price, and type of car? Is the modal feel disruptive?
If you ask the user for their answer ‘they will lie’ so watch them
https://vimeo.com/83962056 minute 38


Experiments:
Run against 10-15% of users
Run for several weeks - prevents biasing test to weekend users vs weekday users



## Articles to read and condence:

Customer Review of Book: “A / B Testing: The Most Powerful Way to Turn Clicks Into Customers”
https://www.amazon.com/gp/customer-reviews/R44BH2HO30T18/ref=cm_cr_dp_d_rvw_ttl?ie=UTF8&ASIN=1118792416
Papers suggested:
- Controlled Experiments on the Web: Survey and Practical Guide
- Seven Rules of Thumb for Web Site Experimenters
- Trustworthy Online Controlled Experiments: Five Puzzling Outcomes Explained
- Online Controlled Experiments at Large Scale
- Unexpected Results in Online Controlled Experiments

Seven Rules of Thumb for Web Site Experimenters
http://www.exp-platform.com/Documents/2014%20experimentersRulesOfThumb.pdf

ToRead

## Resources

Sample Size Calculator
http://www.evanmiller.org/ab-testing/sample-size.html

Allows calculation of sample sizes


## What to Optimize For

http://www.exp-platform.com/Documents/controlledExperimentsHippoEbay.pdf

**Define Your OEC**

Optimize for the long term, not just clickthroughs

* The sewing machine ad did not win on clickthrough, but it won on sales because they sold many pairs
* Example long-term metrics
    * Time on site (per time period, say week or month)
    * Visit frequency
* Phrased differently: optimize for customer lifetime value
* We use the term OEC, or Overall Evaluation Criterion, to denote the long-term metric you really care about
* Continue to evaluate many metrics to understand the specifics and for understanding why the OEC changed

## Further Rough Notes


https://www.forbes.com/sites/danwoods/2017/03/09/why-ab-testers-have-the-best-jobs-in-tech/#7046399d73fe


MOST WINNING A/B TEST RESULTS ARE ILLUSORY
http://www.qubit.com/sites/default/files/pdf/mostwinningabtestresultsareillusory_0.pdf

The introduction of A/B testing often disrupts current power structures, and may be resisted by those who now have to pay attention to data rather than live by their wits. As a friend of mine who worked at Google once told me: “Google doesn’t have a large middle management layer. Because the company has so much data and knows how to use it, data plays the key decision making roles of middle management.” Few companies introduce data as a decision making force without causing disruption.



https://www.invisionapp.com/blog/improving-conversion-rates-ab-tests/
1. Gather data - with analytics and usability testing
	look at where people are going on your website, what they’re doing, and where there could be potential problems.
	
	Traffic
		What traffic sources are converting well? Poorly? Why?
		What device types are converting well? Poorly? Why?
		What are the key pages? Bounce rates? Exit rates?
	Funnel
		Where are the key drop-off points within your funnel?
		Where are the key drop-off points within your forms?
	Goals
		What’s the current conversion rate?
		What’s been your best conversion rate?
	Site search
		What phrases are people searching for?
		What pages are people starting their search from?


https://apptimize.com/blog/2014/01/etsy-continuous-innovation-ab-testing/

A: What are some A/B testing best practices that you use at Etsy?

L: Designing experiments correctly is very important. The infrastructure and the tooling is fun to work with, but you’ve got to know the right question to ask before you can find good answers. We make sure to check the size of the audience as a first step. If the exposure of an experiment is too small, too much time will have to pass in order to prove any results with statistical significance. This can be the biggest challenge. (Note from Apptimize: check out our recent blog post on estimating audience size and time required for running A/B tests.)

A: How often do experiments have a significant result?

L: Most of the time we find out at least a handful of things from an experiment. We measure experiments in terms of their effect on key metrics like conversion, order value, bounce rate or user engagement. It’s very rare that a change won’t affect at least one of these significantly. A lot of the time the experiments reveal that our ideas need more thought and this is how experiments can manage to save us a lot of time in development.


A/B Testing in Angular2
https://github.com/daniellmb/ab-test
https://github.com/daniellmb/angular-test-patterns/blob/master/patterns/ab.md



