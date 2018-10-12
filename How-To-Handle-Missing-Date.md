## Tutorial on How to Handle Missing Data:

Real-world data often has missing values. For example imagine you have a dataset containing list students (boys & girls) in a college with various attributes (height, weight, age etc.). 

Unfortunately, on previewing the data you find few students height and weight are missing. Now let us ask some questions to ourselves like:

  - Can you accurately find a way out off handling the missing heights/ weights?
  - Should one just pretend as if the missing instances isn’t missing.?
  - Should one go and ask those students for their height/ weight? (Not feasible!)
  - Or can one just predict the shape of the missing instances based on previous experience?

Data can have missing values for a number of reasons such as: observations that were not recorded and data corruption. Handling missing data is important as many machine learning algorithms do not support data with missing values.

In this tutorial, you will learn how to handle missing data for machine learning with Python. Let’s get started.

1. **Step 1: Preview the Data**
   - Expolore the data and see if you can observe some pattern. 
   - Learn how different features correlate with each other. 
   - Try to understand significance of each feature with respect to the problem.
        
2. **Step 2: Check Missing Values**
   - Use pandas isnull() function on data frame/ column.
   ```
   # count the number of NaN values in each column
   df.isnull().sum()
   ```

3. **Step 3: Mark missing values**
   - We mark missing values as NaN
   - Values with a NaN value are ignored from operations like sum, count, etc.
   - Use the replace() function on columns
   ```
   # mark zero values as missing or NaN
   df[[1,2,3]] = df[[1,2,3]].replace(0, np.NaN)
   ```
   
4. **Step 4: Remove Missing Values**
   - Simplest strategy for handling missing data is to remove records that contain a missing value.
   - Creating a new Pandas DataFrame with the rows containing missing values removed.
   - Use dropna() function in pandas. that can be used to drop either columns or rows with missing data.
   ```
   # keep the DataFrame with valid entries in the same variable.
   df.dropna(inplace=True)
   ```
   
5. **Step 5: Impute Missing Values**
   - Imputing refers to using a model to replace missing values.
   - There are many options we could consider when replacing a missing value, for example:
     - A constant value that has meaning within the domain, such as 0, distinct from all other values.
     - A value from another randomly selected record.
     - A mean, median or mode value for the column.
     - A value estimated by another predictive model.

Any imputing performed on the training dataset will have to be performed on new data in the future when predictions are needed from the finalized model. This needs to be taken into consideration when choosing how to impute the missing values.

For example, if you choose to impute with mean column values, these mean column values will need to be stored to file for later use on new data that has missing values.

Pandas provides the fillna() function for replacing missing values with a specific value.

6. **Step 6: Use different algorithms that support missing values.**
   - 


