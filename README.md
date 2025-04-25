# Titatic_data_cleaning
<p>This project showcases a full data preprocessing pipeline applied to the Titanic dataset. The goal is to transform raw passenger data into a clean and structured format suitable for machine learning tasks. The workflow covers null value treatment, feature encoding, scaling, outlier removal, and final dataset export.</p>
<h2> Project Summary</h2>
<p>
The Titanic dataset contains demographic and travel details of passengers aboard the RMS Titanic. This notebook focuses on:
Cleaning data by addressing missing and inconsistent entries
Encoding categorical variables for model compatibility
Scaling numerical features to standardize values
Identifying and removing outliers that could distort predictions
</p>
<h2>Processing Workflow</h2>
<h3>1. Data Loading</h3>
<p>The dataset is loaded using pandas.read_csv() from a remote source. Initial structural and statistical information is reviewed using .info() and .describe().</p>
<h3>2. Null Value Handling</h3>
<p>Age: Filled with median to minimize skew.
Embarked: Filled using mode (most common port).
Cabin: Dropped due to extensive missing values.</p>
<h3>3. Categorical Encoding
</h3>
<p>Sex: Converted to numeric values (male → 0, female → 1).
Embarked: Converted using one-hot encoding, keeping two of the three categories (Embarked_Q, Embarked_S).</p>
<h3>4. Feature Scaling</h3>
<p>Numerical columns Age and Fare are standardized using StandardScaler to bring them to a common scale (mean=0, std=1).</p>
<h3>5. Outlier Removal</h3>
<p>Outliers in Age and Fare are detected using the Interquartile Range (IQR) method and removed to improve model robustness.</p>
<h3>6. Exporting Cleaned Data</h3>
<p>The cleaned dataset is saved as cleaned_titanic.csv for downstream machine learning workflows.</p>
<h3>📊 Visualization
A boxplot of the Age and Fare columns is created using Seaborn to visualize the distribution and detect potential outliers</h3>
