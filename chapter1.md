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
Using the dataset mtcars, assign the name "cylinders" to the existing variable named "cyl":

`@hint`
The names of variables can be listed using the command names(mtcars), where mtcars is the name of the dataset that you are using.
Thus, to get the name of the variable "cyl", write:  
``` {r}
names(mtcars)[names(mtcars)=="cyl"]
```
Then, assign the new name "cylinders" to replace the name of that variable. To assign the new name, use the assign operator "<-".

`@pre_exercise_code`
```{r}
data(mtcars)
```

`@sample_code`
```{r}
# get the names of the variables in the dataset:
names(mtcars)
# let's check that the 2nd variable is in fact named as "cyl":
names(mtcars)[4] == "2"     # the result should be "TRUE"
# assign a new name to the variable "cyl":

```

`@solution`
```{r}
names(mtcars)[names(mtcars)=="cyl"] <- "cylinders"
```

`@sct`
```{r}
# the 2nd variable name should now be "cylinders"
ex() %>% check_function(names(mtcars)[2]=="cylinders") %>% check_result() %>% check_equal() 
```
