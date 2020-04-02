# South Africa COVID-19 data and projections

(Click on the charts below to view bigger interactive versions, and the underlying data.)

## ⚠️ Disclaimer ⚠️

This is my personal analysis of the COVID-19 pandemic data,
but I am **not** a medical professional or epidemiologist.
Do not rely on this analysis for critical decisions.

For reliable information, refer to [NICD](http://www.nicd.ac.za/).


## Growth factor

_(Inspiration: [Exponential growth and epidemics](https://www.youtube.com/watch?v=Kas0tIxDvrg), 3Blue1Brown)_

This derivative indicates where we are relative to the inflection point of logistic growth.

* **Growth factor > 1** means we are before the inflection point, in the exponential growth phase.
* **Growth factor = 1** means we are crossing inflection point, and growth is stabilising.
  Ideally, this should be the half-way mark, at roughly half the number of cases that the total will eventually grow to,
  and half the number of days from the first infection to the peak.
* **Growth factor < 1** means we have passed the inflection point, and growth is slowing down.

(The data is noisy, so the charts below include several layers of smoothing over multiple days,
to make the overall trend clearer.)

[![Growth factor SA]][Growth factor SA sheet]

[Growth factor SA]: https://docs.google.com/spreadsheets/d/e/2PACX-1vRXZDdEQoIMZ6Jvx_5He7SUCUAXAVdi5fcX0kOepif2403AKugwHZRz5PZ65VBzptsDdEyzJmF_k6Ie/pubchart?oid=759993482&format=image
[Growth factor SA sheet]: https://docs.google.com/spreadsheets/d/1zJC06iokpJ65-ZdJCgqCAIgpYpUTwOlpcxI_27wTtn8/edit#gid=1190480589

This is a critical graph to keep an eye on: as long as it stays above 1,
we are still in the early exponential phase of the infection.

<!-- Hide for now
[![Growth Factor WC]][Growth Factor WC sheet]

[Growth Factor WC]: https://docs.google.com/spreadsheets/d/e/2PACX-1vRXZDdEQoIMZ6Jvx_5He7SUCUAXAVdi5fcX0kOepif2403AKugwHZRz5PZ65VBzptsDdEyzJmF_k6Ie/pubchart?oid=1440192137&format=image
[Growth Factor WC sheet]: https://docs.google.com/spreadsheets/d/1zJC06iokpJ65-ZdJCgqCAIgpYpUTwOlpcxI_27wTtn8/edit#gid=473566654
-->


## Projections

We can estimate the progression of the infection over time by fitting a logistic growth curve to the data,
along with an estimate of the total infected population.

SACEMA and NICD present the following estimates for how many of South Africa's population will become infected:

* **10% infected** is an optimistic estimate, if early mitigation measures are effective.
* **20% infected** is typical for the seasonal flu (19%).
* **40% infected** is a more pessimistic estimate, if mitigation is slow or ineffective.

_(Source: [The terrifying coronavirus projections that pushed govt into lockdown][1], News24, 2020-03-19)_

[1]: https://www.news24.com/SouthAfrica/News/exclusive-the-terrifying-coronavirus-projections-that-pushed-government-into-lockdown-action-20200319

We can estimate the number of active cases by assuming an average recovery (or fatality) period,
and subtracting this from the infected cases.
Most sources cite **2.5 week** average recovery period, so we'll use that.

[![Projection]][Projection sheet]

[Projection]: https://docs.google.com/spreadsheets/d/e/2PACX-1vRXZDdEQoIMZ6Jvx_5He7SUCUAXAVdi5fcX0kOepif2403AKugwHZRz5PZ65VBzptsDdEyzJmF_k6Ie/pubchart?oid=719594516&format=image
[Projection sheet]: https://docs.google.com/spreadsheets/d/1zJC06iokpJ65-ZdJCgqCAIgpYpUTwOlpcxI_27wTtn8/edit#gid=1060653400

As of 2 April 2020, this gives us these reference points:

* **Inflection point:** 2 – 13 Jun, with 3–12 million infections.
  This is when the growth rate peaks, and begins to slow down.

* **Active case peak:** 11 – 22 Jun, with 3–12 million active cases.
  This is when the recovery (or fatality) rate overtakes the growth rate,
  and the number of cases begins to go down.

Zooming in on the shorter term:

[![Projection current week]][Projection current week sheet]

[Projection current week]: https://docs.google.com/spreadsheets/d/e/2PACX-1vRXZDdEQoIMZ6Jvx_5He7SUCUAXAVdi5fcX0kOepif2403AKugwHZRz5PZ65VBzptsDdEyzJmF_k6Ie/pubchart?oid=1121253821&format=image
[Projection current week sheet]: https://docs.google.com/spreadsheets/d/1zJC06iokpJ65-ZdJCgqCAIgpYpUTwOlpcxI_27wTtn8/edit#gid=649467783

[![Projection next 2 weeks]][Projection next 2 weeks sheet]

[Projection next 2 weeks]: https://docs.google.com/spreadsheets/d/e/2PACX-1vRXZDdEQoIMZ6Jvx_5He7SUCUAXAVdi5fcX0kOepif2403AKugwHZRz5PZ65VBzptsDdEyzJmF_k6Ie/pubchart?oid=765685532&format=image
[Projection next 2 weeks sheet]: https://docs.google.com/spreadsheets/d/1zJC06iokpJ65-ZdJCgqCAIgpYpUTwOlpcxI_27wTtn8/edit#gid=2143156717

## Lockdown period

On 23 March, South Africa declared a 3 week [national lockdown], from 26 March to 16 April 2020.

[national lockdown]: https://en.wikipedia.org/wiki/2020_coronavirus_pandemic_in_South_Africa#National_lockdown

Projections for this lockdown period, as of 27 Mar 2020 (with cases **confirmed** and _projected_):

| Date   | Lockdown |       Cases       |
|-------:|----------|:-----------------:|
| 26 Mar | Week 0   |      **927**      |
|  2 Apr | Week 1   |     **1,761**     |
|  9 Apr | Week 2   |  _4,409 – 4,410_  |
| 16 Apr | Week 3   | _11,030 – 11,041_ |


## Related work

* https://github.com/dsfsi/covid19za
