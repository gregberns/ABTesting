# Optimizely: The New Stats Engine (White Paper)

http://pages.optimizely.com/rs/optimizely/images/stats_engine_technical_paper.pdf

## Pre-Reading

Reading these first:

* [‘How Not To Run an A/B Test’](HowNotToRunAnA-BTest.md)
* [Statistics For The Internet Age](StatisticsForTheInternetAge.md)

may help provide a better background on why Optimizely made a change to their stats engine.

## Summary:

Optimizely is moving away from traditional, fixed horizon hypothesis testing to sequential testing and replacing Type I error control with false discovery rate (FDR) control. This will enable users to confidently check experiments as often as they like, not need to know an effect size in advance, and test as many variations and goals as desired without worrying about hidden sources of error.
