# foster-06-eda
# Project 6.2
## Penguins Dataset
### Purpose: Perform and publish a custom EDA project to demonstrate skills with Jupyter, pandas, Seaborn and popular tools for data analytics using the seaborn penguins dataset.
Dataset [here](https://github.com/mwaskom/seaborn-data/blob/master/penguins.csv)
Author: Lindsay Foster
Date: February 2025

## Install and Run
- Create a GitHub project repository with a default README.md. 
- Clone the repository down to the machine into the Documents folder. 
- Open the repository folder in VS Code. 
- In VS Code, add a .gitignore file, a requirements.txt, and a python folder with imports. 
- Install the imports: jupyterlab, numpy, pandas, pyarrow, matplotlib, and seaborn in the terminal.
- Create a jupyter notebook for this project. 
- Commit these changes to the remote repository using
`git add .
git commit -m "message"
git push`

## Data Acquisition
- Load the dataset into a pandas DataFrame.
`penguins = sns.load_dataset('penguins')`
`df = sns.load_dataset('penguins')`
- Inspect first rows of the DataFrame. 
`print(df.head())`
- Display the first 10 rows to make sure it loaded correctly. 
`print(df.head(10))`
`print(df.shape)`
`print(df.shape)`
`print(df.dtypes)`
- Display a summary of statistics for each column.
`print(df.describe())`

## Data Distribution and Visualization
Create many plots and graphs to visualize the data in various ways: 
1. Show all plots
2. Inspect value counts by categorical column
3. Create scatterplots between all numerical variables, colored by species.
4. Create a boxplot to show the variation in bill length for each species of penguin.
5. Create a FacetGrid to show a scatterplot of bill length vs. bill depth for each species.
6. Create a barplot to display the average body mass of each species.
7. Create a striplot to show how bill depth values are distributed across species, with individual points displayed.
8. Create a countplot to sho how many penguins of each species are in the dataset.
9. Create a KDE plot to show the smoothed distribution of bill lengths for each species.
10. Create the combination of a boxplot with a stripplot to show both summary statistics and individual data points.

## Initial Data Transformation and Feature Engineering
- Rename the species by: 

    - Load the penguins dataset:
    `penguins = sns.load_dataset('penguins')`

    - Rename the "species" column to "penguin_species":
    `penguins.rename(columns={'species': 'penguin_species'}, inplace=True)`

    - Display the first few rows to verify the change:
    `print(penguins.head())`

- Create a new column. The new column "size_category" is added based on the body_mass_g. Penguins with body mass below 3500 grams are categorized as "Small", those with body mass between 3500 and 5000 grams are "Medium", and those with body mass above 5000 grams are categorized as "Large".

    - Load the penguins dataset:
    `penguins = sns.load_dataset('penguins')`

    - Check if the dataset loaded properly and contains the 'body_mass_g' column:
    `print(penguins.columns)`

    - Define the function to categorize body mass:
`def categorize_size(row):
    if row['body_mass_g'] < 3500:
        return 'Small'
    elif 3500 <= row['body_mass_g'] <= 5000:
        return 'Medium'
    else:
        return 'Large'`

    - Apply the function across rows to create a new column "size_category":
    `penguins['size_category'] = penguins.apply(categorize_size, axis=1)`

    - Display the first few rows to verify the new column:
    `print(penguins[['species', 'body_mass_g', 'size_category']].head())`


