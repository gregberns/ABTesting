# Controlled Experiments on the Web
	
Paper: Controlled Experiments on the Web: Survey and Practical Guide
https://ai.stanford.edu/~ronnyk/2009controlledExperimentsOnTheWebSurvey.pdf

“Translating the lost clicks to their monetary value, it was higher than the expected ad revenue, so the idea of adding more ads to the MSN home page was scrapped.”
-Its important to ‘follow’ the money all the way through, or translate to the end goal/ translate to the other downstream metrics.

“Backend algorithm changes, such as search”... can you switch around the top several results and see click through differences?
“Data Mining and Personalization department at Amazon“

Term: “[Overall Evaluation Criterion (OEC) (Roy 2001)](Term-OverallEvaluationCriterion.md). A quantitative measure of the experiment’s objective. In statistics this is often called the Response or Dependent Variable (Mason et al. 1989;Box et al. 2005); other synonyms includeOutcome,Evaluation metric, Performance metric, or Fitness Function (Quarto-vonTivadar 2006). Experiments may have multiple objectives and a scorecard approach might be taken (Kaplan and Norton 1996), although selecting a single metric, possibly as a weighted combination of such objectives is highly desired and recommended. A single metric forces tradeoffs to be made once for multiple experiments and aligns the organization behind a clear objective. A good OEC should not be short-term focused (e.g., clicks); to the contrary, it should include factors that predict long-term goals, such as predicted lifetime value and repeat visits. Ulwick describes some ways to measure what customers want.”

Term: “Factor. A controllable experimental variable that is thought to influence the OEC. Factors are assigned Values, sometimes called Levels or Versions. Factors are sometimes called Variables. In simple A/B tests, there is a single factor with two values: A and B.”

Term: “Experimental unit. The entity over which metrics are calculated before averaging over the entire experiment for each variant. Sometimes called an item. The units are assumed to be independent. On the web, the user is a common experimental unit”

Term: “A/A test. Sometimes called a Null Test (Peterson 2004). Instead of an A/B test, you exercise the experimentation system, assigning users to one of two groups, but expose them to exactly the same experience. An A/A test can be used to (i) collect data and assess its variability for power calculations, and (ii) test the experimentation system (the Null hypothesis should be rejected about 5% of the time when a 95% confidence level is used).”

## 3.4 Effect of robots on experimental results 
Robots can introduce significant skew into estimates, enough to render assumptions invalid. We have seen cases where robots caused many metrics to be significant when they should not have been (e.g., much more than 5% false positives for an A/A test).

## 3.5.3 Software migrations 
Experiments can be used to help with software migration. If a feature or a system is being migrated to a new backend, new database, or a new language, but is not expected to change user-visible features, an A/B test can be executed with the goal of retaining the Null Hypothesis, which is that the variants are not different. We have seen several such migrations, where the migration was declared complete, but an A/B test showed significant differences in key metrics, helping identify bugs in the port. Because the goal here is to retain the Null Hypothesis, it is crucial to make sure the experiment has enough statistical power to actually reject the Null Hypothesis if it false.

## 3.6 Limitations

Quantitative metrics, but no explanations. It is possible to know which variant is better, and by how much, but not “why.”

Short term versus long term effects. Controlled experiments measure the effect on the OEC during the experimentation period, typically a few weeks. While some authors have criticized that focusing on a metric implies short-term focus (Quarto-vonTivadar 2006; Nielsen 2005), we disagree. Long-term goalsshould be part of the OEC. Let us take search ads as an example. If your OEC is revenue, you might plaster ads over a page, but we know that many ads hurt the user experience, so a good OEC should include a penalty term of usage of real-estate for ads that are not clicked, and/or should directly measure repeat visits and abandonment.

