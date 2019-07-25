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
Using the dataset ACS, assign the name "gender" to the existing variable named "sex":

`@hint`
The name of a variable can be listed using the command names(myDS), where myDS is the name of the dataset that you are using.
Thus, to get the name of the variable "sex", we can write:
names(myDS)[names(myDS)=="oldname"])
Now, assign the new name "gender" as the replacement for the name of this variable.
To assign, use the assign operator "<-".

`@pre_exercise_code`
```{r}
ACS <- read.csv("ACS2017_R1-part1.csv",header=TRUE)
```

`@sample_code`
```{r}
# get the names of the variables in the dataset:
names(ACS)
# let's check that the 4th variable is in fact named as "sex":
names(ACS)[4] == "sex"     # the result should be "TRUE"
# assign a new name to the variable "sex":

```

`@solution`
```{r}
names(ACS)[names(ACS)=="sex"] <- "gender"
```

`@sct`
```{r}
# the 4th variable name should now be "gender"
ex() %>% check_function(names(ACS)[4]=="gender") %>% check_result() %>% check_equal() 
```
