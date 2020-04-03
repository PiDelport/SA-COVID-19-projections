> **⚠️ Disclaimer:** I am not a medical professional or epidemiologist.
> Do not rely on this analysis for critical purposes.
>
> See the official [NICD] and [SA Coronavirus] websites for reliable information.

[NICD]: http://www.nicd.ac.za/
[SA Coronavirus]: https://sacoronavirus.co.za/

# South Africa COVID-19 data and projections

This is my attempt to analyse public data about the [2020 coronavirus pandemic in South Africa]
in order to answer two questions:

[2020 coronavirus pandemic in South Africa]: https://en.wikipedia.org/wiki/2020_coronavirus_pandemic_in_South_Africa

1. Where are we? Is it getting worse or better right now? Can we see light at the end of the tunnel yet?

2. What does the future look like?


> ℹ️ **Note:** You can click on charts below to see bigger interactive versions on Google Sheets,
> along with the underlying data and calculations.


## Where are we?

Infections will roughly follow a [logistic growth curve]:
we can try to determine where we are relative to the curve's inflection point (or midpoint).

[logistic growth curve]: https://calculus.subwiki.org/wiki/Logistic_function

### Growth factor

> 💡️ Video explanation: "[Exponential growth and epidemics]" by 3Blue1Brown

[Exponential growth and epidemics]: https://www.youtube.com/watch?v=Kas0tIxDvrg

The first way to look at this is by visualising the growth factor,
which is the second derivative (rate of change of rate of change) of the case numbers.

* **Growth factor > 1** means we are before the inflection point, in the exponential growth phase.
* **Growth factor = 1** means we are crossing inflection point, and growth is stabilising.
  Ideally, this should be the half-way mark, at roughly half the number of cases that the total will eventually grow to,
  and half the number of days from the first infection to the peak.
* **Growth factor < 1** means we have passed the inflection point, and growth is slowing down.

(The data is noisy, so the charts below include several layers of smoothing over multiple days,
to make the overall trend clearer.)

[![Growth factor chart]][Growth factor sheet]

[Growth factor chart]: https://docs.google.com/spreadsheets/d/e/2PACX-1vRXZDdEQoIMZ6Jvx_5He7SUCUAXAVdi5fcX0kOepif2403AKugwHZRz5PZ65VBzptsDdEyzJmF_k6Ie/pubchart?oid=759993482&format=image
[Growth factor sheet]: https://docs.google.com/spreadsheets/d/1zJC06iokpJ65-ZdJCgqCAIgpYpUTwOlpcxI_27wTtn8/edit#gid=1190480589

As long as this graph stays above 1, we are still in the exponential phase of the infection.


### Trajectory of cases

> 💡️ Video explanation: "[How To Tell If We're Beating COVID-19]" by MinutePhysics

[How To Tell If We're Beating COVID-19]: https://www.youtube.com/watch?v=54XLXg4fYsc

The second way to look at this is by visualising the trajectory of new cases to total cases.
This makes the exponential phase linear, and highlights when the curve drops out of it.

[![Trajectory chart]][Trajectory sheet]

[Trajectory chart]: https://docs.google.com/spreadsheets/d/e/2PACX-1vRXZDdEQoIMZ6Jvx_5He7SUCUAXAVdi5fcX0kOepif2403AKugwHZRz5PZ65VBzptsDdEyzJmF_k6Ie/pubchart?oid=1380291220&format=image
[Trajectory sheet]: https://docs.google.com/spreadsheets/d/1zJC06iokpJ65-ZdJCgqCAIgpYpUTwOlpcxI_27wTtn8/edit#gid=1534720164

[![Trajectory 2 chart]][Trajectory 2 sheet]

[Trajectory 2 chart]: https://docs.google.com/spreadsheets/d/e/2PACX-1vRXZDdEQoIMZ6Jvx_5He7SUCUAXAVdi5fcX0kOepif2403AKugwHZRz5PZ65VBzptsDdEyzJmF_k6Ie/pubchart?oid=1965891821&format=image
[Trajectory 2 sheet]: https://docs.google.com/spreadsheets/d/1zJC06iokpJ65-ZdJCgqCAIgpYpUTwOlpcxI_27wTtn8/edit#gid=1589648313


## Projections

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

[![Projection]][Projection sheet]

[Projection]: https://docs.google.com/spreadsheets/d/e/2PACX-1vRXZDdEQoIMZ6Jvx_5He7SUCUAXAVdi5fcX0kOepif2403AKugwHZRz5PZ65VBzptsDdEyzJmF_k6Ie/pubchart?oid=719594516&format=image
[Projection sheet]: https://docs.google.com/spreadsheets/d/1zJC06iokpJ65-ZdJCgqCAIgpYpUTwOlpcxI_27wTtn8/edit#gid=1060653400

As of 3 April 2020, this gives us these reference points:

* **Inflection point:** 8 – 20 Jun, with 3–12 million infections.
  This is when the growth rate peaks, and begins to slow down.

* **Active case peak:** 17 – 29 Jun, with 3–11 million active cases.
  This is when the recovery (or fatality) rate overtakes the growth rate,
  and the number of cases begins to go down.

Zooming in on the shorter term:

[![Projection current week]][Projection current week sheet]

[Projection current week]: https://docs.google.com/spreadsheets/d/e/2PACX-1vRXZDdEQoIMZ6Jvx_5He7SUCUAXAVdi5fcX0kOepif2403AKugwHZRz5PZ65VBzptsDdEyzJmF_k6Ie/pubchart?oid=1121253821&format=image
[Projection current week sheet]: https://docs.google.com/spreadsheets/d/1zJC06iokpJ65-ZdJCgqCAIgpYpUTwOlpcxI_27wTtn8/edit#gid=649467783

[![Projection next 2 weeks]][Projection next 2 weeks sheet]

[Projection next 2 weeks]: https://docs.google.com/spreadsheets/d/e/2PACX-1vRXZDdEQoIMZ6Jvx_5He7SUCUAXAVdi5fcX0kOepif2403AKugwHZRz5PZ65VBzptsDdEyzJmF_k6Ie/pubchart?oid=765685532&format=image
[Projection next 2 weeks sheet]: https://docs.google.com/spreadsheets/d/1zJC06iokpJ65-ZdJCgqCAIgpYpUTwOlpcxI_27wTtn8/edit#gid=2143156717

### Lockdown period

On 23 March, South Africa declared a 3 week [national lockdown] from 26 March to 16 April 2020.

[national lockdown]: https://en.wikipedia.org/wiki/2020_coronavirus_pandemic_in_South_Africa#National_lockdown

Projections for this lockdown period, as of 27 Mar 2020 (with cases **confirmed** and _projected_):

| Date   | Lockdown |       Cases       |
|-------:|----------|:-----------------:|
| 26 Mar | Week 0   |      **927**      |
|  2 Apr | Week 1   |     **1,462**     |
|  9 Apr | Week 2   |      _3,771_      |
| 16 Apr | Week 3   |  _8,776 – 8,782_  |


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