Primacy and newness effects. These are opposite effects that need to be recognized. If you change the navigation on a web site, experienced users may be less efficient until they get used to the new navigation, thus giving an inherent advantage to the Control. Conversely, when a new design or feature is introduced, some users will investigate it, click everywhere, and thus introduce a “newness” bias. This bias is sometimes associated with the Hawthorne effect (2007). Both primacy and newness concerns imply that some experiments need to be run for multiple weeks. One analysis that can be done is to compute the OEC only for new users on the different variants, since they are not affected by either factor.

There are two primary benefits of a single MVT versus multiple sequential A/B tests to test the same factors: 
You can test many factors in a short period of time, accelerating improvement. For example, if you wanted to test five changes to the website and you need to run each A/B test four weeks to achieve the power you need, it will take at least five months to complete the A/B tests. However, you could run a single MVT with all five factors in one month with the same power as with the five A/B tests. 
You can estimate interactions between factors. Two factors interact if their combined effect is different from the sum of the two individual effects. If the two factors work together to enhance the outcome the interaction is synergistic. If instead they work against each other to dampen the effect, the interaction is antagonistic.
Three common limitations are:
Some combinations of factors may give a poor user experience.
Analysis and interpretation are more difficult.
It can take longer to begin the test. 
Generally, we believe the first experiment one does should be an A/B test mainly due to the complexity of testing more than one factor in the same test.

## 5.0 Implementation architecture 
Implementing an experiment on a website involves three components. The first component is the randomization algorithm, which is a function that maps end users to variants. The second component is the assignment method, which uses the output of the randomization algorithm to determine the experience that each user will see on the website. The third component is the data path, which captures raw observation data as the users interact with the website, aggregates it, applies statistics, and prepares reports of the experiment’s outcome.

## 5.3.1 Event-triggered filtering
One critical way to control this variability is to restrict the analysis to only those users who were impacted by the experiment (see Sect. 3.2.3). We can further restrict the analysis to the portion of user behavior that was affected by the experiment. We refer to these data restrictions as event-triggered filtering. Event-triggered filtering is implemented by tracking the time at which each user first saw content that was affected by the experiment.

## 6.1.2 Speed matters 
A Treatment might provide a worse user experience because of its performance. Linden (2006b, p. 15), wrote that experiments at Amazon showed a 1% sales decrease for an additional 100msec, and that a specific experiment at Google, which increased the time to display search results by 500 msecs reduced revenues by 20%

## 6.2.1 Run continuous A/A tests

## 6.2.2 Automate ramp-up and abort
Automatically shut-down a Treatment if it is significantly underperforming relative to the Control

## 6.2.3 Determine the minimum sample size 
Decide on the statistical power, the effect you would like to detect, and estimate the variability of the OEC through an A/A test. Based on this data you can compute the minimum sample size needed for the experiment and hence the running time for your web site.

## 6.2.4 Assign 50% of users to treatment One common practice among novice experimenters is to run new variants for only a small percentage of users.

## 6.2.5 Beware of day of week effects Even if you have a lot of users visiting the site, implying that you could run an experiment for only hours or a day, we strongly recommend running experiments for at least a week or two, then continuing by multiples of a week so that day-of-week effects can be analyzed.

“it would require over 125 days, a period we consider too long for reliable result; factors, such as cookie churn, that have secondary impact in experiments running for a few weeks may start contaminating the data.”

## 6.3.2 Beware of launching features that “do not hurt” users
In the face of a “no significant difference” result, sometimes the decision is made to launch the change anyway “because it does not hurt anything.” It is possible that the experiment is negative but underpowered.

## 6.3.4 Change to a data-driven culture
“Sometimes you have to kiss a lot of frogs to find one prince. So how can you find your prince faster? By finding more frogs and kissing them faster and faster.”
In a web world, we can integrate customer feedback directly through prototypes and experimentation. If an organization has done the hard work to agree on an OEC and vetted an experimentation system, experimentation can provide real data and move the culture towards attaining shared goals rather than battle over opinions.

“Software features in products today are commonly determined by the same way medicine was prescribed prior to World War II: by people who were regarded as experts, not by using scientific methods, such as controlled experiments. We can do better today, especially with our access to customer behavior online.”
