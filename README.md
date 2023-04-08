
# Storslysia Relocation Social Insurance Proposal
![image](https://user-images.githubusercontent.com/129587466/230257771-90115d65-e73b-4413-97de-07b3ec710098.png)

>Team All Pass @ UNSW  
>Boyuan Wang | Jason Zhang | Jingyuan Wang | Yan Ching Tang | Ying Jiang
---

## Executive summary
The following report will be introducing our social insurance program that provides protection to residents in Storslysia against socio-economic loss caused by natural disasters. The divergence of level of development and risk exposure were taken into consideration that we tailored the policy to ensure residents in the six regions of Storslysia are well protected from emergency displacement in an equal and cost-effective basis. In addition, a voluntary relocation section was designed to encourage risk mitigation, believing that awareness and proactive actions are fundamental in reducing potential losses.

Our model was designed based on the historical hazard data of Storslysia, future environmental estimations by the ICCP, and some reliable assumptions made due to the limited information. Stress tests were performed assuming extreme deterioration of weather and poor response to this program that we are highly confident regarding the effectiveness and budget control.

Cost and result of this program were projected across the next twenty years. Effectively, it would more than halve the expected loss arisen from catastrophic weather events by the end of this policy term, with two third of the reduction amount attribute to voluntary relocation.

## Project outline
![image](https://github.com/Actuarial-Control-Cycle-Part-A-2023-T1/group-github-pages-team-all-pass/blob/main/project%20outline.png)
![image](https://github.com/Actuarial-Control-Cycle-Part-A-2023-T1/group-github-pages-team-all-pass/blob/e218fd54c5cd2d37e657f3164ef0d762987eb42a/project%20outline.png)
 
## Brief Working Process
### Objective
The present study aimed to comprehensively analyze the assigned task by conducting a thorough review and examination of the provided data. The primary objective was to develop a sound project outline and test various models for hazard rate modeling.

### Data Analysis
In order to guarantee the veracity of the data, the research team undertook a thorough and rigorous examination of the provided information. The team conducted a detailed analysis of relationships between different variables to discern trends and establish a dependable project outline. To determine the most appropriate methodology for hazard rate modeling, the team conducted testing of multiple models.

### Research and Assumptions
Given the limited availability of data and information, the team sought guidance from similar products that already exist in the market. Moreover, the team relied on prior research published in academic journals that studied the relocation intentions of households to make certain assumptions.

### Hazard Rate Modeling
The team employed the CO2-related model to prognosticate future hazard rates. The amplification factor employed in the model was appraised for diverse years, while the base hazard rate was estimated through the application of a Poisson GLM model. The hazards were categorized into various magnitudes based on their costs, and the average cost was utilized for subsequent modeling.

### Relocation
To determine the probability of encountering hazards, the research team calculated the number of households eligible for relocation based on an estimated level of risk for each property. To focus on displacement and its potential consequences, minor hazards that do not significantly impact the quality of life were disregarded. Additionally, well-defined coverage rules were established to define the program's scope, and the associated costs were computed accordingly. Furthermore, the team conducted stress testing to evaluate the program's performance under varying scenarios.

### Conclusion
The statistical software packages R and Excel were employed to execute the requisite computations. The report culminated by elaborating on the program's costs, enumerating the underlying assumptions, examining the risks entailed, and expounding upon the constraints of the model.

## Objective

This social insurance program for relocation is aimed at helping Storslysia manage its exposure to displacement risk arising from catastrophic climate-related events, as Storslysia is acutely threatened by the impact of climate-related catastrophes that are increasing over time due to climate change.

Key metrics to be reported and used to monitor the proposed program’s success over the selected timeframe (2024 to 2043).  The effectiveness of this program will be accessed from three aspects: reduction in cost, the total cost of the program and pricing of the insurance (accessibility) every year over a 3-year short-term timeframe and 20-year long-term timeframe. 

## Assumptions
### Economic variables
No clear pattern was discovered from the historical interest rate. It was assumed that future interest rates would continue to perform in a similar pattern. The average interest rate from 2002 to 2021 (1.5%) was used to compute the premium of this insurance program.  

It was assumed that appreciation in property value cancels out with depreciation cost as pricing trend for property value was not provided. Therefore, property damage caused by hazards would follow the same trend as historical data.  

The economic growth of Storslysia was assumed to be identical to the inflation rate. Under this assumption, all values provided, such as property damage, were in real terms instead of nominal terms. No adjustments were required to modify them to the present value.  

### Regional geographic and economic conditions 
It was assumed that the regional differences in degree of economic development and risk of experiencing natural disaster (I.e., number of households, accommodation cost, property value distribution, persons per household) exist in a similar manner in the future. This was for the purpose of reducing error due to model complexity.   

### Hazard occurrence  
It was assumed that future frequency of natural disaster is variable only based on CO2 emissions, while their severity and the types of natural disaster are proportionally the same as the past.  

The RAF (risk amplification factor) and annual hazard counts in each region were fitted in a GLM Poisson model to project the hazard rates of each region in 2020, which was used as the baseline to predict future hazard rates.  

### Voluntary reallocation population
The percentage of voluntary relocated households in high-risk areas were assumed to be distributed from (0.02 to 0.14). Generally, there would be a higher intension to relocate in the starting period of this program, and it would gradually diminish. It was assumed that the annual relocation effect of voluntary relocation on reducing property damage is half of the voluntary relocation percentage. The total relocation effect at the end of this insurance term is about 45%, which represents that voluntary relocation would mitigate 55% of property damage in 20 years' time compared to damage without voluntary relocation.   

> Refer to Appendix 1 for detailed voluntary relocation proportion and effect.  

### Policy design assumptions 
As this social insurance program focuses on reducing the relocation risk, minor hazards were considered not able to damage properties to a level that is not suitable for living, thus they were ignored in cost calculations.  

Material and labor costs associated with housing and relocation were assumed to increase 25% after medium and major hazards. Households who need temporary accommodation after hazards were calculated by hazard damage cost after any adjustment for relocation dividing 40k. The value of 40k was decided since this is roughly 20% of average property value. Temporary accommodation cost per person per month was referred to the given data, assumed to be fixed.  

Other components involved in the cost model formula, such as basic needs cost (Ꝕ 400), average persons per household were assumed to be constant throughout the policy term.  

## Project design
### Outline
This social insurance program is designed to cover catastrophic loss while maintaining solvency by charging a premium that is affordable to residents of Storslysia. The market being targeted is all Storslysia’s population and the Government of Storslysia has made the insurance compulsory to residents of Storslysia, in order to spread the cost of natural disasters across the country and make coverage cheaper for those in high-risk regions. The definition of a claimable event is provided in the following section for voluntary relocation and displacement respectively.   

### Voluntary relocation   
For a person to file a claim for voluntary relocation, the following conditions need to be satisfied:  
* Each household, later referred to the insured, can make only one voluntary relocation claim during the period of insurance.    
* The insured must own and live in a property in a region that is rated as a high-risk region under this program.    
* The property must also be the only property that the insured possess.    
* The property must not be involved in other voluntary relocation claims.   
* The insured must have purchased the property before the implementation of this insurance program.   
* The insured must relocate to a region that is rated as a low-risk area under this program.   
* The insured must reinforce the property when relocating and the consolidated property must satisfy specific standards.  

### Involuntary displacement   
For a person to file a claim for involuntary displacement, the following conditions need to be satisfied:   
* The property must be discarded due to health risks (no longer suitable for living). It is usual to wait for an assessor appointed by the insurer to come and inspect the damage before a clean-up commences.   
* Residents must live in the property that is affected by eligible Catastrophe events.   
* The property must be owned before the implementation of this insurance program and has not been involved in any voluntary relocation insurance.   
* The Catastrophe must be a declared event by the Insurance Council of Storslysia during the period of insurance and a code will be issued and used by all the insurers.   

### Coverage   
The focus of this insurance program is primarily to support displacement and encourage voluntary relocation to reduce economic costs of Storslysia due to Catastrophe events. The detail of coverage is listed in the below table.  

| |Coverages|Cost|
|---|---|---|
|Voluntary Relocation |Relocation costs – amount claimable is a certain percentage allocation of the property value |5% of the property value with amount claimable capped at Ꝕ40,000 |
|Involuntary Displacement|*1-month temporary accommodation *1-month basic living expenses *Repair of property damage (Subject to conditions listed above) |*Temporary housing costs per person of the household insured. *Basic living expenses of Ꝕ400 per person of the household insured. *Up to 125% of property damage (extra 25% allowance due to increase after hazards)|

### Incentives for voluntary relocation   
In order to encourage residents living in high-risk areas to relocate voluntarily, a 5% of their own property value is claimable while meaningful consultation and participation of affected populations is provided.   The fact that the program does not cover residents moving in after the implementation of the program or new buildings/houses can also discourage people to move into high-risk regions.    

As the leaders of Storslysia are highly motivated to manage the risks associated with catastrophe-related displacement, the Government can act as the main distribution channel to help encourage residents of Storslysia to relocate.  For extremely high-risk regions, allowing homeowners to sell their properties to the Government so the area can be returned to open floodplains can be one of the alternatives with the support of the Government.

### Other key features   
Specific attention is given to the safety of any unaccompanied children, women and girls, female-headed households, and any other at-risk group.   

The movement is carried out in a manner which is mindful of the frailties of elderly people, of people with health concerns (e.g., by ensuring access to necessary medication for the duration of the move) and the needs of people with mobility restrictions (e.g., by ensuring means of transportation are accessible to people with different disability types).   

Information about when and how the movement is to occur is provided in all relevant languages and in a variety of formats to ensure that people with different impairments can access the information.   

To file a claim, photos of the damaged items and property, especially if they need to be discarded to avoid danger, need to be provided. It is usual to wait for an assessor appointed by the insurer to come and inspect the damage before a clean-up commences.   

Losses of injuries and death caused by Catastrophe events are not covered by this insurance program, the program is designed purely from a relocation support perspective.  Only property owners are covered in the program. 

### Justification
Product design: The basic coverage will be provided for everyone involved in Storslysia where displacement due to catastrophe events occurs, and it will satisfy basic essential daily needs after the catastrophe event occurs.  By forecasting potential relocation costs using hazard event projection and Stroslysia’s GDP each year using the estimated interest rate and inflation rate, the cost from relocation can be controlled under 10% of Stroslysia’s GDP. The overall cost of this insurance will be 38% lower than post-disaster reconstruction in average. In addition, this program provides extra benefits for voluntary relocation compared to involuntary relocation, the premiums premium will be charged according to the risk rate in each region. These specific features are utilized to be an incentive for voluntary relocation.    

Cost-effectiveness: The program provides 5% of property value for people living in high-risk areas with the intention to relocate voluntarily. Limitations are set to prevent people from making profits from this program. In order to make claims for voluntary relocation, the original property needs to be strengthened. This will reduce the later chance of property damage and the potential cost of this program.

### Evaluation timeframes  
The key metrics we use to monitor program performance will be the total cost of this social insurance, reduction in costs arising from catastrophe-related displacement with this program in force, and the affordability of the insurance. The metrics need to be monitored and evaluated over both short and long-term timeframes.   

The short-term timeframe of three years has been used to monitor performance of the program even that the frequency of catastrophe events is expected to be low. As this is a newly implemented program, it needs to be monitored closely to measure performances and make reasonable adjustments if necessary.    

The long-term timeframe of twenty years has been selected as the condition of the economy, climate-change impact and depreciation of properties are expected to demonstrate a steady trend. The demographic of Storslysia is also expected to differ to present if the program progressed successfully. 

## Pricing & Costs 
To account for the economical and geographical differences of the six regions, cost and premium pricing were considered individually. To project the cost of this program in the next 20 years, the following conditions were adopted:  
* hazards rate predicted by the RAF model provided under medium CO2 emission, 
* cost of repair is 125% of damaged property value due to hazard,  
* emergency displacement cost includes the cost of repair and temporary accommodation and basic need cost, 
* total policy cost includes emergency displacement cost and voluntary relocation cost,  
* premium is computed based on total policy cost and households amount for each region and half year interest is considered. 

Note: All values provided are in Ꝕ.

### Hazard Frequency  
Based on the future forecast CO2 emission data provided in the SSP scenarios model, a cubic equation was fitted for each scenario to obtain the annual CO2 emission level from 2020 to 2045. The risk amplification factor (RAF) for natural disasters were obtained by
```math
(CO_2\ emission\ of\ target\ year/CO_2\ emmission\ of\ base\ year)^2
```
By using the predicted number of hazards occurred in 2020 as baseline, the expected number of hazards occur in the next 20 years under medium CO2 emission would be projected.   

### Hazard Severity   
As mentioned in the assumption section, natural disasters were expected to create similar scope of economic losses compared to the past events.  Minor/medium/major hazard rates were computed proportional to the historical total hazard rates for each region. Minor/ medium/major hazards are determined if the property damage is larger or equal to Ꝕ0/100,000/5,000,000. 

> For more details, see Appendix 2 

### Voluntary Relocation Cost 
```math
Household\ wish\ to\ relocate\ =\ Household\ in\ the\ high\ risk\ area\ *\ Relocation\ percentage\ every\ year
```

```math
Voluntary\ relocation\ cost\ =\ Household\ wish\ to\ relocate\ *\ Average\ property\ value\ *\ 0.05\ *\ (benefit\ percent) 
```

### Emergency Displacement Cost
```math
Temporary\ cost\ =\ Estimated\ households\ required\ accommodation\ *\ Average\ person\ per\ household\ *\ (Temporary\ accommodation\ cost\ +\ basic\ needs\ cost)
```

```math
Repair\ cost\ =\ Expected\ property\ damage\ after\ adjustment\ *\ 1.25\ (extra\ 0.25\ allowance\ for\ the\ cost\ rise\ after\ hazards)
```

```math
Emergency displacement cost = Repair cost + Temporary cost
```

> For detail formulas, see Appendix 3. 

### Policy Cost
Annual policy cost for the whole country with this program equals the summation of emergency displacement cost and voluntary relocation cost (sum over all regions). Combining the economic cost without the program (same estimation formula as displacement cost model for the policy, expected no relocation effect), the chart below shows the comparison between policy cost with and without the program. For more detail, see Appendix 4. 

![image](https://user-images.githubusercontent.com/129587466/230258640-351ab265-ea3f-47d9-a0b9-13977edd5298.png)


### Premium  
Households in the six regions will be charged with different premiums based on the level of risk they are exposed to.

|Region|1|2|3|4|5|6|Storslysia|
|---|---|---|---|---|---|---|---|
|Average (Ꝕ) |9.08|196.01|20.04|67.70|178.22|49.43|72.76|

Premium under general condition is provided as a guide to demonstrate affordability. Detail funding is not a part of this project.    

> See Appendix 5 for the detailed annual premiums.

### Economic Capital
To determine economic capital for high degree of certainty, we assume the extreme case as follows:  
* Use one-side 99% confidence interval of predicted hazard rate as the base hazard rate for 2020,  
* Assume very high CO2 emissions,  
* Assume 50% cost increase after hazard,  
* Assume relocation effect has no effect each year while voluntary relocation cost remains the same.  

> See Appendix 6 for annual economic capital required. 

The extra capital required for solvency can be funded in two ways:  
* The government invests initial capital at the start of this program. Extra premiums will be charged in the following year if the claim amount exceeds the general policy cost in the previous year. Under this design, the initial capital required would be approximately Ꝕ 750,000,000 (0.06% of GDP).  
* Or charge a premium at the start of each year according to the estimated extreme policy cost and refund any extra value left at the end of the year to the insured. Under this design, no initial capital is required.  
* Even under the extreme cases, the overall policy cost over 20 years (Ꝕ 23,742,589,828) is significantly smaller than 10% GDP (Ꝕ 129,693,892,200), not to mention the annual total cost. Hence, we are confident that the cost of the program will not exceed 10% of the GDP each year.  

### Voluntary Relocation & Emergency Displacement Costs 
The costs under the program associated with voluntary relocation with those associated with emergency displacement sums up to the total policy cost. The voluntary relocation cost varies each year which depends on the amount of relocation households each year. The emergency displacement cost reduces over time due to relocation effect. Most of the cost under the program is from emergency displacement, the cost of emergency displacement is about 36 times higher than the cost of voluntary relocation on average. 

![image](https://user-images.githubusercontent.com/129587466/230258698-05a2fde4-bfd7-4757-b1ac-5a253c967789.png)


We also computed potential emergency costs that will be reduced by voluntary relocation which measures the total future emergency displacement cost that would be reduced by each year’s voluntary relocation. I.e., the cost reduced for 2024 measures all the cost reduced (from 2024 to 2043) because of 2024 voluntary relocation. From the table below, we can see that the reduced economic cost associated with emergency displacement due to voluntary relocation is significantly larger than the cost needed for voluntary relocation. 

||Emergency displacement|Voluntary relocation|Reduced emergency cost|
|---|---|---|---|
|Overall (Ꝕ)|9,841,095,208|265,124,927|6,356,118,573|
|Average (Ꝕ)|492,054,760|13,256,246|317,805,929|

However, in real world, properties that are relocated may not to be damaged, and instead of percentage effect, damage avoided by each individual property relocated needs to be added up. The value of emergency cost reduced by voluntary relocation will be smaller in real world. Hence, the values of our model should be used as a guide whereas the idea behind and relationships between different costs will remain the same under real world case. 

> Please refer to Appendix 7 for detailed data. 

## Risk and Risk Mitigation Strategies
Under our model, the difference of the economic cost between with and without policy is the voluntary relocation cost and the reduction in emergency displacement cost due to voluntary relocation. Hence, we wish to have some certainty that cost reduced by voluntary relocation effect to be larger than the cost of voluntary relocation.  

From the previous section, “Voluntary Relocation & Emergency Displacement Costs”, we can see that under general assumption, the economic costs reduced due to voluntary relocation is significantly larger than the voluntary relocation cost. For stress testing, the reduction effect of voluntary relocation on property damage due to hazards was set to be 5% of the original assumption. I.e., if originally, we assume the relocation effect to be 0.004, now it is only 0.002.  

Our result suggested that even if the relocation effect is minor (5% of original assumption), emergency cost saved due to voluntary relocation would still be 20% larger than the voluntary relocation cost. With the allowance of more than 95% of our assumed reduction effect of voluntary relocation, and the fact that we assumed the percentage of relocation households to be twice the reduction effect (half of the relocated property will not be affected by hazards even not relocated), we can say that with high degree of certainty that the economic costs associated with the program will be less than the economic costs would be without the program. 

> Please refer to Appendix 8 for detailed data. 

We are also highly confident that the cost of the proposed program will not exceed 10% of Storslysia’s GDP in any given year which is discussed before under “Economic Capital” section.  

The following table introduces some other key risks that may occur when implementing this program and some potential mitigation techniques. 

|Risk|Description|Mitigation Techniques|
|---|---|---|
|Inequality on premium charged|Region at risk has been categorized to low, medium, and high, there is possibility that the risk level for regions defined in each category differs, hence some regions may pay higher premium compared to other regions in the same risk category.|Continuous enhancement of the product needs to be conducted by reviewing the product at a reasonable frequency, to assess whether categories designed still align to the needs of the insured.|
|Market risk|Inflation/interest rate and currency rate will impact the features of the product in terms of maximum coverage, etc.|Stress testing is performed to ensure that the fluctuation in inflation, interest and currency rate is considered when designing a product, and a premium charge is sufficient to cover potential losses due to market impact.|
|Overpopulation pressure on alternate cities|There may be pressure on low-risk regions which may themselves be subject to overpopulation and sea level rise or subsidence as insured from high-risk region tend to relocate to low risk regions.|Monitor low risk region population and propose alternate cities to relocate if overpopulation is identified.|
|Affordability risk|There is risk that price can be high relative to citizens’ income based on the results of the pricing model we built, which may disappoint the insured as we make the social program mandatory.|Removing state taxes on insurance products is an immediate measure that governments can take to make insurance more affordable.|

## Data and Data Limitations 
The given data and model are used (Hazard event data, Demographic and economic data, Emission scenarios and model). Limitations of the data are listed below, incomplete information provided will reduce of the accuracy of the model. 

There were several missing values in the inflation and interest rates data provided by SOA. NA and outliers have been removed from the dataset used in the models.  
* No Atmospheric CO2 Concentrations data provided for years prior to 2005, the data for 2020 has been used as base year data, to align with the data provided in the Demographic-Economic dataset (GDP data has been provided for year 2019 and 2020).   
* The demographic and economic data was provided by region only, accuracy of models produced can be improved once information for specific risk level for areas within each region is made available.   
* Detailed information needed to predict hazard events rate is limited. The frequency projection model given is used to estimate hazard events rate, which is subject to judgement since the rate may not follow the pattern of how atmospheric CO2 concentrations rise or fall. Cubic interpolation was used to determine RAF (risk amplification factor) per year as only data in decade is provided.  
* Information on residents’ relocation intention was not provided, assumption has been made to accommodate the missing information into the models.  

## Appendix
1. Voluntary relocation proportion and effect 
      ![image](https://github.com/Actuarial-Control-Cycle-Part-A-2023-T1/group-github-pages-team-all-pass/blob/main/A1.png)
      
2. Calculation on number of hazard events in next 20 years by using most fitted trend line, and the R-square of fitted trend line is controlled higher than 0.995.
      ![image](https://github.com/Actuarial-Control-Cycle-Part-A-2023-T1/group-github-pages-team-all-pass/blob/main/A2.1%20excel%20trendline.png )
      ![image](https://github.com/Actuarial-Control-Cycle-Part-A-2023-T1/group-github-pages-team-all-pass/blob/main/A2.2%20excel%20emission%20detail.png )
      
3. Formulas used to model voluntary Relocation, emergency displacement and policy cost. 
    * Expected property damage (medium/major) = Average property damage (medium/major) * predicted hazard rate (medium/major) 
    * Expected total property damage = Expected property damage (medium) + Expected property damage (major) 
    * Household in high-risk area = Expected total property damage * Total relocation effect (from 0.96 to 0.45 depending on time) / 40k 
    * Household wish to relocate = Household in the high-risk area * Relocation percent each year (from 0.14 to 0.02 depending on time) 
    * Voluntary relocation cost = Household wish to relocate * Average property value * 5% (benefit percent) 
    * Expected property damage after adjustment for relocation = Expected total property damage * Total relocation effect (from 0.96 to 0.45 depending on time) 
    * Estimated households require accommodation = Expected property damage after adjustment for relocation / 40k 
    * Temporary accommodation & basic need cost = Estimated households require accommodation * Average person per household (regionally based) * (Temporary accommodation after hazard cost per person per month (regionally based) + basic needs cost (Ꝕ 400)) 
    * Repair cost = Expected property damage after adjustment for relocation * 125% (25% increase for cost rise after hazards) 
    * Emergency displacement cost = Temporary accommodation & basic need cost + Repair cost 
    * Total policy cost each region each year = Emergency displacement cost each region each year + Voluntary relocation cost each region each year 
    
4. Cost comparison with or without program
      ![image](https://github.com/Actuarial-Control-Cycle-Part-A-2023-T1/group-github-pages-team-all-pass/blob/main/A4%20cost%20comparison.png )
      
5. Predicted annual regional premium under medium CO2 emission.
    * Premium = Total policy cost for each region/ (1+half year interest) / household in each region 
    ![image](https://github.com/Actuarial-Control-Cycle-Part-A-2023-T1/group-github-pages-team-all-pass/blob/main/A5%20premium.png )
    
6. Economic capital testing
    * Poisson GLM to predict hazards rate in 2020 and 99% one-side confidence interval for extreme cases. 
    ![image](https://github.com/Actuarial-Control-Cycle-Part-A-2023-T1/group-github-pages-team-all-pass/blob/main/A6.1%20capital%20testing%20R%20code.png)
    
    * Comparison of total policy costs under normal and extreme cases  
    ![image](https://github.com/Actuarial-Control-Cycle-Part-A-2023-T1/group-github-pages-team-all-pass/blob/main/A6.2%20comparison.png)
7. Voluntary relocation and emergency displacement costs and effectiveness of voluntary relocation
      ![image](https://github.com/Actuarial-Control-Cycle-Part-A-2023-T1/group-github-pages-team-all-pass/blob/main/A7.1%20table.png )
      ![image](https://github.com/Actuarial-Control-Cycle-Part-A-2023-T1/group-github-pages-team-all-pass/blob/main/A7.2%20chart.png )
8. Emergency costs reduced under extreme case. 
      ![image](https://github.com/Actuarial-Control-Cycle-Part-A-2023-T1/group-github-pages-team-all-pass/blob/main/A8.png )

## BIBLIOGRAPHY
Chetty, R. 2006, “A general formula for the optimal level of Social Insurance,” Journal of Public Economics, 90(10-11), pp. 1879–1901, <https://doi.org/10.1016/j.jpubeco.2006.01.004>

Chetty, R. and Finkelstein, A. 2013, “Social Insurance: Connecting Theory to data,” handbook of public economics, vol. 5, pp. 111–193, 
<https://doi.org/10.1016/b978-0-444-53759-1.00003-0>

Disaster Insurance for the Poor? A review of microinsurance for natural disaster risks in developing countries, accessed 24 February 2023, <https://www.ipcc.ch/apps/njlite/srex/njlite_download.php?id=6705> 

Disaster mitigation and insurance: Learning from Katrina, accessed 24 February 2023, 
<https://journals.sagepub.com/doi/10.1177/0002716205285685> 

McAneney, J. et al. 2015, Government-sponsored natural disaster insurance pools: A view from down-under, International Journal of Disaster Risk Reduction. Elsevier, accessed 24 February 2023, 
<https://www.sciencedirect.com/science/article/pii/S221242091530159X> 

Outline of Japan's earthquake insurance system 2022 Ministry of Finance, accessed 24 February 2023,<https://www.mof.go.jp/english/policy/financial_system/earthquake_insurance/outline_of_earthquake_insurance.html> 

US Government Natural Disaster Assistance: Historical Analysis and a Proposal for the Future, accessed 24 February 2023, 
<https://onlinelibrary.wiley.com/doi/10.1111/1467-7717.00110>



---




