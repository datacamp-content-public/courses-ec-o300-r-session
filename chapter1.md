---
title: 'Chapter Title Here'
description: 'Chapter description goes here.'
---

## Example coding exercise

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
Assign (<-) the new name to the variable that you want to change name:  
names(dataset)[names(dataset)=="oldname"]) <- "newname"
The dataset name is ACS (the same dataset as used in class):

`@pre_exercise_code`
```{r}
ACS <- read.csv("ACS2017_R1-part1.csv",header=TRUE)
```

`@sample_code`
```{r}
names(ACS)
```

`@solution`
```{r}
names(ACS)[names(ACS)=="sex"]) <- "gender"
```

`@sct`
```{r}
names(ACS)[4]=="gender"
# the 4th variable name should now be "gender"
```
