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

Data Management 1 - Create new variable and calculate its mean

`@instructions`
Using the dataset mtcars, create the new variable "efficiency" which should equal to ratio of horsepower to gallons of gasoline needed to run 100 miles, that is, efficiency = horsepower/(100/mpg).

`@hint`
Assign the values of the new variable by writing the formula to compute the values. Recall that variables must be written following the syntax: mtcars$varname. Thus, your code should start as:
mtcars$efficiency <- mtcars$...

`@pre_exercise_code`
```{r}
data(mtcars)
```

`@sample_code`
```{r}
# get the names of the variables in the dataset:
names(mtcars)
# create a new variable efficiency:
mtcars$efficiency <- 

```

`@solution`
```{r}
mtcars$efficiency <- mtcars$hp/ (100/mtcars$mpg)
mean(mtcars$efficiency, na.rm==TRUE)
```

`@sct`
```{r}

```

---

## MC trial1

```yaml
type: MultipleChoiceExercise
key: 01ea082479
xp: 50
```

In the mtcars dataset, what is the name of the 2nd variable (column 2 in the data.frame)?

`@possible_answers`
- ["cyl"]
- "mpg"
- "weight"
- "speed"

`@hint`
Use the command names(dataset) to get the names:

`@pre_exercise_code`
```{r}
data(mtcars)
```

`@sct`
```{r}
msg1 <- "yes!"
msg2 <- "the correct answer is 'cyl'"
msg3 <- "the correct answer is 'cyl'"
msg4 <- "the correct answer is 'cyl'"
ex() %>% check_mc(1, feedback_msgs = c(msg1, msg2, msg3,msg4))
```
