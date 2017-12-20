# Online Controlled Experiments: Lessons from Running A/B/n Tests for 12 Years (Video)

**Ron Kohavi - 2015-11-30**

https://www.youtube.com/watch?v=qtboCGd_hTA

Start by analyzing a small set of users to make sure everything is ok, but grow that to 30-50% of users in the ‘Treatment’ group. 
Instrument and many things as possible. Overtime instrument as many things as possible. 
- Timings on servers
- scroll on the client
- hover
- everything the user does
Msft does A/B/n, 2-4 treatments. MVT rarely used
“Purpose of tests is to show causality. If the metrics are statistically different which are ‘coming out the bottom’ (revenue, sold items, etc) you can claim that the change you’ve introduced in your treatment caused the metrics to change with high probability.”

“Most of the best innovations we have come from people coming up with dramatically different ideas, not from tweaking”
Can do the color test, they do make money and sometimes the surprise me at how well they do. Change shades of black and blue on the search page, and it was worth over $10 million per year. And tested 30 colors. But they’re not going to get you that 10% winner.

“Do you do 0-fact(??) where you change one factor at a time?” Found this works the best when you want to develop some theory about whats happening and improve your knowledge about whats happening.
How do you know which metrics to look at? Look at scorecard(visual way to look at metrics) and it will point out the statistically significant differences

If you change too many different things, everyone will pick the thing they think caused it and being very comfortable. This is a big disadvantage.

Theory is better defined if one change is made at a time.
https://research.google.com/pubs/pub36500.html

The idea of the paper is that to get lots of tests running, users will have to be in more than one experiment. But when theyre in more than one experiment, how do you make sure you the experiments dont overlap or influence one another. - You can run tests to detect these issues/conflicts.

Figure out your OEC
Book: How to Measure Anything: Finding the Value of "Intangibles" in Business by Douglas W. Hubbard
pirate metrics - aarrr - http://startitup.co/guides/374/aarrr-startup-metrics
