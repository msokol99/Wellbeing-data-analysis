# Wellbeing Data Analysis
 
### Files in the repo:
- data_analysis.ipynb - the actual analysis file
- results_survey.csv - the raw .csv file exported from our online survey
- output.png - correlation matrix for all items
- output_strong.png - filtered correlation matrix (threshold = 0.6)
- data_excel.xlsx - *ALMOST* cleaned data & exported to the Excel file for visibility
- correlations.xlsx - correlation matrix in the form of a dataframe (it made it easier to see the labels of the items)

### What was done so far?
1. I checked if all the participants in the survey signed all the consents and I deleted the columns with these consents.
2. I scored/coded the responses according to their respeective scales. I found errors in some of them, for example, "somewhat agree" would surprisingly correspond to the number "8", even though it was a typical Liekert scale, on which "somewhat agree" would typically correspond to the number "4". In other instances, the responses were flipped - "strongly disagree (1)" would become "strongly disagree (7)", or vice versa. I aimed to unify the responses to the best of my ability but there still might be some errors.
3. I created correlation matrices - an unfiltered and a filtered one (with threshold = 0.6).
4. I created the curve of the explained variance by the compartments and I picked 20 as a pretty good number, since it explains almost 80% of the variance.
5. I tried to visualize the compartments

### What could potentially be done?
- review/checking if there are any errors
- finishing up the data cleaning part - this could involve, for example, checking
- some columns still need to be handled somehow. Maybe *binning* could be useful for some categories, such as the participants' salary. You can find the columns that I left unhandled by accessing the data_excel.xlsx file
- at the point where I try to create the correlation matrix, I think I got rid of NaN values, because NaN values were actually those remaining non-numeric values that I had not yet handled anyhow
- brainstorming what else can be done with the data? How to make sense of the results of the PCA? The current number of principal compartments is 20, which explains ~78% of the variance. Maybe we could change this number? How to access the compartments themselves?
