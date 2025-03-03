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

Complaints Per Month 
<img width="418" alt="Screen Shot 2025-03-02 at 8 23 14 PM" src="https://github.com/user-attachments/assets/b7e71a52-fd83-4af9-a29c-553cbc073405" />

Complaints by Airport 
<img width="526" alt="Screen Shot 2025-03-02 at 8 23 45 PM" src="https://github.com/user-attachments/assets/676cc535-4354-4f78-a5f4-2705d9821149" />

Complaints by Airport and Category
<img width="582" alt="Screen Shot 2025-03-02 at 8 24 32 PM" src="https://github.com/user-attachments/assets/510c95ca-00d4-46e9-bfab-207aad01cd0a" />

Complaints by Airport Over Time 
<img width="586" alt="Screen Shot 2025-03-02 at 8 25 51 PM" src="https://github.com/user-attachments/assets/e45ee07a-bdea-425a-bd2b-af61f9e144ed" />

Heat Map Showing Flight Routes 
<img width="584" alt="Screen Shot 2025-03-02 at 8 30 27 PM" src="https://github.com/user-attachments/assets/3c5b1680-5e7b-4b2b-b773-0d8f2ea10b9c" />

  
