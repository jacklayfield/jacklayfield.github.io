---
tag: Machine Learning
permalink: machine-learning-notes
---

## Machine Learning Tips / Best Practices

As I progress through machine learning courses and projects, I thought it would be useful to keep an area for tips and best practices that I pick up along the way. Maybe others will find it useful as well!

(This is an ongoing post that will be updated periodically from my "MachineLearning" repository [Notes](https://github.com/jacklayfield/MachineLearning/blob/main/notes.md))

---

<h4 style="color:#bcffe5">Inspecting / Exploring the data:</h4>

- Use horiztonal histograms when possible
- It is important to thoroughly check out the data before jumping right into training in order to fully understand the data.

<h4 style="color:#bcfff4">Visualization must haves:
</h4>

- run histograms on the entire data set
- run histograms on columns you are most interested in
- plot any geographic data
- correlation matrix (preferred)

<h4 style="color:#bcffff">Training / Test sets:</h4>

- ~66% train and ~33% test is reccomended (Or ~80% train and 20% test)
- visualize train and test set to ensure they are similar. Very important that they are not signifigantly different. Use a stratified split if this is hard to achieve (gets you even distribution).
- Look at test set as little as possible, you want to be unbiased.

<h4 style="color:#bcecff">Preparing data:</h4>

- To deal with missing data in columns you can either delete the rows with the missing column data, delete the column entirely or perform imputation.

<h4 style="color:#bce6ff">General:</h4>

- Code is read way more than it is written, use conventions whenever possible.
- ALWAYS VISUALIZE DATA (Don't just trust the stats)
- matplot lib is ok, but plotly power bi or tableu (mac) are better.
- sklearn will transform things into numpy arrays which are bad for data visualization. Use pandas DataFrame to convert these for visualization purposes.
- Use an ordinal encoder when you have categories that have an order to them (ex. good, better, best). If not objectively better, use a hot encoder. Hot encoder will avoid bias.

<h4 style="color:#bcdbff">Feature engineering:</h4>

- Science of using domain knowledge to create new features (columns) of data using raw data.

<h4 style="color:#bcd1ff">Scaling data:</h4>

- Columns with unintentionally higher values will skew calculations. Always scale your data.

<h4 style="color:#c0bcff">Validation:</h4>

- Use K-Fold Cross-Validation to validate our data. This will divide out set into a specified number of folds (10) and train on 9 while testing on the last.

<h4 style="color:#d0bcff">Fine Tuning:</h4>

- After picking a model you need to fine-tune the hyper paramaters (parameters unaffected by training) in order to find the ideal ones for a given model. You can use Grid Search.
- Grid Search may take a long time due to it searching every single feature in the feature space. Try randomized search for large feature space.
