## Diabetes Patients Data Analysis

You can use the [editor on GitHub](https://github.com/tapatia/dats6103_p3/edit/main/README.md) to maintain and preview the content for your website in Markdown files.

Whenever you commit to this repository, GitHub Pages will run [Jekyll](https://jekyllrb.com/) to rebuild the pages in your site, from the content in your Markdown files.

Markdown is a lightweight and easy-to-use syntax for styling your writing. It includes conventions for

```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```
For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/tapatia/dats6103_p3/settings). The name of this theme is saved in the Jekyll `_config.yml` configuration file.



### 1. Motivation and Questions

According to the CDC, over 34 million Americans have diabetes, just a little over 1 person among every 10.
In light of this prevalence, I wanted to answer the following questions:

- Which demographic groups are overrepresented among diabetes patients?
- What are the diseases that tend to be co-morbid with diabetes?
- Which demographics have higher morality rates??
- Is there demographic bias in the care received?
- Does a longer hospital stay reduce later readmission?
- What do the records of the "most problematic" patients look like?


### 2. Dataset Source and Cleaning 

This dataset was imported without any changes from the UC Irvine Machine Learning Repository, accessible [here](https://archive.ics.uci.edu/ml/datasets/Diabetes+130-US+hospitals+for+years+1999-2008).

The original data was extracted from the Health Facts database, a voluntary program offered to organizations which use the Cerner Electronic Health Record System. Clinical care data was collected from 130 hospitals and integrated delivery networks throughout the U.S., from 1999 - 2008. Only inpatient visits where the patient had diabetes as an existing condition were included. More details on the data selection methodology can be accessed [here](https://www.hindawi.com/journals/bmri/2014/781670/).

The steps in cleaning and pre-processing are, listed in order:
1. the removal of columns that contained over 50% NA values
2. the removal of rows wwith Null, Not Mapped, or Not Available entries for demographic columns
3. the removal of rows whose diagnosis is NA or not numeric
4. the rearranging of columns to leave all medicines for last 
5. the shortening of column names for ease of understanding
6. the creation of two new cleaned dataframes, one for encounters (each visit), and one for patients (the first visit for each recorded patient) 


### 3. Analysis and Jupyter Notebook

The Jupyter notebook is accessible through the repository [here](https://github.com/tapatia/dats6103_p3/blob/main/DATS%206103%20-%20Individual%20Project%203%20-%20Dai%20Wei%20Tsang.ipynb). 




### 4. Conclusion





