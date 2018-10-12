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
   - Use 

3. **Step 3: Mark missing values**
   - Wee mark missing values as NaN
   - Values with a NaN value are ignored from operations like sum, count, etc.
   - We can mark values as NaN easily with the Pandas DataFrame by using the replace() function on a subset of the columns we are interested in.
   ```
   # mark zero values as missing or NaN
   df[[1,2,3]] = df[[1,2,3]].replace(0, np.NaN)
   ```
4. **Step 4: Remove Missing Values**

5. **Step 5: Impute Missing Values**

6. **Step 6: Use different algorithms that support missing values.**


