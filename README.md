# Surfs_Up
Using 


## Overview of the analysis: 

This project consists on using Python, Pandas functions and methods, and SQLAlchemy to analyze temperature treends for the months of June and December, in order to determine if the surf and ice cream shop business is sustainable year-round.

## Results

From 1700 sample of temperatures in the month of June we get:
- average temperature is 74.94 
- min is 64 
- max 85

![JuneSummary](https://user-images.githubusercontent.com/37987602/142750933-1fb172de-84d2-4f4d-91b5-70427853efca.png)


From 1517 sample of temperatures in the month of December we get:
- average temperature is 71.04 
- min is 26
- max 83

![DecemberSummary](https://user-images.githubusercontent.com/37987602/142750937-262eceee-ba12-44c6-ba41-8a75435916be.png)


## Summary

This firs thing to consider is that our samples are not the same lenght, this could have affected the results. Working and analyzing the data, the conclusion is the two months are not very different. Therefore we can say YES the surf and ice cream shop business is sustainbale year-roud.


I would rather, try to get more infomation about the temperature of the other months. 
```
Cahning the number of the month
temp = session.query(Measurement).filter(extract('month', Measurement.date) == 1).all()
list_temp = [temp.tobs for temp in temp_dec]
list_temp_df = pd.DataFrame(list_temp, columns=["Temperature"])
```
Also adding a graph would also help

```
list_temp_df.plot()

````

