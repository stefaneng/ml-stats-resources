# Categorical Data

In algorithms such as logistic regression, data is assumed to be numeric.
Not all data is numeric though.

Examples of non-numeric data:
  - Gender
  - Nationality
  - Occupation
  - Language

and much more.

## Handling Non-Numeric Features

### Option 1
Use algorithms that support categorical data such as:
  - Decision Trees
  - Naive Bayes
  - Etc..

### Option 2
Convert these features to numeric features so we can use any learning method.

## Types of Non-Numeric Features

### Categorical
  - Has two or more categories
  - No intrinsic ordering to the categories
  - E.g, Gender, Country, Occupation, Language

### Ordinal
  - Has two or more categories
  - Intrinsic ordering, but no consistent spacing between the ordering (relatively ordered).
  - Often seen in survey questions, e.g., "Is your health poor, reasonable, good, or excellent".

## Non-numeric => Numeric

### One Idea
Create single numeric feature to represent non-numeric one.

#### Ordinal Features
```
poor, reasonable, good, excellent
```
would map to
```
poor = 1, reasonable = 2, good = 3, excellent = 4
```

This preserves ordering, but introduces a degree of closeness that didn't previously exist.

#### Categorical Features
```
ARG, FRA, USA
```

would map to
```
ARG = 1, FRA = 2, USA = 3
```

Which implies that FRA is between ARG and USA.

The big problem with this approach is that a single numerical feature introduces relationships between categories that don't otherwise exists.

### One-Hot-Encoding
Create a dummy feature for each category.

The categorical features
```
ARG, FRA, USA
```

would introduce new features
```
ARG => [1, 0, 0]
FRA => [0, 1, 0]
USA => [0, 0, 1]
```
These dummy features don't imply anything beyond the original categories.

#### Computing Features
If we have multiple categories
