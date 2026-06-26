# Exploratory Data Analysis (EDA)

###  Workflow of EDA 
```mermaid
flowchart LR
A@{ shape: tag-rect, label: "What have i got?" }==>B@{ animate: true, shape: tag-rect, label: "Is it clean?"}==>C@{ shape: tag-rect, label: "What's in it?"}==>D@{ shape: tag-rect, label: "What conclusions can we dreive?"}
```

## Introduction
When we are working with a dataset, we want to be able to ask questions such as *"is this good data?"* or *"what questions can it answer for us?"*
EDA (Exploratory Data Analysis) is the process of cleaning and reviewing data, in order to gain insights such as descriptive stats and correlation and be able to generate hypotheses for experiements. EDA is useful because it allows us to take the next steps for the dataset, like generating a hypothesis, preparing data for a machine learning  model or deeming that the data is insufficient/irrelevant.

### "How do we explore the data?"
Initially, we import the data and utilise a few key pandas methods in order to grasp what we're working with.

```python
books = pd.read_csv("book_sales.csv") # Import the .csv file

books.head() # Get the top 10 columns of the dataset

books.describe() # DESCRIBES your data through summary statistics

books.info() # Col names, data types and missing values

books.value_counts() # To check categorical values
```
### Validating data types

To check the type value

```python
# Checking the type of values

books.dtypes

# Or just a single column

books["sales"].dtype
```

To change type value

```python
# Change the entire column

books["sales"].astype("float")
```
