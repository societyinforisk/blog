Title: Reducing Ignorance
Date:  2012-03-04 11:19:00
Category: Blog
Tags: Blog
Slug: reducing-ignorance
Author: Jay Jacobs (@jayjacobs)

<p>With this year&rsquo;s RSA conference still close in the rear view mirror, I felt I had to write about something that stuck in my mind as I went through the week.&nbsp; I found repeated <a href="http://en.wikipedia.org/wiki/Confirmation_bias">confirmation</a> to something <a href="https://www.societyinforisk.org/content/doug-hubbard-subject-matter-expertise-vs-expertise-risk-analysis">Doug Hubbard wrote</a>, &ldquo;I have never seen a single objection to using risk analysis in any profession that wasn&rsquo;t based on ignorance of what risk analysis is and what it can do.&rdquo; &nbsp;Keep in mind, ignorance isn&#39;t meant to be derogatory or insulting. &nbsp;It simply means a lack of knowledge or uninformed. &nbsp;Many of the people I heard object to risk analysis were incredibly smart in many ways, yet they were presenting objections from an uninformed position of risk analysis. &nbsp; It makes me wonder if we have to reduce ignorance about this field before we are able to successfully reduce uncertainty around our exposure to loss. &nbsp;</p>
<p>One such objection I encountered was during a conversation I had on the first night I was in San Francisco.&nbsp; After some lively back-n-forth with a colleague on the efficacy of risk management and some healthy skepticism from this person, I received this challenge: &ldquo;suppose I go into a casino with $100,000, what am I going to come out with?&rdquo;&nbsp; The assumption on his part was that analysis would provide a single number (perhaps an average loss) and whatever the answer was, it&rsquo;d be wrong.&nbsp; But my response was simply, &ldquo;what if I produce a distribution?&rdquo;&nbsp; And so, for this challenge I have whipped out the first graph.&nbsp; It is based on some very specific assumptions though.&nbsp; I made the assumption that the gambler would chose a (single) game for their visit and they were consistent in their gambling.&nbsp; Not that it mirrors reality, it just makes this example much easier (and this is just an example).&nbsp;&nbsp; <a href="/images/roulette1.png"><img align="right" alt="Screen shot 2012-03-03 at 6.22.46 PM" border="0" height="146" src="/images/roulette1.png" style="background-image: none; border-right-width: 0px; padding-left: 0px; padding-right: 0px; display: inline; float: right; border-top-width: 0px; border-bottom-width: 0px; border-left-width: 0px; padding-top: 0px" title="Screen shot 2012-03-03 at 6.22.46 PM" width="244" /></a></p>
<p>Here are the other assumptions:</p>
<ul>
	<li>
		American Roulette (with the &ldquo;0&rdquo; and &ldquo;00&rdquo;)</li>
	<li>
		Bets were one of the red/green, even/odd options (which wins about 47.3% and pays 1&nbsp;to 1)</li>
	<li>
		The gambler played for about 4 hours at a lively pace of <a href="http://www.mahalo.com/answers/on-average-how-many-times-per-hour-does-single-roulette-wheel-spin">60+ games per hour</a> (for a total of 250 rounds)</li>
	<li>
		The gambler consistently wagered $5 per round</li>
</ul>
<p>I know these would probably not match reality, but that&rsquo;s okay.&nbsp; The assumptions are clear and the analysis could be updated as the assumptions are updated.&nbsp;&nbsp; Point being, it only matters that the analysis matches the assumptions and that we can update the the assumptions (and the model). &nbsp;The analysis could be redone with the odds from any game, or the analysis could combine multiple games played during a casino visit.&nbsp; I&rsquo;m just trying to keep this simple.</p>
<p>My answer to the original question would start out with &ldquo;given the assumptions&hellip;&rdquo; and say something like this:</p>
<ul>
	<li>
		The gambler would leave with less money than they started with around 78% of the time</li>
	<li>
		About half the time, the gambler would lose more than $70</li>
	<li>
		10% of the time, the gambler would lose more than $170</li>
	<li>
		10% of the time, the gambler would win more than $40</li>
</ul>
<p>Since we have to answer similar questions regardless of methods used (everyone makes risk-based statements regardless of what they call it), I challenged my skeptical colleague to answer the question in his way and his answer was simple.&nbsp; He would advise the gambler to look at the casino itself, because it logically means they take more money than they give out.&nbsp;&nbsp; While true, there is a large amount of uncertainty in that statement and lacks any feedback or ability to learn over time.&nbsp; We can do better.</p>
<h3>
	A Better Gambling Story</h3>
<p>Pure games of chance (like roulette) have loads of variability and almost zero uncertainty since it&rsquo;s in the house&rsquo;s interest to make the games as unbiased as possible.&nbsp; This makes them ripe for some simple models and allows us to create a better story.&nbsp;&nbsp; Plus, by telling a gambler that they&rsquo;ll lose more than they win isn&rsquo;t very helpful, and may erode (or fail to build) trust, especially when the gambler walks away with money.&nbsp;</p>
<p>My solution is to model visits the casino repeatedly and see how the gambler does (a method known as Monte&nbsp; Carlo).&nbsp; I set up the model to play Roulette 250 times per visit, betting on the 1 to 1 payout options, and record the offset in cash for the gambler over the visit, then I set the model to run 10,000 times.&nbsp; Finally, I made a pretty picture (with red, yellow and green of course) that showed the trends over the 250 iterations (left to right).&nbsp; By looking at this we <a href="/images/final-10k2.png"><img align="right" alt="final-10k2" border="0" height="244" src="/images/final-10k2_thumb.png" style="background-image: none; border-right-width: 0px; padding-left: 0px; padding-right: 0px; display: inline; float: right; border-top-width: 0px; border-bottom-width: 0px; border-left-width: 0px; padding-top: 0px" title="final-10k2" width="244" /></a>can get a sense of the individual stories here.&nbsp; For example, there&rsquo;s a red line that hovers around $50 early in the visit (around rounds 40-70) and then ends up dipping down for a loss around $200 (sound familiar?)&nbsp; Overall though, this should help inform the simple roulette gambler</p>
<p>So, can I tell my colleague exactly how much he&rsquo;ll walk out of the casino with?&nbsp; Absolutely not, nobody can.&nbsp; But given the correct assumptions we can make some statements of probability that reduce the gambler&rsquo;s uncertainty better than other methods (including the de facto unaided intuition).&nbsp; This is an important point: it&rsquo;s not that statistics and math is going to convert lead into gold, but it will be better and more consistent than alternatives.&nbsp; We cannot lose sight of that.&nbsp; It will always be possible to poke the models (and some really deserve to be poked), but we should not tear down a solution just to replace it with something worse.&nbsp;</p>


