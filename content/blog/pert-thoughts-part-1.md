Title: Some Thoughts about PERT and other distributions - part 1
Date: 2011-12-13 14:16:00
Category: Blog
Tags: Blog
Slug: pert-thoughts-part-1
Author: Patrick Florer

<p><span face="">(This is the first of three posts)</span></p>
<p><span face="">Most of the people in SIRA have heard of the PERT and BetaPERT distributions.&nbsp; Many of us use them on a daily basis in our modeling and risk analysis.&nbsp; For this reason, I think it is important that we understand as much as we can about where these distributions came from, what some of their limitations are, and how they match up to actual data.</span></p>
<p><strong><u><span face="">The PERT Distribution:</span></u></strong></p>
<p><span face="">The PERT approach was developed more than forty years ago to address project scheduling needs that arose during the development of the Polaris missile system.&nbsp; With regard to its use in scheduling, we can agree that the passage of time has a linear, understandable nature (leaving quantum mechanics out of the discussion, please) that might be appropriate for estimates of task completion times.&nbsp; The Polaris missile program probably wasn&rsquo;t the first big project these people had done (DoD and Booz Hamilton), so we can also assume that the originators of PERT had both experience and data to guide them when they constructed the function and created the math that they did.&nbsp; </span></p>
<p><span face="">The BetaPERT distribution was developed by David Vose in order to provide more flexibility in allowing for certainty or lack of certainty in PERT estimates.&nbsp; Vose added a fourth parameter, called gamma, that impacts the sampling around the most likely value and consequently controls the height of the probability density curve.&nbsp; As gamma increases, the height of the curve increases, and uncertainty decreases.&nbsp; As gamma decreases, the opposite happens.&nbsp; Some people use gamma as a proxy for confidence in the most likely estimate. </span></p>
<p><span face="">For additional information about the PERT and BetaPERT distributions and how to use them, please see the excellent SIRA blog post that Kevin Thompson wrote a few weeks ago.</span></p>
<p><span face="">(In order to keep things simple, from this point forward, unless there is a reason to make the distinction, I will use PERT to mean both PERT and modified/BetaPERT.)</span></p>
<p><strong><span face="">What&rsquo;s the problem?</span></strong></p>
<p><span face="">Most of us have been taught that PERT distributions are appropriate tools for taking estimates from subject matter experts (SME) and turning them into probability distributions using Monte Carlo simulation.&nbsp; As many of you know, this is very easy to do.&nbsp; The graphics and tables look very nice, informative, and even a bit intimidating.</span></p>
<p><span face="">But how do we really know that the distributions we create have any validity?</span></p>
<p><span face="">Just because they may have worked in project scheduling, why should we believe that the distribution of loss magnitude, frequency, or anything else actually corresponds to the probability distribution that a PERT function can create?&nbsp; Even if these distributions are useful and informative, might there be circumstances where we would be better served by not using them?&nbsp; Or by using other distributions instead?</span></p>
<p><span face="">I will address three of these issues below.</span></p>
<p><span face="">In case you don&rsquo;t feel like reading the whole post, I will tell you right now that:</span></p>
<ol>
	<li>
		<span face="">Yes, there are circumstances where PERT distributions do not yield good information.</span></li>
	<li>
		<span face="">In a series of tests with a small data set, PERT distributions DID seem to correspond to reality &ndash; closely enough, in my opinion, to be useful, informative, and even predictive.</span></li>
	<li>
		<span face="">Depending upon what we are trying to model, there are other distributions that might be even more useful than PERT.</span></li>
	<li>
		<span face="">It&rsquo;s a continual learning process &ndash; I want to encourage everyone to keep studying, experimenting, and sharing when possible.</span></li>
</ol>
<p><strong><u><span face="">When the PERT distribution doesn&rsquo;t work</span></u></strong></p>
<p><span face="">One of the assumptions of the PERT approach is that the standard deviation should represent approximately 1/6<sup>th</sup></span> of the spread between the minimum and maximum estimates.&nbsp; When I look at the PERT and BetaPERT math, I can see this at work.&nbsp; (for a full explanation, see <a href="http://vosesoftware.com/ModelRiskHelp/index.htm#Distributions/Continuous_distributions/PERT_distribution.htm"><span face="">http://vosesoftware.com/ModelRiskHelp/index.htm#Distributions/Continuous_distributions/PERT_distribution.htm</span></a><span face=""> )&nbsp; I have also read, and have demonstrated in my own experience, that PERT doesn&rsquo;t return useful results when the minimum or maximum are very large multiples of the most likely value.</span></p>
<p><span face="">For example, try this with OpenPERT or any other tool you like:</span></p>
<p class="rteindent1"><span face="">Min = 1</span></p>
<p class="rteindent1"><span face="">Most Likely = 100</span></p>
<p class="rteindent1"><span face="">Max = 100,000,000</span></p>
<p class="rteindent1"><span face="">gamma/lambda = 4</span></p>
<p><span face="">run for 1,000,000 iterations of Monte Carlo simulation, just to be fanatical about sampling the tail values.</span></p>
<p><span face="">(BTW, this is not a theoretical example &ndash; these data were supplied by a SME as part of a very large risk analysis project I was involved with two years ago &ndash; some list members who were involved in that project may remember this scenario.)</span></p>
<p><span face="">I think that you will find that the mode (if your program calculates one), the median, and the mean are all so much greater than the initial most likely estimate as to be useless.&nbsp; In addition, I think that you will find that the maximum from the MC simulation is quite a bit lower than the initial maximum estimate.</span></p>
<p><span face="">Here are my results:</span></p>
<p><span face="">(Please note &ndash; if you do this yourself, you won&rsquo;t get exactly the same results, but, if you run 1,000,000 iterations, your results should be close)</span></p>
<p><u><span face="">RiskAMP:</span></u></p>
<p class="rteindent1"><span face="">Min = 10</span></p>
<p class="rteindent1"><span face="">Mode = 40,058,620 </span></p>
<p class="rteindent1"><span face="">(This is very interesting &ndash; in a distribution this skewed, you would expect the mode &lt; median &lt; mean: maybe this is an example of why Vose considers the mode to be uninformative?)</span></p>
<p class="rteindent1"><span face="">Median = 12,960,195</span></p>
<p class="rteindent1"><span face="">Mean = 16,675,377</span></p>
<p class="rteindent1"><span face="">Max = 94,255,562</span></p>
<p>&nbsp;</p>
<p><u><span face="">ModelRISK:</span></u></p>
<p class="rteindent1"><span face="">Min = 6</span></p>
<p class="rteindent1"><span face="">Mode = &nbsp;&nbsp;&nbsp;ModelRISK doesn&rsquo;t calculate a Mode &ndash; see Vose&rsquo;s book for the explanation of why not</span></p>
<p class="rteindent1"><span face="">Median = 12,923,895</span></p>
<p class="rteindent1"><span face="">Mean = 16,654,354</span></p>
<p class="rteindent1"><span face="">Max = 93,479,781</span></p>
<p>&nbsp;</p>
<p><span face="">What&rsquo;s the takeaway here?&nbsp; </span></p>
<p><span face="">That there are some sets of estimates that PERT distributions don&rsquo;t handle very well.&nbsp; When we encounter large ranges that are highly skewed, we may need to re-think our approach, or ask the SME additional questions.</span></p>
<p>&nbsp;</p>
<p><span face="">To be continued &hellip;</span></p>
