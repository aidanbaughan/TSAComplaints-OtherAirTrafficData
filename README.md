# TSA Traveler Complaints Dataset  

This repository contains data obtained by the **Data Liberation Project** via the **Freedom of Information Act**. The **Transportation Security Administration (TSA)** publishes semi-regular reports on the monthly number of traveler complaints by **airport, category, and subcategory**.  

## Background and Motivation  

The dataset covers complaints from **440+ airports** starting from **January 2015**. The **Data Liberation Project** maintains an updated pipeline to convert the **TSA's PDF reports into CSV files** for easier analysis.  

### Dataset Details  

- **Airport**: Three-letter airport codes are included. The dataset has been joined with another dataset (**USairports**) to display airport names.  
- **Category**: The main areas of complaints, such as **screening**, **mishandling of property**, and **ID requirements**.  
- **Sub-category**: Further breakdown of complaints, e.g., **mishandling of checked baggage vs. carry-on luggage**.  

Both **category** and **sub-category** columns are already cleaned. **Ambiguous subcategories** are marked with an **asterisk (\*)**, and the fields **clean_cat_status** and **clean_subcat_status** track data cleaning/standardization. Possible values include:  
- **original**  
- **imputed**  
- **ambiguous**  
- **missing**  

While complaints are continuously received, **TSA only reports them periodically**.  

## Goals of the Analysis  

- Identify **airports with the most complaints**  
- Determine **which categories generate the most complaints**  
- Analyze **trends over time**  

### Additional Dataset: Airports2  

I also incorporated another dataset, **Airports2**, which contains **3.5 million+ US domestic flights from 1990 to 2009**, sourced from **OpenFlights**.  

However, this dataset does not overlap with the TSA complaints dataset, which is frustrating since it limits comparative analysis.  

I searched extensively for **alternative airport-related datasets** but found no useful sources. If anyone knows of relevant data sources, **please let me know!**  

## Analysis Plan  

Despite the limitations, I proceeded with **Airports2** and supplemented it with relevant updated data where possible, such as:  
- **Total flights per year**  
- **Passenger traffic trends**  
- **Busiest airports**  

My goal is to analyze **how airport size, flight count, and passenger count correlate with TSA complaints**.  

Additional analyses:  
- Identify **most common flight routes** for this period  
- Determine if **airport size correlates with population size**  
- Examine how the creation of the **TSA in 2001 (post-9/11)** impacted air travel
  
**If you have any insights or know of additional datasets, please share!**

## Summary of Findings 


## Figure 1 - Complaints Per Month  
![Complaints Per Month](https://github.com/user-attachments/assets/b7e71a52-fd83-4af9-a29c-553cbc073405) 

### Potential reason for the increase of complaints over time:

In March 2024, a TSA spokesperson provided comments to **FedScoop** reporter **Rebecca Heilweil**, indicating that (at least) some of the increase in complaints over time can be attributed to the agency making it easier to submit **PreCheck complaints**:

The spokesperson said that changes to several platforms and customer service tools are responsible for the rise in complaints. In **May 2021**, the agency created a new **TSA PreCheck webform** that saw complaints increase around **79%** in the following four months. That **August**, the agency deployed messaging enhancements that, in combination with the new online form, saw complaints grow by **62%** in the subsequent four months. 

## Figure 2 - Complaints by Airport   
<img width="517" alt="Screen Shot 2025-03-05 at 9 08 10 AM" src="https://github.com/user-attachments/assets/45f9975b-e80a-415b-b55b-d17b6259c0a4" />

Newark Airport (EWR) has a reputation for being one of the worst airports for TSA complaints compared to the number of passengers it serves, and the dataset reflects that. Doing some research online, it seems like the number of TSA complaints is also correlated to average TSA wait times, and this would be an interesting thing to analyze further. 

## Figure 3 - Complaints by Airport and Category  
![Complaints by Airport and Category](https://github.com/user-attachments/assets/510c95ca-00d4-46e9-bfab-207aad01cd0a)  
The most common type of complaint for most of the top airports in the dataset is expedited passenger screening complaints, better known as the TSA precheck complaints. The only airports this wasn't true for in the top 10 were Harry Reid International Airport(LAS) and Miami International Airport (MIA), where the top complaint was mishandling of passenger property. Further analysis shows that the TSA PreCheck Webform has had a significant effect on the number of complaints and has contributed to the increase in expedited passenger screening complaints. 

## Figure 4 - Complaints by Airport Over Time  
![Complaints by Airport Over Time](https://github.com/user-attachments/assets/e45ee07a-bdea-425a-bd2b-af61f9e144ed) 
Most airports have experienced similar patterns in the amount of complaints over time, where complaints stayed around the same range from 2015-2020, before dropping off massively due to the COVID-19 Pandemic. But, the number of complaints soared to new heights starting in 2022, likely due to the increase of precheck complaints. Some airports, such as the Newark Liberty International Airport have seen a **Massive** increase in these years, while other airports have had more modest increases. 

## Figure 5 - Heat Map Showing Flight Routes  
![Heat Map Showing Flight Routes](https://github.com/user-attachments/assets/3c5b1680-5e7b-4b2b-b773-0d8f2ea10b9c)  
This was a cool visual I wanted to show, it was not that useful for analysis, but more just my curiosity. I wanted to see where flights from major airports were flying most often, and this was an interesting way to show it. 

## Code 
This repository contains one Malloy code file:
* TSAcomplaints.malloynb, performs the analysis piece of the data provided by the Data Liberation Project.

## Licensing 
The files provided directly via FOIA (see listing above) are, as government documents, now in the public domain. All other data files have been generated by Aidan Baughan for Gonzaga University Graduate School of Business as part of the MSBA-622-01 Data Science for Business (Spring 2025) course and are available under Creative Commons’ CC BY-SA 4.0 license terms. The license applies to this file and other files in the GitHub repository hosting this file.
