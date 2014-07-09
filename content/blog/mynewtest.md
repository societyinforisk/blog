Title: Aggregating Risk Scenarios: put away the calculator.
Date: 2011-10-20 22:40:00
Category: Blog
Tags: Blog
Status: draft
Slug: aggregating-risk-scenarios
Author: Kevin Thompson (@bfist)

The other day I was thinking about how one might go about expressing the aggregate information risk of an organization.  Lately I find myself favoring a balanced scorecard approach to expressing risk, but even after breaking risk scenarios into several groups, you still need to aggregate them in some way.  So how would one go about expressing the combined distribution of loss from several loss risk scenarios?

Let's make up a story to illustrate.  Lets say that you are going to go to your favorite amusement park in Minnesota.  Your mom is going to her favorite amusement park in California and your dear sweet grandmother is going to her favorite amusement park in Florida.  Each of you is going to bring $100 with you.  You all have an equal risk of being robbed, but your mother and grandmother are so paranoid that they wont go unless you promise to reimburse them for any robbery they suffer.  If any of you are robbed you know that the robber will get at least $1 and no more than $100.  So you could express each risk scenario as a uniform distribution with a minimum of $1 and a maximum of $100.  But what is your total risk exposure?

Your total risk exposure is $300 because you have three risks with a maximum loss of $100.  But we usually do not want to express what is possible, we want to express what is probable.  You might want to express risk out to the 95th percentile or the 99th percentile.  The total exposure number is actually quite rare.  How rare?  There is a 1% chance that one of you will be robbed for $100.  Since these events are independent, the probability of two of you being robbed for $100 is 1% of 1% or .01%.  The probability of all three of you being robbed for $100 is .0001% or once every million trips to the amusement park.  And even that is assuming that all three of you will certainly be robbed!

The same effect happens on the minimum side of the aggregate risk distribution for the same reason.  I ran a monte carlo simulation with these three scenarios with 5000 samples.  Even after 5000 samples I couldn't get a minimum value less than 11.  In fact, only 10% of the simulations had less than $85 for the aggregate loss.  What you're seeing here is the Central Limit Theorem at work.  When we combine three uniform distributions, we get a result that starts to look more like a normal distribution.  The graphic here shows the outcome of adding these three loss distributions together.  The effect becomes even more pronounced when the distributions aren't uniform.  If we had used a Pert distribution to describe each of the losses with a most likely loss of $30 then the effect is even greater.  I never saw a loss less than $22 or more than $228.  If you wanted to have enough cash to cover your losses for 95% of the trips to the amusement park, I would only need to have $164.

<img alt="Aggregate of three uniform distributions" src="http://mavdisk.mnsu.edu/kevin/totalloss.png" style="width: 622px; height: 402px;" />

So if you're going to be aggregating the loss from several risk simulations then the tool of choice is not a calculator, but another simulation.  The aggregate risk becomes a simulation where each of the inputs is the output of a risk scenario.  That way you can more accurately express what is probable rather than what is possible.
