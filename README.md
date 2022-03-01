# Fleet-Management-for-Public-Transport

The Objective of the project is to create and design a system which solves problems faced by the Indian public transport system revolves around the unwillingness of the users to opt for public transport. One of the most important, yet easily unnoticed, aspects about fleet management is preventative care and maintenance. It's not the quality of a vehicle's build that causes a premature demise, but rather improper maintenance. Given a lot of fleet data, our team would analyze it, so we can promote a more pro-active, instead of reactive, approach to maintenance, thus ultimately saving a company money and preventing unnecessary waste.

*** Click on the folder Fleet Management for Public Transport to view the folders and files of Sourcecode respectively.*****

***Explanation of the project***

Fleet Management for Public Transport is an Android App that predicts when a vehicle will require servicing and the type of servicing.

**Salient Features of the Android application**

A user can log into the app and check up on their fleet of vehicles. The user can add new vehicle by simply scanning the QR code containing vehicle number .From there, a python script manipulated the data given to find vehicles that need service/maintenance. The app will then tell the user which vehicles need what service, and the user can easily locate what vehicles need service by using augmented reality and location data! It chiefly takes into consideration the work laod over engine to compute the next required service check but also the other two main features are that it will use the latitude longitude data along with timestamp to check for weather log at that day, and also it would leverage the location data to find out terrain of the location. The weather and terrain form two important factor alongside of mileage/fuel efficiency of vehicle these all parameters are taken into consideration to find out when is next maintenance required and what type of maintenance is required. Based on location it suggests the nearest service station at the time of required maintenance.

public transport is not maintained with proper hygiene which discourages a large proportion of the commuters from using them.

public transport Fleet management is all about keeping costs reasonable, maximizing profitability, and minimizing risk.


 ***Solution Track Location***:
 
 We propose the development of a The python script communicates to the app by a firebase database. The authentication is also done from firebase. We used a t-test to find what vehicles need maintenance. which can be used to record every detail pertaining to a vehicle. The details may include the date of purchase, tire condition, engine oil status, etc. As a result, the user is provided with a complete history of the vehicle, thereby allowing him to make more informed choices.

When you click on the location option & allow to access the device's location, the app tracks your car's location and find nearby service.

It chiefly takes into consideration the work laod over engine to compute the next required service check.

The other two main features are that it will use the latitude longitude data along with timestamp to check for weather log at that day, and also it would leverage the location data to find out terrain of the location. 

The weather and terrain form two important factor alongside of mileage/fuel efficiency of vehicle these all parameters are taken into consideration to find out when is next maintenance required and what type of maintainance is required. Based on location it suggests the nearest service station at the time of required maintainance

The novelty of idea: Real-time monitoring of vehicle health. Novel and flawless use of Blockchain. Transparent Highly Secure

We believe that our solution will urge people to use public transport and also it serves as a monitoring mechanism for authorities to maintain public transport better.

Dealing with a lot of data was difficult as it caused for very long run times just to work with the data.

***Qualitative Accomplishments****

We managed to find vehicles that needed maintenance and present that in a very user-friendly way! We also learned a lot about data analysis techniques and managed to work efficiently as a team the whole time.

Built With Android Studio Firebase Echo Ar PyreBase Python Java

***Solution Derived with below Hypothesis and Test Data***

**Key metrics are mentioned**  
1.	aop = Area of operation. For each vehicle, found the furthest Northern, Easter, Southern, and Western latitude/longitude coordinates. Stored monthly and total furthest points.
2.	frpv = fuel ratio per vehicle. For each vehicle, calculated the fuel/hour ratio. A high ratio should indicate that a vehicle is working hard and will require more frequent maintenance. Stored averages daily, monthly, total, per 150 hours, and per 300 hours. 150 hours was chosen because this is when oil fitlers are typically replaced. 300 hours was chosen because this is when fuel filters are typically replaced
3.	dpv = distance per vehicle. For each vehicle, calculated the difference in distance between days. Stored accumulated totals daily, monthly, and total.
4.	over_under_use = The vehicles that failed the t-test. As of right now, the columns in over_under_use.csv do not signify anything beyond simply identifying the vehicle IDs that failed the t-test.

     Using a t-test, we tested the hypothesis that a vehicle's monthly fuel/hours ratio is the same as the total average fuel/hours ratio of vehicles of the same type ( i.e. motor grader, excavator, etc.) We found some vehicles with a p-value < 0.05 which indicates a significant difference between the set of a vehicles fuel/hour ratio and the total average population of that vehicles type. We believe fuel/hours ratio to be a good indicator of how hard a vehicle is working, thus the vehicles that failed the null hypothesis indicates they are either under or over utilized and might require maintenance. Also, failing the hypothesis could mean a bad fuel-air mixture in the engine, which would still indicate requiring maintenance. Differentiating between over/under utilized vehicles should be as simple as comparing their average fuel/hour ratio to the population's fuel/hour ratio.

Some of these vehicles could have failed the t-test because certain months did not have enough data collected, so in the future we will try to scrub the data more accurately. Also, in the future I would like to run a BIRCH clustering algorithm on the data which I believe would show which months had the highest fuel/hour ratios. Lastly, it would also be nice to run even more t-tests and test more hypotheses with the data generated.

The data used for the t-test:

frpv_month 

frpv_total 

