## Diabetes Patients Data Analysis

According to the CDC, over 34 million Americans have diabetes, just a little over 1 person among every 10.
In light of this prevalence, I wanted to answer the following questions:

- Which demographic groups are overrepresented among diabetes patients?
- What are the diseases that tend to be co-morbid with diabetes?
- Which demographics have higher morality rates??
- Is there demographic bias in the care received?
- Does a longer hospital stay reduce later readmission?
- What do the records of the "most problematic" patients look like?


### Dataset Source and Cleaning 

This dataset was imported without any changes from the UC Irvine Machine Learning Repository, accessible [here](https://archive.ics.uci.edu/ml/datasets/Diabetes+130-US+hospitals+for+years+1999-2008).

The original data was extracted from the Health Facts database, a voluntary program offered to organizations which use the Cerner Electronic Health Record System. Clinical care data was collected from 130 hospitals and integrated delivery networks throughout the U.S., from 1999 - 2008. Only inpatient visits where the patient had diabetes as an existing condition were included. More details on the data selection methodology can be accessed [here](https://www.hindawi.com/journals/bmri/2014/781670/).

The steps in cleaning and pre-processing are, listed in order:
1. the removal of columns that contained over 50% NA values
2. the removal of rows wwith Null, Not Mapped, or Not Available entries for demographic columns
3. the removal of rows whose diagnosis is NA or not numeric
4. the rearranging of columns to leave all medicines for last 
5. the shortening of column names for ease of understanding
6. the creation of two new cleaned dataframes, one for encounters (each visit), and one for patients (the first visit for each recorded patient) 


### Analysis and Jupyter Notebook

The Jupyter notebook is accessible through the repository [here](https://github.com/tapatia/dats6103_p3/blob/main/DATS%206103%20-%20Individual%20Project%203%20-%20Dai%20Wei%20Tsang.ipynb). 


### Conclusion


**Q: Which demographic groups are overrepresented among diabetes patients?**

The dataset contained many more Caucasian patients than patients from other races, so a conclusion on race cannot be drawn.<br> However, 50-60 is the age range across all race groups where there is an obvious increase in the number of patients, only leveling off after 80, most likely due to death from old age or other reasons.


**Q: What are the diseases that tend to be co-morbid with diabetes?**

Diseases related to the cardiac, urinary and body fluid PH levels.


**Q: Which demographics have higher morality rates??**

There is an increase in the number of deaths among patients over 60 years old, increasing every decade until years 80-90. <br> Women are only slightly more likely to die than men.


**Q: Is there demographic bias in the care received?**

Surprisingly, that does not seem to be the case.<br>
The patients all received very similar numbers of lab procedures, medications, and stayed for roughly the same amount of days in the hospital. 


**Q: Does a longer hospital stay reduce later readmission?**

No, the reverse situation seems to be true.<br>
Patients who were not readmitted or only readmitted 30 days after the last visit had spent similar days in the hospital, but patients who stayed longer last time also came in much sooner after being discharged.<br>
It's more likely that the more severe the patients' diabetes is, the longer their stay, and the sooner they return.


**Q: What do the records of the "most problematic" patients look like?**
The number of medications prescribed to the top 10 patients does not plateau or lower over time - this indicates that their condition was constantly changing rather than being stabilized.
