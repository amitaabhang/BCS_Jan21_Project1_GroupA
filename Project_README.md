# Group 1 - Project 1

The city of Newark, NJ has compiled a list of multiple abandoned and vacant buildings.  From this list, our goal was to find a correlation between this list and the factors that may have contributed to the number of abandoned properties. The overall data on city statistics of housing demographics, crime, education, and poverty were obtained and evaluated.



# Part 1 - Newark Overall Housing

The notebook for this segment appears under the "01_Newark Overall Housing Data" folder, named "HousingDataAnalysis.ipynb".

This part of the project covers data and its analysis of the overall housing in NEwark, NJ

The data was collected from the Census website for years from 2015-2019. The data was cleaned to roll up to city level, drop the unwanted values, format the data to remove the unwanted characters in the data. After cleaning the data it was further analysed as below.

1. Demographics: This section covers the details on demographics in Newark. The data collected is for 2019. 
   The output shows the race distribution, population, median age in Newark for 2019

2. THe next section is Occupancy characterstics in NEwark for years from 2015- 2019 . No of units occupied, which were rented, owner occupied.

3. Following section covers the housing details from 2015-2019 in Newark and in NEw Jersey.

4. Used this data with Occupancy data observations to plot a line graph to see a trend of how the housing changed in Newark, NJ over 5 years.

5. Geographical Mobility : This section tracks how the movement in Newark, NJ over 5 years 

6. The line plot describes the mobility observed in NEwark, NJ. Data gives details on  how many people moved in county, moved from out of state to NEwark, from outside country to Newark.

7. This section shows the property values data of NJ state to Newark over 5 years.

8. The plot describes the property value price range and the number of properties in Newark from 2015-2019
 



# Part 2 - Newark Abandoned Housing

The notebook for this segment appears under the "02_Abandoned Housing" folder, named "2_Newark_abandoned_data.ipynb".

For this part you will need the following to run this notebook:
1) Your Google.com API key as g_key in the file named api_keys.py (saved to the "02_Abandoned Housing" folder)
2) Install geocoder from the Terminal (see https://pypi.org/project/geocoder)

The processes below yield outputs that have been saved in a folder located "02_Abandoned Housing/output".

The Newark_abandoned_data notebook calls a JSON file from the City of Newark website obtaining a list of abandoned properties by address. (http://data.ci.newark.nj.us/dataset/abandoned-properties/resource/796e2a01-d459-4574-9a48-23805fe0c3e0)

Building DataFrames from this source allows us to utilize various functions to manipulate the data for analytical purposes.

KEY FACTORS

Translate DataFrame headers (keys) for context of the data
Build out full address including city, state, and zip code (used for next steps)

NOTE: the zip code collection for loop will run for approx. 5 minsutes before completing the process
----------------------------------------------------------------------------------------------------------------------
Add longitude and latitudes to the addresses for use in mapping (using geocoders)

Additional actions
Extract the summaries by year, zip code and other useful criteria for abandoned properties on the list.  
These summaries should be compatible with other data (poverty, crime, etc.)

Map the abandoned addresses on a map of Newark, NJ
Pie plot showing the relative percentages of abandoned property by zip code



# Part 3 - Poverty Rate Data Analysis

Before running Jupyter notebook (Newark Poverty Rate.ipynb) make sure you have the following:
1. Your Google API key as g_key AND Census API key as census_key in the file named config.py.
2. Check that newark_abandoned_data.csv is in 'data' folder
Once the notebook is run, it should display the following:
1. A csv file with population per zip code and poverty rates (output.csv)
2. A csv file that appends the output.csv to geographical coordinates (newark_poverty_population.csv)
3. A png file that displays the poverty rates per zip code over a map of Newark (newark_poverty_map.png)
4. These 3 files are available in the 'output' folder
This notebook combines the abandoned property data csv with US Census American Community Survey (5-Yr) for 2019.
It then groups the data by zip code and calculates an average value for geographical coordinates, to get at a "central" lat/long coordinate for each zip code. Then this data is displayed over a google map of Newark.



# Part 4 - Education

The notebooks for this segment appear under the "04_Education" folder, named "CollegeINFO.ipynb" and "HighSchoolINFO.ipynb".


College scorecard 
https://www.kaggle.com/kaggle/college-scorecard
college-scorecard-release-*.zip contained a compressed version of the same data available through Kaggle Scripts.
we used the data for 2014 to 2019 to undersand the surronding college. 
Extracted the files, saved the .csv files, extrcated the columns needed for comparison and removed. Selected the infroamtion for NJ and compailed the data for the files into one to get the over all picture.  To show the number of years for each college we created the stack plot. Creted a Line chart to show withdrawla rate from NJIT to essex. completed an analysis on the withdarl rate as that column had more information to tell and we can use it to show if studets are staying in colleges after registring to show the effect of the high schools. 


Higschool information 
https://nj.gov/education/administrators/
https://simple.wikipedia.org/wiki/List_of_counties_in_New_Jersey
Collect the High school information for year 2015_ 16, assumption (students from high school in 2015-16 would have by be in college by 2018-2019). 

From the data collected we pullled the Facility Attendace and Student Suspension Rate to see social impact of housing.
Analyzed the commitment of the students and Facitlity in Newark (13) and Somerville(35). from the same data set we also looked at Graduation rate and School Climate.



# Part 5 - Crime Data Study

The notebooks for this segment appear under the "05_Crime_Data_Study" folder, named "5a_combined_Crime_UCR_2018_2019_2020.ipynb" and "5b_crime_data_Newark.ipynb".

1) Load and run the "5a_combined_Crime_UCR_2018_2019_2020.ipynb". This combines data from the UCR for 2018, 2019, and 2020. The data sets were pulled and merged into a master data file before running a clean-up. Only the data for Newark, NJ was pulled and processed in the Jupyter notebook.

a. This notebook includes the total percentage graphs for each year, 2018, 2019, and 2020, respectively, and a final graph of the totals for all three together in one graph

2) Load and run the "5b_crime_data_Newark.ipynb". This data was pulled from a text file so additional steps were needed for processing the cleaning the data. The data was pulled in and converted to a CSV file by adding columns for each data set.

a. CSV was saved and then loaded into the Jupyter notebook for additional processing.

i. A “quick convert” button was added to Jupyter notebook but does not need to be used for running the notebook. This is noted by: “Extra optional cell to run for instant conversion from text to csv file”

ii. You can skip this to run the rest of the Jupyter notebook quicker

b. The one line of Newark specific data was pulled in and processed for the crime and additional items that were not used for the finished project but was run out of curiosity of the data.

c. A complete graph of just the crime data was created out of this data set.