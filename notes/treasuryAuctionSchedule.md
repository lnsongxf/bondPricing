# Auction frequencies

| Maturity | Frequency    | Type                    | Day    | Re-open                                                     |
|----------|--------------|-------------------------|--------|-------------------------------------------------------------|
| 13 weeks | weekly       | bill (zero coupon)      | Monday | Every 13 week bill is a re-opening of a 26 week bill        |
| 26 weeks | weekly       | bill (zero coupon)      | Monday | Every fourth 26 week bill is a re-opening of a 52 week bill |
| 52 weeks | four weeks   | bill (zero coupon)      |        |                                                             |
| 2 years  | monthly      | notes (biannual coupon) |        |                                                             |
| 5 years  | quarterly    | notes (biannual coupon) |        |                                                             |
| 10 years | quarterly    | notes (biannual coupon) |        |                                                             |
| 30 years | semiannually | bonds (biannual coupon) |        |                                                             |

# Alternate auction schedule

<p><strong>Treasury  Auction Calendar</strong></p>
<p>Treasury auctions are held on a regular basis, generally as  follows:</p>
<table class="nyfed-table">
<tbody>
<tr>
<td>4-week bills</td>
<td>Weekly (Tuesdays)</td>
</tr>
<tr>
<td>13-week and 26-week bills</td>
<td>Weekly (Mondays)</td>
</tr>
<tr>
<td>52-week bills</td>
<td>Every 4 weeks (Tuesdays)</td>
</tr>
<tr>
<td>2-year notes</td>
<td>Monthly (End of month)</td>
</tr>
<tr>
<td>3-year notes</td>
<td>Monthly (Middle of month)</td>
</tr>
<tr>
<td>5-year notes</td>
<td>Monthly (End of month)</td>
</tr>
<tr>
<td>7-year notes</td>
<td>Monthly (End of month)</td>
</tr>
<tr>
<td>10-year notes</td>
<td>Monthly (Middle of month)</td>
</tr>
<tr>
<td>30-year bonds</td>
<td>Monthly (Middle of month)</td>
</tr>
<tr>
<td>5-year TIPS</td>
<td>Three times per year (Apr, Aug, Dec)</td>
</tr>
<tr>
<td>10-year TIPS</td>
<td>Bimonthly (Jan, Mar, May, Jul, Sep, Nov)</td>
</tr>
<tr>
<td>30-year TIPS</td>
<td>Three times per year (Feb, Jun, Oct)</td>
</tr>
<tr>
<td>2-year FRN</td>
<td>Monthly (End of month)</td>
</tr>
</tbody>
</table>

# Ceased maturities

- 20 year bond in 1986
- 4 year note in 1990
- 7 year note in 1993
- 3 year note in 1998

# References

- The Treasury and Securities Market: Overview and Recent Developments
- https://www.newyorkfed.org/aboutthefed/fedpoint/fed41.html

# Holidays in tentative auction schedule

Holiday - Monday, May 30, 2016 - Memorial Day
Holiday - Monday, July 04, 2016 - Independence Day
Holiday - Monday, September 05, 2016 - Labor Day
Holiday - Monday, October 10, 2016 - Columbus Day

# Conventions

From MATLAB Financial Toolbox documentation:

- The basis for Treasury bill interest calculation is actual/360

From https://www.newyorkfed.org/aboutthefed/fedpoint/fed07.html:

- bills are quoted at a discount from face value, with the discount
  expressed as an annual rate based on a 360-day year. 

From https://en.wikipedia.org/wiki/Talk:United_States_Treasury_security#Dubious:
- Actual/Actual, which is what you were expecting to see, is used by
  U.S. Treasury notes and bonds, but not bills. See the day count
  article for more details.


# Bond pricing

Large-scale framework:
- a lot of bonds
- a lot of days
- different yield curves

Bond price evolution:
- for each bond we need to determine all cash-flows (time consuming:
  only once!)
- for each date, we need to get durations to all outstanding
  cash-flows
- for all durations (varying number depending on outstanding
  cash-flows) we need to evaluate the respective yield curve

Coupon-rate determination: same yield curve, same durations, multiple
bonds (different coupon rates)
- determine cash-flow times
- determine durations (fix number in all calculations)
- evaluate yield curve at given durations
- get average yield as initial coupon-rate guess
- modify coupon-rates and hence cash-flows
