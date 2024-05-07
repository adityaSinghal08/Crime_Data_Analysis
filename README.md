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
