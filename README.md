<h1 id="toc_0">King County Housing Prices</h1>

<h2 id="toc_1">Overview</h2>

<p>This project seeks to develop a predictive model in for housing prices in King County, Washington. Investigation and final modeal are based on the file <code>&#39;kc_house_data_test_features.csv&#39;</code>(found in Resources folder), which is a dataframe of houses sold in 2014 and 2015 in King County, Seattle.</p>

<h2 id="toc_2">Business Problem</h2>

<p>We will explore the following business questions:</p>

<ul>
<li><p>How does the number of bedrooms and bathrooms determine the selling price of a house?</p></li>
<li><p>How does the condition of a house determine selling price?</p></li>
<li><p>How does the square footage determine selling price?</p></li>
<li><p>Does renovation influence the selling price?</p></li>
</ul>

<p><img src="./Resources/heatmap_original.png" alt="heatmap"></p>

<h2 id="toc_3">Analysis</h2>

<p>A first look at an initial heatmap of our features immediately shows the most meaningful correlations to price are the square footage of the living space (<code>sqft_living</code>), and the building construction rating (<code>grade</code>). Trailing closely behind we can also see that bathrooms and view are strong indicators as well.</p>

<ul>
<li><p><strong>highest correlations:</strong> <code>bathrooms</code> <code>sqft\_living</code> <code>grade</code> <code>sqft\_above</code> <code>sqft_living15</code> </p>

<ul>
<li>check for outliers and extreme values</li>
<li>sqft_living seems like a better predictor, interact this variable with others</li>
</ul></li>
<li><p><strong>low correlations to check out:</strong> <code>bedrooms</code> <code>waterfront</code> <code>view</code> <code>condition</code> <code>renovation</code> </p>

<ul>
<li>manipulating data into dummy variables helps with correlation (create dummy variables for <code>renovation</code> <code>view</code> <code>condition</code>)</li>
</ul></li>
</ul>

<ul>
<li>Reign in outliers for variables with sqft</li>
<li>Inspect extreme outliers:

<ul>
<li>&#39;11&#39; and &#39;33&#39; bedrooms </li>
<li>&#39;0&#39; bathrooms</li>
</ul></li>
</ul>

<h3 id="toc_5">Initial Investigation</h3>

<ul>
<li>Investigate binomial variables using statistical tests</li>
<li>Generate new features that will be useful</li>
</ul>

<p><img src="./Resources/statistical_tests.png" alt="statistical tests"></p>

<p>There is a stark increase in value for waterfront property as opposed to inland. It can also be determined that there is a statistically significant increase in price for homes that have a basement and homes that have been renovated.</p>

<h2 id="toc_6">Findings</h2>

<p>We can deduce that the highest selling homes have larger than average interior square footage and are in neighborhoods surrounded by other large homes, and/or where a high level of attention is paid to construction grade.</p>

<p>It was particularly surprising to see that a property&#39;s view, condition quality rating, and the number of bedrooms were fairly weak indicators of price. With the unexplainable outliers within this dataset, we may need additional information in order to better fit our model. </p>

<h2 id="toc_7">Next Steps</h2>

<p>I would like to take a closer look at outliers in order to bin categories to keep the model more streamlined. I would also seek outside sources such as information on school districts, records of parks, and local attractions.</p>
