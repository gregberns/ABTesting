# How Not To Run an A/B Test

http://www.evanmiller.org/how-not-to-run-an-ab-test.html

If you run experiments: the best way to avoid repeated significance testing errors is to not test significance repeatedly. Decide on a sample size in advance and wait until the experiment is over before you start believing the “chance of beating original” figures that the A/B testing software gives you. “Peeking” at the data is OK as long as you can restrain yourself from stopping an experiment before it has run its course. I know this goes against something in human nature, so perhaps the best advice is: no peeking!

If you really want to do this stuff right: Fixing a sample size in advance can be frustrating. What if your change is a runaway hit, shouldn’t you deploy it immediately? This problem has haunted the medical world for a long time, since medical researchers often want to stop clinical trials as soon as a new treatment looks effective, but they also need to make valid statistical inferences on their data. Here are a couple of approaches used in medical experiment design that someone really ought to adapt to the web:

Sequential experiment design: Sequential experiment design lets you set up checkpoints in advance where you will decide whether or not to continue the experiment, and it gives you the correct significance levels.
http://www.evanmiller.org/sequential-ab-testing.html

Bayesian experiment design: With Bayesian experiment design you can stop your experiment at any time and make perfectly valid inferences. Given the real-time nature of web experiments, Bayesian design seems like the way forward.
http://www.evanmiller.org/bayesian-ab-testing.html
