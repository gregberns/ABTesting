# Statistics For The Internet Age

https://blog.optimizely.com/2015/01/20/statistics-for-the-internet-age-the-story-behind-optimizelys-new-stats-engine/

To illustrate how dangerous continuous monitoring can be, we simulated millions of A/A tests with 5,000 visitors, and evaluated the chance of making an error under different types of continuous monitoring policies. We found that even conservative policies can increase error rates from a target of 5% to over 25%.

In our investigation, more than 57% of simulated A/A tests falsely declared a winner or loser at least once during their course, even if only briefly. In other words, if you had been watching these tests, you might have wondered why your A/A test results called a winner.  The increase in error rate is still meaningful even if you aren’t looking after each visitor. If you look every 500 visitors, the chance of making a false declaration increases to 26%, while looking every 1000 visitors increases the same chance to 20%.
