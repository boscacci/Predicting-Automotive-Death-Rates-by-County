# Predicting Automotive Death Rates by County
An initial stab at multiple linear regression in Python.

### Which attributes, of US counties, correlate with their annual motor vehicle death rates?

![from datausa.io](/readme/map.png)

This was our first crack at a building a multiple linear regression model, just to see how it's done and get some practice.

After parsing through some funky data from New York State's **solar panel installation** tax incentive program (https://www.nyserda.ny.gov/All-Programs/Programs/NY-Sun/Data-and-Trends), we realized that said data was not indicative of more general solar panel adoption trends, so we went looking for other data to play with.

A classmate turned us towards (https://datausa.io/map/?level=county&key=uninsured). The next dependent variable we considered was **alcohol-related** motor vehicle deaths, but the metrics were not well defined—compressed into percentages and ambiguous units; we could not use them to extrapolate an actual scalar number of automotive fatalities involving alcohol per county.

For the sake of time, we went with a simpler metric: Given some demographic attributes of a county, could we predict the number of plain old motor vehicle deaths that will happen in a year in that county? Could we do better than just guessing the average for every county? Tl;dr: Yes, linear regression works, but you have to start with the right data.

#### Contents of the Jupyter Notebook:
1. Data fetching and cleaning
2. Checking for normality and any colinearity
3. Splitting and Scaling the data
4. Making a baseline model
5. Making improved models¶

#### Excerpts:

![data](/readme/first_five.png)

![data](/readme/norm.png)

![data](/readme/pair_plots.png)

![data](/readme/co-lin.png)

##### A graph of our L2-CV model's coefficients, aka weights, aka betas, aka:

![data](/readme/L2.png)

##### Our model's guesses vs ground truth test set data:

![data](/readme/guesses.png)

![data](/readme/r2.png)

## Takeaways:

* A deep understanding of your initial data set and its provenance is imperative.
* Resilience and flexibility are key characteristics of a data scientist.
* In our multiple linear regression model, the two strongest features for predicting the motor vehicle death rate in any given US county are **teen childbearing rates** and the percentage of that county's **population that lives in a rural area.**
* We chose our features because they were handy in the available data set, but ultimately, these particular features may not be the best ones for predicting the number of **motor vehicle deaths** in any given US county, obviously.
