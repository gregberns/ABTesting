# Experiments at Airbnb

https://medium.com/airbnb-engineering/experiments-at-airbnb-e2db3abf39e7

Users often take a long time to book, so the early converters have a disproportionately large influence in the beginning of the experiment.

How long should experiments run for then? To prevent a false negative (a Type II error), the best practice is to determine the minimum effect size that you care about and compute, based on the sample size (the amount of new samples that come every day) and the certainty you want, how long to run the experiment for, before you start the experiment. Setting the time in advance also minimizes the likelihood of finding a result where there is none.
http://www.evanmiller.org/ab-testing/sample-size.html

A simple example of this process is to run an experiment where the treatment is equal to the control. These are called A/A or dummy experiments. In a perfect world the system would return a neutral result (most of the time). What does your system return? We ran many ‘experiments’ like this (see an example run in Figure 9) and identified a number of issues within our own system as a result. In one case, we ran a number of dummy experiments with varying sizes of control and treatment groups. A number of them were evenly split, for example with a 50% control and a 50% treatment group (where everybody saw exactly the same website). We also added cases like a 75% control and a 25% treatment group. The results that we saw for these dummy experiments are displayed in Figure 10.

In general, experiments should be run to make good decisions about how to improve the product, rather than to aggressively optimize for a metric. Optimizing is not impossible, but often leads to opportunistic decisions for short-term gains. By focusing on learning about the product you set yourself up for better future decisions and more effective tests.
