# foster-06-eda
# Project 6.2
## Penguins Dataset
### Purpose: Perform and publish a custom EDA project to demonstrate skills with Jupyter, pandas, Seaborn and popular tools for data analytics using the seaborn penguins dataset.
Dataset [here](https://github.com/mwaskom/seaborn-data/blob/master/penguins.csv)

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

## Initial Data Transformation and Feature Engineering

