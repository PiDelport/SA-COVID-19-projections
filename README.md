> **⚠️ Disclaimer:** I am not a medical professional or epidemiologist.
> This analysis is not necessarily reliable.
>
> See the official [NICD] and [SA Coronavirus] websites for reliable information.

[NICD]: http://www.nicd.ac.za/
[SA Coronavirus]: https://sacoronavirus.co.za/

# South Africa COVID-19 data and projections

This analysis of public data about the [2020 coronavirus pandemic in South Africa] tries to answer two questions:

[2020 coronavirus pandemic in South Africa]: https://en.wikipedia.org/wiki/2020_coronavirus_pandemic_in_South_Africa

1. Where are we now? Is the infection slowing down? Are our efforts working?

2. What's ahead? When will the infection peak, and when might it be over?


> ℹ️ **Note:** You can click on charts below to see bigger interactive versions on Google Sheets,
> along with the underlying data and calculations.


## Where are we now?

We can expect that infections will roughly follow a [logistic growth curve],
so we can try to visualise where we are relative to that curve's inflection point, or midpoint.

[logistic growth curve]: https://calculus.subwiki.org/wiki/Logistic_function


### Growth factor

> 💡️ Video explanation: "[Exponential growth and epidemics]" by 3Blue1Brown

[Exponential growth and epidemics]: https://www.youtube.com/watch?v=Kas0tIxDvrg

The first way to look at this is to visualise the growth factor,
which is the second derivative (rate of change of rate of change) of the total cases over time,
or the ratio between new cases each day.

* **Growth factor > 1** means we are before the inflection point, in the exponential growth phase.
* **Growth factor = 1** means we are crossing inflection point, and growth is stabilising.
  Ideally, this should be the half-way mark, at roughly half the number of cases that the total will eventually grow to,
  and half the number of days from the first infection to the peak.
* **Growth factor < 1** means we have passed the inflection point, and growth is slowing down.

The data is noisy, so this chart includes several layers of smoothing over multiple days,
to make the overall trend clearer:

[![Growth factor chart]][Growth factor sheet]

[Growth factor chart]: https://docs.google.com/spreadsheets/d/e/2PACX-1vRXZDdEQoIMZ6Jvx_5He7SUCUAXAVdi5fcX0kOepif2403AKugwHZRz5PZ65VBzptsDdEyzJmF_k6Ie/pubchart?oid=759993482&format=image
[Growth factor sheet]: https://docs.google.com/spreadsheets/d/1zJC06iokpJ65-ZdJCgqCAIgpYpUTwOlpcxI_27wTtn8/edit#gid=1190480589

As of the start of the national lockdown (~27 March), the growth rate is dipping below 1,
but this is likely a temporary artifact of reporting, rather than a true inflection point.


### Trajectory of cases

> 💡️ Video explanation: "[How To Tell If We're Beating COVID-19]" by MinutePhysics

