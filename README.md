# Managing-Outlier-in-Biomass-Data-EU-Countries

This time, we try to do simulation in managing ourliers of Biomass use Data throughout EU countries. Using Python libraries such as pandas, seaborn and numpy, we could see how much Biomass could be produced in each sectors.

1. Download the raw data in (https://datam.jrc.ec.europa.eu/datam/public/pages/previousFilters.xhtml?dataset=34178536-7fd1-4d5e-b0d4-116be8e4b124&rdr=1618867520333)

[Biomass](https://github.com/altheanabila/Managing-Outlier-in-Biomass-Data-EU-Countries/blob/main/Dataset_JRC_-_Biomass_uses_and_flows.csv)

2. import related libraries, and extracting into panda dataframe

![Test image 1](https://github.com/altheanabila/Managing-Outlier-in-Biomass-Data-EU-Countries/blob/main/biomass3.png)


3. perform the code in order to show the graph and detect ourliers

`ax = sns.boxplot(x="Sector", y= "Value (THOUSAND TONS)", data=data)`

![Test image 2](https://github.com/altheanabila/Managing-Outlier-in-Biomass-Data-EU-Countries/blob/main/biomass2.png)


4. Manage outliers to see the data population better

`data[['Value (THOUSAND TONS)']] = np.log(data[['Value (THOUSAND TONS)']])` 
`ax = sns.boxplot(x="Sector", y= "Value (THOUSAND TONS)", data=data)`

![Test image 3](https://github.com/altheanabila/Managing-Outlier-in-Biomass-Data-EU-Countries/blob/main/biomass.png)
