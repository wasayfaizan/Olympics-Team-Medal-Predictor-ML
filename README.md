<body>
    <h1>Olympics Medal Prediction - Data Analysis</h1>
    <div class="section">
        <h2>Project Overview</h2>
        <p>This project is focused on analyzing data from the Olympics Games, predicting the number of medals won by different countries based on various features such as the number of athletes, previous medals, and other factors. The dataset consists of Olympics participation data from 1964 to 2016. The goal is to build a model to predict the number of medals won by each country in future Olympic Games.</p>
    </div>
    <div class="section">
        <h2>Dataset</h2>
        <p>The dataset contains information about Olympic teams, including:</p>
        <ul>
            <li><strong>team</strong>: The abbreviation for the country</li>
            <li><strong>country</strong>: Full name of the country</li>
            <li><strong>year</strong>: The year of the Olympics</li>
            <li><strong>athletes</strong>: Number of athletes representing the country</li>
            <li><strong>age</strong>: Average age of athletes</li>
            <li><strong>prev_medals</strong>: Number of medals won in the previous Olympics</li>
            <li><strong>medals</strong>: Number of medals won in the current Olympics</li>
        </ul>
        <p>Example dataset snippet:</p>
        <pre>
team  country     year  athletes  age  prev_medals  medals
0    AFG  Afghanistan  1964  8  22.0  0.0  0
1    AFG  Afghanistan  1968  5  23.2  0.0  0
2    AFG  Afghanistan  1972  8  29.0  0.0  0
        </pre>
    </div>
    <div class="section">
        <h2>Data Preprocessing</h2>
        <p>The data was cleaned and transformed to remove irrelevant columns and handle missing values:</p>
        <ul>
            <li>Columns such as 'team' and 'country' were removed for analysis.</li>
            <li>Null values in the dataset were dropped.</li>
        </ul>
        <p>After preprocessing, the data looks like this:</p>
        <pre>
team  country     year  athletes  age  prev_medals  medals
0    AFG  Afghanistan  1964  8  22.0  0.0  0
1    AFG  Afghanistan  1968  5  23.2  0.0  0
2    AFG  Afghanistan  1972  8  29.0  0.0  0
        </pre>
    </div>
    <div class="section">
        <h2>Correlation Analysis</h2>
        <p>The correlation between various features and the number of medals was analyzed. The highest correlation was found between the number of athletes and the number of medals won:</p>
        <pre>
athletes    0.840817
prev_medals 0.920048
medals      1.000000
        </pre>
        <p>This indicates that the more athletes a country has, the higher their likelihood of winning medals. The number of previous medals also correlates highly with the number of medals won.</p>
    </div>
    <div class="section">
        <h2>Modeling</h2>
        <p>A linear regression model was built using the number of athletes and previous medals as the predictors. The model was trained on data from 1964 to 2012 and tested on data from 2012 to 2016.</p>
        <p>The model's predictions for the test dataset are shown below:</p>
        <pre>
team  country     year  athletes  age  prev_medals  medals  predictions
6    AFG  Afghanistan  2012  6  24.8  1.0  1  0.0
7    AFG  Afghanistan  2016  3  24.7  1.0  0  0.0
        </pre>
    </div>
    <div class="section">
        <h2>Performance Evaluation</h2>
        <p>The model's performance was evaluated using the mean absolute error (MAE) metric, which was calculated as follows:</p>
        <pre>
MAE = 3.30
        </pre>
        <p>This indicates that the model's predictions are fairly close to the actual number of medals won, with an average error of 3.30 medals.</p>
    </div>
    <div class="section">
        <h2>Conclusion</h2>
        <p>The model was able to predict the number of medals won by countries with reasonable accuracy, and the features used (number of athletes and previous medals) proved to be highly correlated with the medal count. Further improvements could involve exploring more features, such as the country’s GDP or investment in sports.</p>
    </div>
    <div class="section">
        <h2>How to Run the Code</h2>
        <p>1. Install the required libraries:</p>
        <pre>
pip install pandas seaborn scikit-learn
        </pre>
        <p>2. Run the Python script containing the code for data preprocessing, correlation analysis, modeling, and evaluation.</p>
        <p>3. Ensure the 'teams.csv' file is in the same directory as the script.</p>
    </div>

</body>
</html>
