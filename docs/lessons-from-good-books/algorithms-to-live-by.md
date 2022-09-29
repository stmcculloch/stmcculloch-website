---
sidebar_position: 1
---

# Algorithms to Live by

## 1. Optimal Stopping

:::tip Quote

Inaction is just as irrevocable as action.

Spend 37% of the time evaluating, then immediately commit to the first option that is the best so far.

:::

If you need to decide on something, and you see options one-by-one and can't go back, spend the first 37% of the sample size just evaluating and seeing what's out there.

For example, if you want to buy a house, and expect to see 10 houses total, visit the first 4 with no intention of buying (don't even bring the chequebook), and then as soon as a house appears that's better than any other of the available options,  buy that house immediately.

If you can go back after seeing an option with a 50% chance of previously seen options being available to you, the stopping percentage raises to about 60%. For example, when dating, if 50% of previous dating partners would be willing to get back together, then spend the first 60% of the total sample "just looking".

[Read more about optimal stopping](https://en.wikipedia.org/wiki/Optimal_stopping)

## 2. Explore vs. Exploit

:::tip Quote

“It’s fairly intuitive that never exploring is no way to live. But it’s also worth mentioning that never exploiting can be every bit as bad. In the computer science definition, exploitation actually comes to characterize many of what we consider to be life’s best moments. A family gathering together on the holidays is exploitation. So is a bookworm settling into a reading chair with a hot cup of coffee and a beloved favorite, or a band playing their greatest hits to a crowd of adoring fans, or a couple that has stood the test of time dancing to “their song.”

:::

Explore = gathering information
Exploit = using information

Start off by exploring. Finish by exploiting. Gradually fade Explore into Exploit. The value of exploring goes down over time, because the opportunities to savor it dwindle. The value of exploiting goes up over time.

If one option is provably better than another, be prepared to completely ditch the worse optiion. Never bet "tails" on a coin biased towards "heads".

Seizing the day and seizing a lifetime are two entirely different endeavors. When balancing favorite experiences and new ones, nothing matters more than the interval over which we plan to enjoy them. Explore early and explore lots, so you can find the best stuff to exploit forever after.

Exploring has intrinsic value.

:::tip Quote

“The old adage tells us that “the grass is always greener on the other side of the fence,” but the math tells us why: the unknown has a chance of being better, even if we actually expect it to be no different, or if it’s just as likely to be worse.”

:::


## 3. Sorting

:::tip Quote

“Sorting something that you will never search is a complete waste; searching something you never sorted is merely inefficient.”

:::

Merge sort: It is much easier to sort 5 bookshelves of 10 books each (5\*10^2 = 500 comparisons), than 1 bookshelf of 50 books (50^2 = 2500 comparisons).
n*log(n) is much better than n^2. Split large data sets into smaller data sets. Sort individually recombine at the end.

Sorting isn't always worth it. 
Sort books by category, but not also alphabetically by title. Make multiple rough, unsorted groups.
Sorting requires slow hands. Searching uses fast eyes (or computers).

Race vs. Tournament. Score everyone by a metric, and the list is self-sorting. Tournaments just tell you who's best. Races tell you "by how much".
In single knockout tournaments, silver medals can be misleading. The true second place person could have lost to the 1st place person in round 1.

## 4. Caching

:::tip Quote

"Forgetting can be just as important as remembering."

“We say “brain fart” when we should really say “cache miss.”

:::

Use a storage heirarchy. Put commonly used items in accessible locations. Put occasionally-used items out of sight in long-term storage.


For example, my tools: (from most commonly used to least commonly used)
- Desk (pens, paper, eraser, soldering station, garbage can)
- Toolchest (screwdrivers, nuts/bolts/etc)
- Attic (spare 3D printer parts)
- Self-storage locker (motorcycle in the winter)

Put most recently used items at the front of the list to reduce searching. 

:::tip Steven super tip

When using Windows OS, I make use of the "Quick access" folder all of the time. All your most recently used files are available there!

:::

Avoid completely discarding items that are important but rarely used. E.g. birth certificate. Long term storage is good but don't lose track of things!

## 5. Scheduling

:::tip Quotes

"How we spend our days is how we spend our lives."

"We are what we repeatedly do."

:::

When deciding what to do, **Earliest Deadline First (EDF)** is optimal. And intuitive. Assuming all tasks are equal priority.

Even better: **Weighted Completion Times (WCT)**. Divide weight of each task by the time to complete. Work by highest result per unit of time. This reduces the total weight.

:::tip Steven super tip

WCT got me through university! An assignment is worth only 2% of your grade, but takes 10 hours to complete? Just don't do it. Spend that time studying for the final which is worth 50% of your grade. It's OK to use the "triage" approach. With limited resources, low weight-per-time tasks must die.

:::

**Interrupt Coalescing**. Check email 1x per day. Check messages at morning/lunch/dinner. This avoids the cost of "context switching". Time for "deep work" is valuable. Make time for it. Be aware of the tradeoff between responsiveness & throughput.

**Priority Inversion** Never let a low-priority task block a high priority task. For example, don't disassemble your computer to clean the dust off, if you also have to write a thesis paper on that same computer. You won't be able to work on the high-priority task until the low-priority task has been completed. If a low-priority task ever blocks a high-priority task, then **priority inheritance** should occur, and the low-priority task should become just as important as the high priority task.

Sometimes, it is better to repeat a task unnecessarily, than to check if it has already been done. 

## 6. Bayes Rule

:::tip Quote

“Bayes’s Rule tells us that when it comes to making predictions based on limited evidence, few things are as important as having good priors—that is, a sense of the distribution from which we expect that evidence to have come. Good predictions thus begin with having good instincts about when we’re dealing with a normal distribution and when with a power-law distribution. As it turns out, Bayes’s Rule offers us a simple but dramatically different predictive rule of thumb for each.  …”

:::

Two types of things:
- Things that tend towards and cluster around a natural value (human lifespan).
- Things that don’t. (Population of cities. Villages of 100, Towns of 10,000, and cities of 1,000,000. [Power distribution](https://www.statisticshowto.com/power-law/) )

## 7. Over-fitting

:::tip Quotes

"The simplest solution is usually the best solution" - Occam's Razor

“The greater the uncertainty, the bigger the gap between what you can measure and what matters, the more you should watch out for overfitting - that is, the more you should prefer simplicity”

:::

Sometimes it is better to think less about things. E.g. if you use a pros and cons list, only list the most important pros/cons. Don't get bogged down by insignificant details.

To avoid over-fitting, penalize complexity. A 2-factor model is often better than a 9-factor model. Capturing the trend is better than perfectly fitting the dataset. Save 20% of the dataset in order to 'test' the model.

## 8. Relaxation

If you have a hard problem to solve, solve an easier version of that problem. You might learn somthing new about the hard problem. To make a hard problem easier to solve, remove constraints. Let discrete values become continuous. 3.67 humans doesn't make any sense, but just round it to 4.

**Remove unnecessarily strict constraints.** It's OK if you sometimes need to move Taco Tuesday to a Wednesday in order to fit everything into your weekly schedule. You'll survive.

**Allow breaking of rules.** Sometimes it is worth dealing with some penalties, if it turns an intractable problem into a tractable one. Sometimes, you'll have to let some people down, or 'drop the ball' in order to maximize overall happiness. 

When solving a hard (possibly intractable) problem, accept that it will be impossible to find the optimal solution. Instead, define what "good enough" is, and aim for that instead. For example, when choosing a movie to watch on Netflix, there are 1000s of movies to choose from. Don't spend 1hr looking for a 10/10 movie. Spend 2 minutes to find an 8/10 movie.

[Here's a wonderful video about the travelling salesman problem](https://www.youtube.com/watch?v=GiDsjIBOVoA)

## 9. Randomness

:::tip Quote

"You often need to take 1 step back to take 2 steps forward"

:::

Don't get stuck at the top of a small hill. If you want to find the tallest mountain, you'll need to explore a lot. Randomness can help you explore.

Sometimes sampling by playing/trying is better than a mathematical solution.

Randomness is the best way of testing certain problems. Like Polynomial Identity test. Do two seemingly completely different functions give the same output with every value of 'x' tested? They are probably the same function. More likely the more values of 'x' you test.

Just randomly choosing an option can be a viable algorithm in some cases.

**Simluated Annealing:** Start off with a lot of randomness, and slowly 'cool down' until randomness drops to zero. This is good at getting closer to a "global maximum".

## 10. Networking

:::tip Quote

"Embrace the buffer"

:::

**Exponential back-off:** The algorithm of forgiveness. Keeping in touch with a flaky friend? Invite them using this schedule: 
- Send an invitation on week 1
- If declined, send another in 2 weeks.
- If declined, send another in 4 weeks,
- If declined, send another in 8 weeks.

Never go out of touch with them, but every non-response makes the wait time 2x longer next time you try contacting them.

**Buffers** Having 'give' in a system makes it much more robust.
- Buffers don't work if the buffer is constantly full. Make sure inflow < outflow.
- A big buffer isn't always a good thing. Things in a big buffer spend a longer time waiting, and you'll have a lot more work waiting for you.
- E.g. Your email inbox is overflowing with work as soon as you get back from a vacation.
- In the past, we had to knock on our friend's door. If they didn't answer, too bad. Now we can just send a message, and expect a reply eventually.
- Buffer bloat is real. Sometimes it is best to just 'drop' packets that exceed the length of the buffer.

:::tip Super Steven Tip

When driving, if you want to save gas, use a big buffer between your car and the car in front. Therefore, if you need to slow down, you can just ease off the gas instead of pumping the brakes. (This is why stop-and-start traffic uses more gas than highway driving, per km). 

Also, if you can,  brake early when approaching a red light, so that you don't have to come to a complete stop.

 [Read more driving efficiency tips](../tips-for-maximum-efficiency/fuel-efficient-driving-techniques) 

:::

## 11. Game Theory

When playing a game (e.g. poker) you should try to play just 'one level ahead' of your opponent. "only a fool would bluff here, which is exactly why he won't ever expect it when I bluff him! But of course, he knows that I know that he knows that I know...." Don't get too bogged down by recursion.

When in doubt, return to the "Nash Equilibrium" or the optimal strategy going by first principles.


Seek out games where honesty wins. E.g. Vickrey sealed bid auctions, where the optimal strategy is bidding exactly what you think the item is worth.
**Mechanism design. When the game sucks, change the game.** 

Ask "what rules will create the behavior we want"


Sometimes, 'harsh' rules can result in a better outcome for everyone. For example, Evernote CEO offers employees $1000 to take a vacation. Bad move. Better is to change the rules to force compulsory 2 weeks vacation.

Another example. Godfather says "if you rat out your partner, we'll kill you". Turns the [prinsoner's dilemma](https://en.wikipedia.org/wiki/Prisoner%27s_dilemma) into a game of forced cooperation (both prisoners are compelled to stay quiet, ensuring they both go free and split the loot). Otherwise, it is always in their best interest to selfishly rat the other guy out.

Another example. Living in a society. If everyone takes slightly more than their fair share of the pie, the person at the end of the line will starve. Forcing everyone to only take their fair share results in maximum happiness.

Another example. Overfishing. Forcing a company to catch less fish in a single year will mean more total fish in the long run.


## Conclusion

:::tip Quote 

“Seemingly innocuous language like 'Oh, I'm flexible' or 'What do you want to do tonight?' has a dark computational underbelly that should make you think twice. It has the veneer of kindness about it, but it does two deeply alarming things. First, it passes the cognitive buck: 'Here's a problem, you handle it.' Second, by not stating your preferences, it invites the others to simulate or imagine them. And as we have seen, the simulation of the minds of others is one of the biggest computational challenges a mind (or machine) can ever face.”

:::

Don't make people solve open-ended problems. Whenever possible, give them a constrained yes/no decision rather than forcing them to solve a travelling salesman problem in their head.

E.g. "Want to grab coffee Sunday at 1 PM?"

is **way** better than

"Let's grab coffee this week, let me know when is most convenient for you"

State your preferences instead of saying "I'm flexible". Play your own music for the group every once in a while. Most people are happy when you make decisions for them, especially if they also have no particular preferences. 