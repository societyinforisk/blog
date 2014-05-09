Title: Some Thoughts about PERT and other distributions - part 2
Date: 2011-12-13 14:37:00
Category: Blog
Tags: Blog
Slug: pert-thoughts-part-2
Author: Patrick Florer

<p><span face="">(this is the second of three posts)</span></p>
<p><strong><u><span face="">Does the shape of PERT distribution match up to an actual data set?</span></u></strong></p>
<p><span face="">At the beginning of this post (Part 1), I raised the question about the validity of the PERT function and whether the distributions it creates correspond to anything. </span></p>
<p><span face="">What follows are the results of an attempt to answer this question using a small data set extracted from a Ponemon Institute report called &ldquo;<em>Compliance Cost Associated with the Storage of Unstructured Information&rdquo;, </em>sponsored by Novell and published in May, 2011. &nbsp;I selected this report because, starting on page 14, all of the raw data are presented in tabular format.&nbsp; As an aside, this is the first report I have come across that publishes the raw data - <strong><em>please take note, Verizon, if you are reading this!</em></strong></span></p>
<p><span face="">Here is a histogram of the 94 actual observations, created using the standard functionality in Excel (Data\Data Analysis\Histogram) and tweaked a bit to show probability instead of frequency.</span></p>
<p><img src="/images/SIRABlog2011_11_30_v4-pt2-graphic1.jpg" style="width: 600px; height: 400px; " /></p>
<p align="center"><span face=""><img src="file:///C:\Users\Patrick\AppData\Local\Temp\msohtmlclip1\01\clip_image001.jpg" /></span></p>
<p><span face="">As you can see, the histogram is suggestive of a positively-skewed distribution - with some exceptions &ndash; there are several peaks and valleys.&nbsp; What these peaks and valleys mean is unclear &ndash; it could simply be observations that are missing &ndash; the study size was small:&nbsp; N = 94 organizations.&nbsp; Or they could be real &ndash; only more observations would tell us.</span></p>
<p><span face="">At this point, I asked myself &ndash; what if the Ponemon study had captured and had published minimum, maximum, and most likely values instead of single point estimates?&nbsp; If it had, then we could have constructed a more informative histogram.</span></p>
<p><span face="">In an attempt to simulate what things might have looked like, I took the Ponemon study raw data, computed minimum and maximum values for each of the 94 data points, and then ran a Monte Carlo simulation, using the following parameters:</span></p>
<p><span face="">Most Likely = the actual reported cost estimate provided by the report.</span></p>
<p><span face="">Min = Most Likely&nbsp; x&nbsp; a random number between 0 and 1</span></p>
<p><span face="">Max = Most Likely&nbsp; x&nbsp; ((1 + a random number between 0 and 1)&nbsp; x&nbsp; Most Likely))</span></p>
<p><span face="">gamma/lambda was set to 4 for all.</span></p>
<p><span face="">Since true minimum and maximum values were not reported by the study, I decided that using a random number as a multiplier to calculate both the minimum and the maximum values seemed as defensible as anything else for the purpose of my simulation.</span></p>
<p><span face="">I then ran 10,000 iterations of Monte Carlo simulation for each of the 94 BetaPERT functions, which resulted in 940,000 total estimates.&nbsp; Using 940,000 data points, standard functionality in Excel (Data\Data Analysis\Histogram), and a tweak to show probability instead of frequency, I created the following histogram:</span></p>
<p><img src="/images/SIRABlog2011_11_30_v4-pt2-graphic2.jpg" style="width: 600px; height: 328px; " /></p>
<p align="center"><span face=""><img src="file:///C:\Users\Patrick\AppData\Local\Temp\msohtmlclip1\01\clip_image003.jpg" /></span></p>
<p>This histogram is even more suggestive of a positively-skewed distribution.</p>
<p><span face="">But the same questions remain:&nbsp; Are the dips and valleys representative of missing observations, or are they real?&nbsp; And, how well would a BetaPERT function predict the shape of this histogram?&nbsp; How well would any other probability function perform, for that matter?&nbsp; And, perhaps most importantly, what, if anything, can we extrapolate about other compliance cost data sets from this one?</span></p>
<p><span face="">So, it was time for another experiment or two!</span></p>
<p><span face="">To be continued &hellip;</span></p>
<p>&nbsp;</p>

