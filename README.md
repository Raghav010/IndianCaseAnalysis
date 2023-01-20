# **Analysing indian court case data**

## **Files and how to run**
- **All the files as ipynb files**
- **only run cells after the second heading in `criminalCourtTime.ipynb` and `bailableCaseCourtTime.ipynb`**
- **One insight from `criminalCourtTime.ipynb`** 
- **one insight from `bailableCaseCourtTime.ipynb`**
- **One insight from `CriminalCaseRates.ipynb`**
- **One insight from `JudgeGenderRatioOvertime.ipynb`**
- **`CleaningProcessingData.ipynb` cleans and processes data and saves this data to be used by `criminalCourtTime.ipynb` and `bailableCaseCourtTime.ipynb` since they have similar data requirements**

## **Insights**

### **Indian court cases are known for being notoriously long, so I wanted to explore what factors determine a long case? And how long do cases last based on these factors**

### **The factors I chose for this were** 
- the criminality of the case
- if the case was bailable or not

### **Insights from `bailableCaseCourtTime.ipynb`**
- The first part of the notebook shows a sample exploratory run on 2018 data, after which I automate this for all the years
- I calculate the average time a bailable or non-bailable case runs for in court (in days)
- Here we can see that the average time in court for bailable case is lower than a non-bailable case way back in 2010, but in the years after 2010 the bailablity of a case does not affect how long the case runs.
![](/a.png)
- We can also see an improvement in the court system in recent years, since the average time in court has decreased dramatically
- The average time has been on a downward decline since 2010
- Average duration over all the years is pretty huge,with bailable cases running longer in court 
    - non-bailable: little more than an year
    - bailable: almost an year and quarter
    - ![](/b.png)
- If we calculate averages for the last 3 years we get shorter durations , but are still long cases neverthless
(_last 3 years only, since we saw from criminalCourtTime and bailableCaseCourtTime that
only durations from last 3 years are representative of current world data_)
- ![](/c.png)

### **Insights from `criminalCourtTime.ipynb`**
- The first part of the notebook shows a sample exploratory run on 2018 data, after which I automate this for all the years
- We can see that the difference in durations between criminal and non-criminal cases is more significant than bailable/non-bailable cases from 2010-2013 and 2016-2018
- ![](/d.png)
- The duration of criminal and non-criminal cases during the years 2013-2015 are more or less the same i.e criminality didnt affect the run time of the case
- The interesting part is that the graph forms an intersecting reverse S-curve
- And as expected the run time of a case in general drops over the years
- Average duration of a case over all years
- ![](/e.png)
- Average duration of a case over last 3 years
- ![](/f.png)

### **We infer that the assumption that cases run for a very long time in court holds true and criminality affects the duration of a case**

### **Insights from `CriminalCaseRates.ipynb`**
- We see that criminal and non-criminal case rates drop to a low at 2011 oddly
- The non-criminal cases peak at 2016
- Criminal cases peak at 2018
- We see that criminal cases are more or less stable during 2010-2012, and during 2013-2018 they steadily increase
- There is a huge jump in criminal and non-criminal cases from 2013 to 2014
![](/k.png)
- Criminal vs non-criminal cases in different states over all years
- We can see that maharashtra has the highest number of criminal and non-criminal cases, and the non-criminal cases are nearly double the criminal cases
- Bihar and jharkhand seem to be the only states with more criminal cases than non-criminal cases
- Ladakh.mizoram etc i.e north eastern states have a very low criminal rate
![](/l.png)


### **Insights from `JudgeGenderRatioOvertime.ipynb`**
- Insight generated from this was the ratio of male to female gender ratio over the years
- The hard part generating this insight was calculating how many male and female judges were active during an year, since the input data just gave the years during which a particular judge was active
- The number of male judges is more than double the number of female judges(over all years)
![](/g.png)
![](/h.png)
- Data collection before 2000 and after 2019 is scarce so we can ignore those years
- Number of judges in general grows till 2016 and drop after that, expected
![](/i.png)
- The ratio stays stable at around 2 to 4 over 2010-2018 
![](/j.png)
- A big gender gap exists in judges

### **Dependcies**
- matplotlib
- seaborn
- gc
- pandas

