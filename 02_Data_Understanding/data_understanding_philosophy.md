### Phase 02: Data Understanding

---

In this chapter, **we cover the next CRISP-DM Step: Data Understanding.** We take a pause with the BSPF while we **get to know the data and begin the process of preparing for modeling.** In this chapter, you will learn:

* Techniques for effectively analyzing the features in dataset
* How to use the skimr package for data investigation by data type
* How to use the GGally package for visual data investigation

### WHERE WE ARE AFTER 'BUSINESS UNDERSTANDING' PHASE

In the business understanding phase we gathered enough data to:

1. Better understand the business problem.
2. Glean insights and share with stakeholders.
3. Sized the problem to investigate if it's worth our time e.g., 1k problem vs. 1M dollar problem.

### DATA UNDERSTANDING WORKFLOW (2nd phase of CRISP-DM)

This is where we collect and dive into, exploring our data.

* **Preparation Needed Prior to beginning Phase:** Ideally, we've collected data and interatively met with stakeholders to **Understanding the Business Problem.** In the beginning it's best to start with simple data and iteratively move toward gathering, importing, and tidying your data to move towards modeling it.

### High Level Goals
1. Collect & Compile Data (engineer features, etc.)
2. Exploratory Data Analysis (EDA): Identify critical properties of the underlying features (Independent/Predictor Variables) and potential relationships between them and our Target (Response/Dependent Variable).

### Tools we will use to be Highly Effective & Efficient (EDA R Packages)
1. skimr package: Review many features by datatype.
2. GGally package: Excellent package for visualizing relationships between a Target Variable & the Features w/in our Data.

### THE WORKFLOW FOR DATA UNDERSTANDING PHASE

By now your data should have all the predictor features along with the target feature i.e., Tidy Data.

1. **Glimpse() Function** to View data and understand various ways features can be grouped into feature categories.
   * Question to ask: How do these features relate together (e.g., descritive features, time-based, department, etc.).
   * **Pro-Tip:** Breakdown data collection activities in to strategic areas.
2. **EDA Part 1: Explore Summary Stats** -- Data Summarization w/skimr::skim()
    * Investigating the Summarized Feature Attributes.
      1. **Skim()** returns summary by data type. This includes missing values and number of unique features for categorical data. For numeric data, it returns the histogram and quantiles.
    * **Objective:** High-Level understanding of My Data -- E.g., missing values, feature distribution(s), etc.
      1. **Pro-Tip:** Separating your data by data type (numerical vs. categorical) is a great way to investigate properties of the data. This is really the first attack on understanding my data. **These two data-types should be thought about differently.**
    * **CHARACTER DATA (or Factor)** is typically categorical: Consider each & if there is anything interesting individually.
        * **GOAL HERE:** Contain Character/Category features and investigate their proportions (**see code example**). This moves us towards better understanding our population.
        * **Pro-Tip:** If the number of unique categorical features is large, consider creating an "other" category. This is b/c there may in fact be a better way to group on the data. And those with only 1 category are useless for modeling (zero-variance features).

     * **Numeric Data:** Can be analyzed by its distribution (mean, std dev, & quantiles) -- It's a bit more descriptive b/c of these summary statistics. Keep an eye out for Numeric Data that may be better suited for categorical data (e.g., they have levels).
        * **Discrete Features:** Some numeric features may not be continuous, and are actually categorical. These are called discrete features b/c they have defined levels even though they are stored as numeric. They typically should be converted to categorical (i.e. factor) data types.
        

# left off midway through video on numeric data

* **EDA Part 2: Explore Data Visually** -- Visual Data Analysis w/GGally::ggpairs()
* Investigate the Predictor/Target Relationships.









