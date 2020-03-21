# South Africa COVID-19 data and projections

(Click on the charts below to view bigger interactive versions, and the underlying data.)

## Cases

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

This projects the number of confirmed cases into the future by fitting the curve to the logistic function. 


[![Projection]][Projection sheet]

[Projection]: https://docs.google.com/spreadsheets/d/e/2PACX-1vRXZDdEQoIMZ6Jvx_5He7SUCUAXAVdi5fcX0kOepif2403AKugwHZRz5PZ65VBzptsDdEyzJmF_k6Ie/pubchart?oid=1322399407&format=image
[Projection sheet]: https://docs.google.com/spreadsheets/d/1zJC06iokpJ65-ZdJCgqCAIgpYpUTwOlpcxI_27wTtn8/edit#gid=384217832

(This only considers confirmed cases: the true number of unconfirmed, unreported, and undetected cases will be higher.)

## Related work

* https://github.com/dsfsi/covid19za
