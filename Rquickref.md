Quick reference for R commands useful for lab assignments in EVE 101.



| To ...        | ...use the command   | more arguments / details  |
| :--------------------- |:-------------:| :-----:|
| set working directory | `setwd("/path/to/working/dir")` | use `getwd()` to see current working directory|
| read in csv   | `read.csv(file.choose())` | or replace `file.choose()` with file name if it's in current working directory |
| create new column that's sum of columns| `d$new.column <- rowSums(d[ , c(2,4,7)])` | each row in `new.column` is sum of value in columns 2, 4, 7|
| plot two columns from a data frame `d` | `plot(d$col1, d$col2)` or `plot(col2 ~ col1, data=d)` | data.frame is what is created by `read.csv`|
| plot `y1` vs `x` | `plot(x, y1)` | `type="l"` for line, `lty` for linetype, `col` for color, see `?plot` and `?par` for details |
| add points or lines `col2` vs `col1` from data.frame d to already-created plot      | `points(col2 ~ col1)` or `lines(col2 ~ col1)`    |   same options as `plot` |
| add points or lines `y2` vs `x` to already-created plot      | `points(x, y1)` or `lines(x, y1)`    |   same options as `plot` |
| store linear regression of column `y` on `x` from data `d` in `my.lm`      | `my.lm <- lm(y ~ x, d)`     |   ... |
| summarize `my.lm` including coefficients, standard errors, `R^2`      | `summary(my.lm)`     |  see function `coef` to extract just the coefficients |
| add line of best fit from  `my.lm` to existing graph      | `abline(my.lm)`     |  ... |


### Plotting multiple lines on the same plot (lab 3)

Tips: 

* plot the data with the greatest range first, using `plot` and the `type="l"` argument to create a line (or as in example code, use `ylim(y_min, y_max)` to specify the range)
* to add more data, use `lines` but be sure to use an argument for linetype `lty` or color `col` to differentiate the lines

### Using `lm` and `summary` (lab 4)

* fit a model with `lm` and store it in a variable, say `my.lm`
* use `summary(my.lm)` to view coefficients and statistics


### Learning more about commands: 

* *plot*: to understand the basics of plot, including options for the `type` argument, type `?plot` at `R` prompt
* *plot* *lines* and *points*: for more information on linetypes and colors, type `?par` at the `R` prompt (there is lots of other information in this help file too)
