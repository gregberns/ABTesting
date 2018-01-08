# Data-Driven Metric Development for Online Controlled Experiments: Seven Lessons Learned (Paper)

http://www.kdd.org/kdd2016/papers/files/adf0853-dengA.pdf

## 2.2 Types of online metrics

* Type 1: Business report driven metrics
* Type 2: Simple heuristic based metrics.
* Type 3: User-behavior-driven metrics.

## Metric qualties: Directionality and Sensitivity

Directionality - a good goal metric (or OEC) should have a clear directional interpretation that aligns with user experience in most common cases.

Sensitivity - a good goal metric (or OEC) needs to be sensitive to most of the improvement of user experience.

## Understand roles of metrics

Instead of having an clear directional interpretation, it is more important for a good debugging metric to be sensitive. This is a distinct difference between debugging metrics and guardrail metrics.

### Guardrail Metrics

Guardrail metrics are metrics that help to guard against situations when the goal metrics may give us wrong signals.

The first scenario is to replace the goal metric (or OEC) in cases when the goal metric is not applicable.

The second scenario of guardrail metrics is to capture the dimensions of user experience that the goal metrics are not able to measure.

### Debugging Metrics

Are usually used to help us understand why some important metrics, especially the goal metrics, move or do not move, and how to interpret their movements.

## Evaluate metric qualities

### 3.3.1 Validation Corpus

Collect a set of high quality past experiments for which we have high confidence on whether their features are good for the users or not. This set of past experiments is called the validation corpus.

### 3.3.2 Degradation experiment

This leads us to the idea of using degradation experiments to validate metric direction and sensitivity

## 3.5 Lesson 5: Learn from offline data

A more advanced type of metrics – user-behavior-driven metrics – are getting more importance when the systems are at matured stages. User-behavior-driven metrics are based on user behavioral models that can predict or classify user experience of using the system, such as satisfaction, frustration, gain or cost [9; 11; 15; 17]. Thus, a carefully designed user-behavior driven metric usually has good alignment with user experience and high sensitivity.

Generally speaking, there are three major steps in developing user-behavior-driven metrics:

* Step 1: Have some hypotheses about the user experience based on preliminary observations. Start with the simplest model.
* Step 2: Design user study experiments and collect labeled data sets. Test the model from Step 1 on the collected labeled data sets.
* Step 3: Design online metrics based on the model learned from Step 2. Validate the metrics based on the validation corpus and try out the metrics on new A/B testing experiments as much as possible.

First of all, the hypotheses we start in Step 1 should capture important collective behavioral patterns of most users. By “collective behavioral patterns”, we mean the behavioral patterns that can be observed from most users.

It is absolutely possible that there are some users whose clicking or reformulation behavior is different from the majority; however, we do not have to worry too much about the behavioral patterns of the minority of the users unless there are some special cases we want to address (such as the feature of instant answer in search). 

In other words, the behavioral models for online metrics need to capture users’ homogeneous behavior instead of their heterogeneous behavior.

## 3.6 Lesson 6: Choose the right rate metrics

A rate metric is a metric that has two parts in its definition: the numerator and the denominator (and the denominator not be the count of users), such as Click Through Rate, Views per Movie, or Success Query Rate (i.e. the count of success queries divided by the count of total queries).

Rate metrics have good properties such as with bounded values, less skewed (e.g. the value of rate metric Query Success Rate is bounded between 0 and 1 and its distribution is less skewed than the count metric of Successful Queries per User) and relatively more sensitive.

Thus, there are two rules we have to follow when dealing with rate metrics:
1. We should always keep the denominator and the numerator as debugging metrics (discussed in Section 3.2) for a rate metric;
2. When we choose a rate metric to be a goal metric, we should choose the one whose denominator is relatively more stable in most cases.

The second issue is that there are two ways to compute the metrics for rate metrics: Average of Ratios and Ratio of Averages.

For instance, Click Through Rate (CTR) can be defined as A) Average CTR per User, and B) #(Clicks of all users)/#(Pageviews of all users).

Their main difference is how users are weighted. For average of ratios, users have the same weight on the final metric because each user has a single value of ratio. For ratio of averages, mathematically it is equivalent to weighted average of ratio per user, where weight is proportional to the denominator value for each user, e.g. user with more pageviews will have a higher impact on CTR.

Because of the difference in weighting, optimizing ratio of averages puts more emphasize on heavy users while optimizing average of ratios treats each user equally important.

In our experience, these two versions of rate metrics move in the same direction for most experiments. When they don’t, we get an interesting signal that the treatment effect is different between heavy users and average users, which begs our further investigation.
