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

## Analyis

### Figures

> Fig 1. Most important model features

![Most important model features](https://github.com/maxemileffort/DataScienceGuidedCapstone/blob/master/images/most%20important%20model%20features.jpg)

> Fig 2. Heat Map for Correlations

![Heat Map for Correlations](https://github.com/maxemileffort/DataScienceGuidedCapstone/blob/master/images/corr%20heatmap.jpg)

### Talking Points

Initially, we were missing a few major pieces of data:

- visitor numbers
- how many tickets they buy
- operating costs, past and projected
- revenue, past and projected

Even without those, though, we were able to find some interesting correlations for price:
On the heatmap in Fig 2, we see that (indicated by the lighter squares) the most important 
features when deciding on price are Fast Quads, Runs, Snow Making, and Vertical Drop.

Our model confirms this (Fig 1), even with trying several other features as the basis for price.

More good news, BM ranks at the top in all of those categories (seen below) and even in the top 
for many resorts across the country.

## Modeling

### Figures

> Fig 3. Ticket prices, All resorts

![Ticket Price, All resorts](https://github.com/maxemileffort/DataScienceGuidedCapstone/blob/master/images/ticket%20price%2C%20all%20resorts.jpg)

> Fig 4. Ticket prices, Montana Only

![Ticket Price, Montana Only](https://github.com/maxemileffort/DataScienceGuidedCapstone/blob/master/images/ticket%20price%2C%20montana%20only.jpg)

> Fig 5. Fast Quads

![Fast Quads](https://github.com/maxemileffort/DataScienceGuidedCapstone/blob/master/images/fast%20quads.jpg)

> Fig 6. Longest Run

![Longest Run](https://github.com/maxemileffort/DataScienceGuidedCapstone/blob/master/images/longest%20run.jpg)

> Fig 7. Number of Chairs

![Number of Chairs](https://github.com/maxemileffort/DataScienceGuidedCapstone/blob/master/images/num%20of%20chairs.jpg)

> Fig 8. Number of Runs

![Number of Runs](https://github.com/maxemileffort/DataScienceGuidedCapstone/blob/master/images/num%20of%20runs.jpg)

> Fig 9. Skiable Terrain

![Skiable Terrain](https://github.com/maxemileffort/DataScienceGuidedCapstone/blob/master/images/skiable%20terrain.jpg)

> Fig 10. Area Covered by Snow Makers

![Area Covered by Snow Makers](https://github.com/maxemileffort/DataScienceGuidedCapstone/blob/master/images/snow%20area.jpg)

> Fig 11. Vertical Drop

![Vertical Drop](https://github.com/maxemileffort/DataScienceGuidedCapstone/blob/master/images/vertical%20drop%2C%20all%20resorts.jpg)

> Fig 12. Run Closures

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

A price increase that small should come as good news: with 7 easily marketable attributes,
pitching this price increase should be fairly easy for the marketing department. And if BM
elects to cut costs, Fig 12 will help them make that decision.

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