[How To Tell If We're Beating COVID-19]: https://www.youtube.com/watch?v=54XLXg4fYsc

The second way to look at this is to visualise the trajectory of new cases versus total cases.
This makes the exponential growth phase look linear, and clearly highlights when the curve begins to decelerate.

[![Trajectory chart]][Trajectory sheet]

[Trajectory chart]: https://docs.google.com/spreadsheets/d/e/2PACX-1vRXZDdEQoIMZ6Jvx_5He7SUCUAXAVdi5fcX0kOepif2403AKugwHZRz5PZ65VBzptsDdEyzJmF_k6Ie/pubchart?oid=1380291220&format=image
[Trajectory sheet]: https://docs.google.com/spreadsheets/d/1zJC06iokpJ65-ZdJCgqCAIgpYpUTwOlpcxI_27wTtn8/edit#gid=1534720164

[![Trajectories chart]][Trajectories sheet]

[Trajectories chart]: https://docs.google.com/spreadsheets/d/e/2PACX-1vRXZDdEQoIMZ6Jvx_5He7SUCUAXAVdi5fcX0kOepif2403AKugwHZRz5PZ65VBzptsDdEyzJmF_k6Ie/pubchart?oid=1965891821&format=image
[Trajectories sheet]: https://docs.google.com/spreadsheets/d/1zJC06iokpJ65-ZdJCgqCAIgpYpUTwOlpcxI_27wTtn8/edit#gid=1589648313

This shows the same temporary (?) dip after the start of the national lockdown.


## What's ahead?

We can estimate the progression of the infection over time by fitting a logistic growth curve to the data,
along with an estimate of the total infected population.

SACEMA and NICD present the following estimates for how many of South Africa's population will become infected:

* **10% infected** is an optimistic estimate, if early mitigation measures are effective.
* **20% infected** is typical for the seasonal flu (19%).
* **40% infected** is a more pessimistic estimate, if mitigation is slow or ineffective.

> 📰️ Source:
> "[The terrifying coronavirus projections that pushed govt into lockdown](https://www.news24.com/SouthAfrica/News/exclusive-the-terrifying-coronavirus-projections-that-pushed-government-into-lockdown-action-20200319)",
> News24, 19 March 2020

We can estimate the number of active cases by assuming an average recovery (or fatality) period,
and subtracting this from the infected cases.
Most sources cite **2.5 week** average recovery period, so we'll use that.

[![Projection chart]][Projection sheet]

[Projection chart]: https://docs.google.com/spreadsheets/d/e/2PACX-1vRXZDdEQoIMZ6Jvx_5He7SUCUAXAVdi5fcX0kOepif2403AKugwHZRz5PZ65VBzptsDdEyzJmF_k6Ie/pubchart?oid=719594516&format=image
[Projection sheet]: https://docs.google.com/spreadsheets/d/1zJC06iokpJ65-ZdJCgqCAIgpYpUTwOlpcxI_27wTtn8/edit#gid=1060653400

As of 5 April 2020, this gives us these reference points:

* **Inflection point:** 20 Jun – 3 Jul, with 2.9 – 11.8 million infections.
  This is when the growth rate peaks, and begins to slow down.

* **Active case peak:** 29 Jun – 12 Jul, with 2.5 – 10.1 million active cases.
  This is when the recovery (or fatality) rate overtakes the growth rate,
  and the number of cases begins to go down.

Zooming in on the shorter term:

[![Projection current week chart]][Projection current week sheet]

[Projection current week chart]: https://docs.google.com/spreadsheets/d/e/2PACX-1vRXZDdEQoIMZ6Jvx_5He7SUCUAXAVdi5fcX0kOepif2403AKugwHZRz5PZ65VBzptsDdEyzJmF_k6Ie/pubchart?oid=1121253821&format=image
[Projection current week sheet]: https://docs.google.com/spreadsheets/d/1zJC06iokpJ65-ZdJCgqCAIgpYpUTwOlpcxI_27wTtn8/edit#gid=649467783

[![Projection next 2 weeks chart]][Projection next 2 weeks sheet]

[Projection next 2 weeks chart]: https://docs.google.com/spreadsheets/d/e/2PACX-1vRXZDdEQoIMZ6Jvx_5He7SUCUAXAVdi5fcX0kOepif2403AKugwHZRz5PZ65VBzptsDdEyzJmF_k6Ie/pubchart?oid=765685532&format=image
[Projection next 2 weeks sheet]: https://docs.google.com/spreadsheets/d/1zJC06iokpJ65-ZdJCgqCAIgpYpUTwOlpcxI_27wTtn8/edit#gid=2143156717

### Lockdown period

On 23 March, South Africa declared a 3 week [national lockdown] from 26 March to 16 April 2020.

[national lockdown]: https://en.wikipedia.org/wiki/2020_coronavirus_pandemic_in_South_Africa#National_lockdown

Projections for this lockdown period, as of 27 Mar 2020 (with cases **confirmed** and _projected_):

| Date   | Lockdown |       Cases       |
|-------:|----------|:-----------------:|
| 26 Mar | Week 0   |      **927**      |
|  2 Apr | Week 1   |     **1,462**     |
|  9 Apr | Week 2   |      _3,011_      |
| 16 Apr | Week 3   |  _6,296 – 6,299_  |


## Related work

### South Africa

* [Data Repository](https://github.com/dsfsi/covid19za) and
  [Dashboard](https://bitly.com/covid19za-dash)
  by the Data Science for Social Impact Research Group @ University of Pretoria

* [Dashboard](https://datastudio.google.com/u/0/reporting/15817068-62f2-4101-8e0f-385e2ddd9326/page/wI9JB)
  by Wits University, iThemba LABS, and DataConvergence.

* [Dashboard](https://health.hydra.africa/) by The Awareness Company

### International

* [Covid Trends](https://aatishb.com/covidtrends/) by Aatish Bhatia and MinutePhysics
