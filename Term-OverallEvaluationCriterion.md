# Term - Overall Evaluation Criterion

Overall Evaluation Criterion (OEC) is referenced in many of the papers published by Kohavi et al. It originally comes from *[Design of Experiments Using The Taguchi Approach: 16 Steps to Product and Process Improvement](https://books.google.com/books?id=6zq3c3FaCq8C&q=Overall+Evaluation+Criterion#v=snippet&q=Overall%20Evaluation%20Criterion&f=false)*.

> The conept of an overall evaluation critieria occurs when there are more than one objective that a product or process is expected to satisfy. [1](Page 51)

In A/B experiments, we may need use more than one metric when evaluating the success of an experiment.

> The Overall Evaluation Criterion (OEC) [1] is a quantitative measure of the experiment’s objective. In statistics this is often called the Response or Dependent Variable (Mason et al. 1989;Box et al. 2005); other synonyms include Outcome, Evaluation metric, Performance metric, or Fitness Function (Quarto-vonTivadar 2006). Experiments may have multiple objectives and a scorecard approach might be taken (Kaplan and Norton 1996)[5], although selecting a single metric, possibly as a weighted combination of such objectives is highly desired and recommended. A single metric forces tradeoffs to be made once for multiple experiments and aligns the organization behind a clear objective. A good OEC should not be short-term focused (e.g., clicks); to the contrary, it should include factors that predict long-term goals, such as predicted lifetime value and repeat visits. Ulwick describes some ways to measure what customers want.”
> [2](Page 3)

> When a product or process under study is to satisfy more than one objective, performances of samples tested for each trial condition are evaluated by multiple criteria of evaluation. Such evaluations can be combined into a single quantity, the overall evaluation criterion (OEC), which is considered the result for the sample. But the evaluation of each individual criterion may have different units of measure, quality characteristics, and relative weighting. To combine the different criteria, they must first be normalized and weighted accordingly. [1](Page 53)

> **Define Your OEC**
> Optimize for the long term, not just clickthroughs
> * The sewing machine ad did not win on clickthrough, but it won on sales because they sold many pairs
> * Example long-term metrics
>     * Time on site (per time period, say week or month)
>     * Visit frequency
> * Phrased differently: optimize for customer lifetime value
> * We use the term OEC, or Overall Evaluation Criterion, to denote the long-term metric you really care about
> * Continue to evaluate many metrics to understand the specifics and for understanding why the OEC changed
> [3](Slide 10)


> It has been suggested that OECs should include metrics that reflect an improvement in the long-term (years) rather than metrics that merely optimize for the short-term (days or weeks). In [2], Kohavi et al. show that optimizing for short-term gains may actually be detrimental in the long-term.
> We encountered this problem at Google when experimenting with changes to the systems and algorithms that determine which ads show when users search. Optimizing which ads show based on short-term revenue is the obvious and easy thing to do, but may be detrimental in the long-term if user experience is negatively impacted. Since we did not have methods to measure the long-term user impact, we used short-term user satisfaction metrics as a proxy for the longterm impact. When using those user satisfaction metrics, we did not know what trade-off to use between revenue and user satisfaction, so we tended to be conservative, opting for launch variants with strong user experience. The qualitative nature of this approach was unsatisfying: we did not know if we were being too conservative or not conservative enough. [4](Page 1)


[1][Design of Experiments Using The Taguchi Approach: 16 Steps to Product and Process Improvement](https://books.google.com/books?id=6zq3c3FaCq8C&q=Overall+Evaluation+Criterion#v=snippet&q=Overall%20Evaluation%20Criterion&f=false)

[2][Trustworthy Online Controlled Experiments: Five Puzzling Outcomes Explained](http://www.exp-platform.com/Documents/puzzlingOutcomesInControlledExperiments.pdf)

[3][Practical Guide to Controlled Experiments on the Web: Listen to Your Customers not to the HiPPO](http://www.exp-platform.com/Documents/controlledExperimentsHippoEbay.pdf)

[4][Focusing on the Long-term: It’s Good for Users and Business](https://static.googleusercontent.com/media/research.google.com/en//pubs/archive/43887.pdf)

[5][Balanced Scorecard](http://home.bi.no/fgl99011/bok2302/BM96.pdf)
