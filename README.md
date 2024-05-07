The dataset is quite large and hence can't be uploaded here. You can download the dataset by visting this <a href="https://data.world/dcopendata/crime-incidents-in-2011/workspace/file?filename=Crime_Incidents_in_2011.dbf">link</a>.

<h1>About the Dataset</h1>

<p>This dataset is an instance of many crime registered in the Columbia city of USA in the year 2011. Here each record represents a particular registered crime. This dataset consists of various fields, out of which our primary focus will be on five particular fields. These fields are reporting date, shift, method, offense, and district.</p>

<h2>About the Columns</h2>

<h3>Reporting Date</h3>

<p>This column (initially of the name report dat) represents the date on which the crime was registered. Initially, its entries are of the format 'yyyy-mm-dd + T + hh.mm.ss.mmm'. Our aim is to convert these entries into the 'dd-mm' format. Futhermore, we will be creating a reporting month column so that we can study the montly crime trends.</p>

<h3>Shift</h3>

<p>This column represents the shift during which the crime was registered. There are three values that this field contains. These are day, evening and midnight.</p>

<h3>Method</h3>

<p>This column represents the method using which the crime was commited. There are three values that this field contains. These are knife, gun and others (if the crime was carried out using any means other than a knife or a gun).</p>

<h3>Offense</h3>

<p>This column represents the nature of the crime. Initially this column contains many unique values. Our goal is to categorise the crime into of the eight categories based on its nature. These categories are burglary, motor vehicle theft, homicide, sex abuse, assault, robbery, arson, and other theft (if the crime does not fit into the first seven categories).</p>

<h3>District</h3>

<p>This column indicates the district in which the crime occurred. Initially this column contains values in the form 'Cluster n', where n indicates a cluster number pre-defined by the authrities. Our goal is to convert these values into the integer n.</p>

<br>

<p>Other than the columns named above, we have also retained the case id column (initially of the name ccn), the neighbourhood column (initially of the name neighborho), and the precinct column (initially of the name voting pre). The case id column can be used to uniquely identify a registered crime. Although the use of the other two columns is close to none during the analysis, these may still serve as a good measure to identify the crime trends.</p>

<p>Using this dataset we will be studying crime trends over various fields. We will also be analysing the relationship between our primary fields. Based on the observed crime trends, we will be deriving appropriate conclusions.</p> 

<h1>Pre-Processing</h1>

<p>In this section, we will be preprocessing the dataframe for it to achieve our desired format. Most of the preprocessing necessities are already described above in the dataset section. Other than that, we will be checking for any null values in our dataset. In such a case, depending on the number of missing values, we will be either dropping such records or taking in place other appropriate measures to handle the missing values</p>

<h1>Individual Column Trends</h1>

<p> In this section, we will be analysing the crime trends for all of our reatined columns individually. That is, we will be studying how crime trends varies over a particular field.</p>

<h1>Pair-wise Column Trends</h1>

<p>In this section, will be analysing how crime trend varies with respect to any two of our primary fields. That is, we will be studying how crime trends varies over a field with repect to another field.</p>

<h1>Dependencies between Fields</h1>

<p>In this section, we will be checking whether any of our primary field is dependent on other primary fields. For this task, we will be performing chi-squared test under the null hypothesis of independence for our 10 primary fields pairs. On performing a chi-squared test, we will obtain a p-value which will help us decide whether to reject our null hypothesis of independence or accept it.</p>

### Interpretation of p > 0.05 in a Chi-Squared Test

- **No Significant Association:** No strong evidence of an association between categorical variables.

- **Fail to Reject Null Hypothesis:** Data does not provide enough evidence to reject the assumption of independence between variables.

- **Independence Assumption:** Observed frequencies in the contingency table are not significantly different from expected frequencies under independence.

- **Caution in Interpretation:** Lack of statistical significance doesn't imply the absence of an association; it suggests insufficient evidence based on the data.


### Interpretation of \( p < 0.05 \) in a Chi-Squared Test

- **Significant Association:** Strong evidence of an association between categorical variables.

- **Reject Null Hypothesis:** Data provides sufficient evidence to reject the assumption of independence between variables.

- **Dependent Variables:** Observed frequencies in the contingency table significantly differ from expected frequencies under independence.

- **Interpretation Confidence:** Confidence in concluding that a relationship exists based on the observed data.

## Proportion Distribution: An alternate to the Central Limit Theorem (CLT)

When dealing with categorical data, we often want to understand the distribution of proportions of different categories within a dataset. Proportion distribution refers to the distribution of the relative frequencies of each category within a sample or population. It helps us understand how the proportions of different categories vary across different samples or populations.

Proportion distribution is similar to the Central Limit Theorem (CLT) in the context of sampling from a population. According to the CLT, the distribution of sample means approaches a normal distribution as the sample size increases, regardless of the shape of the population distribution, under certain conditions.

Similarly, when we repeatedly sample from a population and compute the proportions of different categories within each sample, the distribution of these proportions tends to approximate a normal distribution as the sample size increases. This is known as the proportion distribution and is analogous to the CLT for sample means.

In essence, both the CLT and proportion distribution deal with the behavior of sample statistics (means and proportions, respectively) as we take multiple samples from a population. They both demonstrate the tendency of sample statistics to follow a normal distribution, making them valuable tools in statistical analysis and inference.

In this section, we will be examining the proportion distribution of each unique value for each of our primary fields. Since all of our columns are interdependent, we expect that the proportion distribution will faintly approximate a normal distribution.
