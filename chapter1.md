---
title: 'Chapter Title Here'
description: 'Chapter description goes here.'
---

## Data management

```yaml
type: NormalExercise
key: 2bafef99a3
lang: r
xp: 100
skills: 1
```

Data Management 1 - Change variable name

`@instructions`
Change the name of the "sex" variable to "gender"

`@hint`
# Assign (use <-) the new name to the variable that you want to change the name:  
Generic syntax: names(dataset)[names(dataset)=="oldname"]) <- "newname"
The dataset name is ACS (as in the class example):

`@pre_exercise_code`
```{r}
ACS <- read.csv("ACS2017_R1-part1.csv",header=TRUE)
```

`@sample_code`
```{r}
# get the names of variables in the dataset:
names(ACS)
# let's check that the 4th variable is in fact named as "sex":
names(ACS)[4] == "sex"
# assign a new name to the variable "sex":

```

`@solution`
```{r}
names(ACS)[names(ACS)=="sex"] <- "gender"
```

`@sct`
```{r}
# the 4th variable name should now be "gender"
is_equal(names(ACS)[4], "gender", eq_condition = "equivalent") 
```
