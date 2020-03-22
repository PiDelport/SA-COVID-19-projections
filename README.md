# South Africa COVID-19 data and projections

(Click on the charts below to view bigger interactive versions, and the underlying data.)

## Cases

The number of confirmed cases over time, broken down by province, in order of first appearance.

[![Cases]][Cases sheet]

[Cases]: https://docs.google.com/spreadsheets/d/e/2PACX-1vRXZDdEQoIMZ6Jvx_5He7SUCUAXAVdi5fcX0kOepif2403AKugwHZRz5PZ65VBzptsDdEyzJmF_k6Ie/pubchart?oid=1959488780&format=image
[Cases sheet]: https://docs.google.com/spreadsheets/d/1zJC06iokpJ65-ZdJCgqCAIgpYpUTwOlpcxI_27wTtn8/edit#gid=658827335

[![Case %]][Case % sheet]

[Case %]: https://docs.google.com/spreadsheets/d/e/2PACX-1vRXZDdEQoIMZ6Jvx_5He7SUCUAXAVdi5fcX0kOepif2403AKugwHZRz5PZ65VBzptsDdEyzJmF_k6Ie/pubchart?oid=291377335&format=image
[Case % sheet]: https://docs.google.com/spreadsheets/d/1zJC06iokpJ65-ZdJCgqCAIgpYpUTwOlpcxI_27wTtn8/edit#gid=108384335


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

[![Growth Factor WC]][Growth Factor WC sheet]

[Growth Factor WC]: https://docs.google.com/spreadsheets/d/e/2PACX-1vRXZDdEQoIMZ6Jvx_5He7SUCUAXAVdi5fcX0kOepif2403AKugwHZRz5PZ65VBzptsDdEyzJmF_k6Ie/pubchart?oid=1440192137&format=image
[Growth Factor WC sheet]: https://docs.google.com/spreadsheets/d/1zJC06iokpJ65-ZdJCgqCAIgpYpUTwOlpcxI_27wTtn8/edit#gid=473566654


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

This gives us a rough time frame:

* **Inflection point:** End April. This is when the growth rate peaks.
  We may reach 3–12 million infections at this point.

* **Active case peak:** Early to mid May, at 5–20 million active cases.
 This is when the recovery (or fatality) rate overtakes the growth rate,
 and the number of cases begins to go down.

Zooming in on the shorter term:

[![Projection zoomed]][Projection zoomed sheet]

[Projection zoomed]: https://docs.google.com/spreadsheets/d/e/2PACX-1vRXZDdEQoIMZ6Jvx_5He7SUCUAXAVdi5fcX0kOepif2403AKugwHZRz5PZ65VBzptsDdEyzJmF_k6Ie/pubchart?oid=1121253821&format=image
[Projection zoomed sheet]: https://docs.google.com/spreadsheets/d/1zJC06iokpJ65-ZdJCgqCAIgpYpUTwOlpcxI_27wTtn8/edit#gid=649467783


## Related work

* https://github.com/dsfsi/covid19za
