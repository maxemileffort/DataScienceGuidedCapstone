# Guided Capstone Project Report 

![](image.png)

## Intro
From the brief:

The resort's pricing strategy has been to charge a premium above the average price of
resorts in its market segment. They know there are limitations to this approach. There's
a suspicion that Big Mountain (BM) is not capitalizing on its facilities as much as it could.
Basing their pricing on just the market average does not provide the business with a
good sense of how important some facilities are compared to others. This hampers
investment strategy. BM has brought in a data science team to implement a
more data-driven business strategy. The business wants some guidance on how to
select a better value for their ticket price. They are also considering a number of
changes that they hope will either cut costs without undermining the ticket price or will
support an even higher ticket price.

## Initial Analyis

### Figures

> Fig 1. Most important model features
![Most important model features](https://github.com/maxemileffort/DataScienceGuidedCapstone/blob/master/images/most%20important%20model%20features.jpg)
> Fig 2. Heat Map for Correlations
![Heat Map for Correlations](https://github.com/maxemileffort/DataScienceGuidedCapstone/blob/master/images/corr%20heatmap.jpg)

### Talking Points

Initially, we were missing a few critical pieces of data:

- visitor numbers
- how many tickets they buy
- operating costs, past and projected
- revenue, past and projected



## Modeling

### Figures

![Ticket Price, All resorts](https://github.com/maxemileffort/DataScienceGuidedCapstone/blob/master/images/ticket%20price%2C%20all%20resorts.jpg)
![Ticket Price, Montana Only](https://github.com/maxemileffort/DataScienceGuidedCapstone/blob/master/images/ticket%20price%2C%20montana%20only.jpg)
![Fast Quads](https://github.com/maxemileffort/DataScienceGuidedCapstone/blob/master/images/fast%20quads.jpg)
![Longest Run](https://github.com/maxemileffort/DataScienceGuidedCapstone/blob/master/images/longest%20run.jpg)
![Number of Chairs](https://github.com/maxemileffort/DataScienceGuidedCapstone/blob/master/images/num%20of%20chairs.jpg)
![Number of Runs](https://github.com/maxemileffort/DataScienceGuidedCapstone/blob/master/images/num%20of%20runs.jpg)
![Skiable Terrain](https://github.com/maxemileffort/DataScienceGuidedCapstone/blob/master/images/skiable%20terrain.jpg)
![Area Covered by Snow Makers ](https://github.com/maxemileffort/DataScienceGuidedCapstone/blob/master/images/snow%20area.jpg)
![Vertical Drop](https://github.com/maxemileffort/DataScienceGuidedCapstone/blob/master/images/vertical%20drop%2C%20all%20resorts.jpg)
![Run Closures](https://github.com/maxemileffort/DataScienceGuidedCapstone/blob/master/images/effect%20of%20closed%20runs.jpg)

### Talking Points

Big mountain currently charges 81 USD, which is at the top end for prices in Montana, 
and roughly the top 3rd for the rest of the country. Our model shows that they could 
charge almost 96 USD, and still be within prices explained by the data. What that tells 
us though, is not necessarily to charge 96 USD, but that there is definitely room for the prices 
to go up.

After receiving some more data from BM about expected visitors and average # of 
tickets those visitors buy, we were able to get a much better idea of expected revenue 
in relation to the cost of the new lift that was installed for this season. With a tiny 
price increase of 2 USD, the lift will be more than paid for just this season.

## Recommendations

It seems that BM's arbitrary pricing has held them back for a while. In the brief, it 
stated they just took some average price from their 'market segment' (probably the 
average price for the state) and added a premium on top. Which sounds OK in theory, seeing 
as how they offered more of just about everything than all the other resorts in the state.

But the data tells a better story! They've apparently been shooting themselves in the 
foot, price wise. Compared to resorts with similar attributes but in other states, they've been 
under charging by around 15 USD per ticket, which is an order of magnitude off. Assuming they 
still bring in 350k visitors, with a 95 USD ticket, that's a 15 million USD difference to their 
bottom line. If their jaws don't hit the floor for that, I'd ask them, "Does that surprise 
anyone in the room?"

Even before any price increase, BM is the most expensive in Montana. But they are also 
bringing the most to the table, as far as runs, skiiable terrain, vertical drop, number 
of runs, etc. The 2 USD increase is only a 2.5\% increase in price, but results in just 
under 3.5 million USD in additional revenue.

So as long as the rest of the operating costs are at most break even, or that BM is OK with 
closing some runs for a few days to lower operating costs, this season should also be profitable!

It would be nice to know operating costs before the new lift went in. Especially if they 
could be narrowed down to payroll, equipment, cost per run (if they differed), etc. That way 
the numbers could be explained in terms of profit, instead of just pure revenue numbers.

In the event industry, they say if you sell out something like a concert (what's a concert? 
Oh, Covid.), then ticket prices probably could have been doubled. Even if half the people 
don't show up with the higher ticket prices, the operating cost goes down (less cleaning, 
fewer staff, fewer supplies used), resulting in higher revenue.

So in BM's case, a price increase is absolutely justified, financially. They would probably want 
to connect the higher price correlated features to the benefits for the consumer ("Hey guys! Come check
out the resort with the most runs and most skiiable terrain in all of Montana!" or something). That 
way, in the visitor's mind, the higher cost is justified.

If the execs found it useful, I'd let them keep the model. Having a software background, I'd turn 
his into an intranet app for the business so that they could use it to play around with their pricing 
structure. That'd also probably bring a nice little premium to the data company that BM consulted 
for this analysis, with being able to license out the app or sell it for a lifetime use or something. 
I mean, that's a million dollars the app could bring in, if it makes a company another 15 million.

## Notes
In any case, that would be one of the critical components in deciding whether or not to price higher/lower 
and add more chairs to the resort.

States with more resorts in them, or more resorts per capita, were likely to charge middle of the road prices, 
which gives a nice floor concerning Montana's data. Adding other features (like the lift that Big Mountain added) 
should theoretically add to the ceiling for ticket prices, because skiers will have less down time between runs 
due to large crowds, which common sense dicatates would be a major selling point.

That being said, the data shows a point of diminishing returns as far as total chairs go, so then the next investment 
I think would probably be lights, as night skiing seems like it helped other resorts charge higher prices as well.

The first thing that happened was that we took a stab at guessing if the mean of prices would be a good 
predictor for the model. As it turns out, that was a very solid choice, model-wise. As for the Big Mountain's 
pricing strategy, it probably falls a little short, since it puts pricing in the middle of the pack.

After imputing some missing values (using both the mean and the median), we started with a linear regression model. 
Our initial model was a bit worse than our first guess, though. After some tuning cross validation, this model at 
least came into range of the guess with the average, but still off by ~$2.

So another model was tried: random forest regression. Initially, it was much closer at predicting price, relative 
to the guess with the mean. After tuning with cross validation, the differences were almost none.

Based on all of that, it seems like random forest is the way to go. The random forest model also pointed out that the 
most important features as they correlate with price were total drop, number of runs, fast quads, and snow making. 
So those might be initial insights for the business, as well as something to dive deeper into for the next section.



