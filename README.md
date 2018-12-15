# Multiple Regression: Automotive Deaths by County

### Which attributes, of a US county, correlate to the rate of motor vehicle deaths in that county?

<p>
  <img src="https://photos.app.goo.gl/q5Q8BcUhwagx8wTm9" width="500" title="datausa.io">
</p>

This was our first crack at a building a multiple linear regression model, just to see how it's done and get some practice.

After parsing through some funky data from New York State's **solar panel installation** tax incentive program (https://www.nyserda.ny.gov/All-Programs/Programs/NY-Sun/Data-and-Trends), we realized that said data was not indicative of more general solar panel adoption trends, so we went looking for other data to play with.

A classmate turned us towards (https://datausa.io/map/?level=county&key=uninsured). The next dependent variable we considered was **alcohol-related** motor vehicle deaths, but the values provided were just percentages of the total number of motor vehicle related deaths **involving alcohol** per county (of all motor vehicle deaths? wasn't clear if these were from the samem measurement), so we weren't sure if we could use that to extrapolate an actual number.

For the sake of time, we went with a simpler metric: Given some demographic and other attributes of a county, could we predict the number of plain old motor vehicle deaths that will happen in a year in that county? Could we do better than just guessing the average for every county? Tl;dr: Yes, linear regression works.

#### Outline:
1. Data fetching and cleaning
2. Checking for normality and any colinearity
3. Splitting and Scaling the data
4. Making a baseline model
5. Making improved models¶
