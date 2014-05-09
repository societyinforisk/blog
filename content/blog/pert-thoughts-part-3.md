Title: Some Thoughts about PERT and other distributions - part 3
Date: 2011-12-13 14:42:00
Category: Blog
Tags: Blog
Slug: pert-thoughts-part-3
Author: Patrick Florer

<p><span face="">(this is the third post of three)</span></p>
<p>&nbsp;</p>
<p><strong><em><span face="">Experiment #1 &ndash; how well does BetaPERT predict the actual data?</span></em></strong></p>
<p><span face="">Using the overall minimum and maximum for the 94 observations, I ran another Monte Carlo simulation using these parameters:</span></p>
<p class="rteindent1"><span face="">Min = 0</span></p>
<p class="rteindent1"><span face="">Most Likely = 2,000,000 (derived as described below)</span></p>
<p class="rteindent1"><span face="">Max = 7,500,000</span></p>
<p class="rteindent1"><span face="">gamma/lambda = 4</span></p>
<p class="rteindent1"><span face="">Monte Carlo iterations = 100,000</span></p>
<p><span face="">Excel could not calculate a mode because all 94 values in the Ponemon study were unique.&nbsp; Using a value for the bins = 76 (0 through 7,500,000 binned by 100,000), I obtained a value of 2,000,000 from the histogram, which I used as the mode/most likely estimate.</span></p>
<p><span face="">Here is the histogram that was created by ModelRISK, using the VoseModPERT function: </span></p>
<p><img src="{filename}/images/pt3-graphic1.jpg" style="width: 600px; height: 377px;" /></p>
<p><span face="">As you can see, the shape of the histogram created by the BetaPERT function is similar to the histogram for the actual data.&nbsp; But is it similar enough to be believable?&nbsp; A comparison of values at various percentiles tells a better story:</span></p>
<p><img src="{filename}/images/Pic2.jpg" style="width: 451px; height: 581px;" /></p>
<p><span face="">With the exception of the minimum estimate, where the variance is due to using 0 as a minimum estimate instead of 378,000, and the estimates at the 5<sup>th</sup></span> and 10<sup>th</sup> percentiles, the remaining variances are within +/-20%.&nbsp;&nbsp; In fact, all of the variances between the 1<sup>st</sup> and 99<sup>th</sup> percentiles are positive, which means that, up to the 99<sup>th</sup> percentile, the BetaPERT function has over-estimated the values.</p>
<p><span face="">Is this close enough, especially the 8% underestimate at the 99<sup>th</sup></span> percentile?&nbsp; For me, probably so, because we already know that we are going to have trouble in the tails with any kind of estimate.&nbsp; But for you, maybe not - you be the judge.</p>
<p><strong><em><span face="">Experiment #2 &ndash; is there another distribution that predicts the actual data more closely than BetaPERT?</span></em></strong></p>
<p><span face="">The ModelRISK software has a &ldquo;distribution fit&rdquo; function that allows you to select a data set for input and then fit various distributions to the data.&nbsp; Using the 94 compliance cost values from the Ponemon study as input, I let ModelRISK attempt to fit a variety of distributions to the data.</span></p>
<p><span face="">The best overall fit was a Gamma distribution, using alpha = 3.668591 </span>and beta = 588093.8.&nbsp; The software calculated these values &ndash; I didn&rsquo;t do it and would not have known where to start.</p>
<p><span face="">Here is the histogram:</span></p>
<p><img src="{filename}/images/pt3-graphic3.jpg" style="width: 600px; height: 377px;" /></p>
<p><span face="">And here is a comparison based upon percentiles:</span></p>
<p><img src="{filename}/images/pt3-graphic4.jpg" style="width: 451px; height: 581px;" /></p>
<p><span face="">This gamma distribution is even a better fit than the BetaPERT distribution.&nbsp; Except at the extreme tails, the variances fall within +/- 11% - closer than the +/- 20% of the BetaPERT.</span></p>
<p><span face="">From a theoretical point of view, this is interesting.&nbsp; But from a practical point of view, it is problematic.&nbsp; It&rsquo;s one thing to fit a distribution to a data set and derive the parameters for a probability distribution.&nbsp; But it&rsquo;s quite another matter to know, in advance, which distribution might best predict a data set and what the parameters should be for that distribution.&nbsp; In addition, the Gamma distribution is typically used for creating distributions that describe the random occurrence of events during a time-frame.&nbsp; I am not sure how appropriate its use might be to describe a distribution of loss magnitudes or costs &ndash; I plan to find out!</span></p>
<p>&nbsp;</p>
<p><strong><span face="">Concluding remarks:</span></strong></p>
<p><span face="">While tests on a single, small dataset do not provide conclusive proof for the ability of the PERT and other distributions to match up to actual data, they do provide encouragement and motivation for further testing.</span></p>
<p><span face="">It would be useful to perform tests like these on larger datasets.&nbsp; Perhaps one of you has access to such data?&nbsp; If so, how about doing some tests and writing a blog post?</span></p>
<p><span face="">It might also be possible to use the &ldquo;Total Affected&rdquo;/Records exposed data from datalossdb to test the ability of BetaPERT to model reality.&nbsp; I would invite anyone interested to give it a try.</span></p>
<p><span face="">As we build our experience fitting parametric distributions to different data sets, our knowledge of which distributions to try in which circumstances will surely grow, and lead, hopefully, to more useful and believable risk analyses.</span></p>
