Quick reference for R commands useful for lab assignments in EVE 101.



| To ...        | ...use the command   | more arguments / details  |
| :--------------------- |:-------------:| :-----:|
| set working directory | `setwd("/path/to/working/dir")` | use `getwd()` to see current working directory|
| read in csv   | `read.csv(file.choose())` | or replace `file.choose()` with file name if it's in current working directory |
| create new column that's sum of columns| `d$new.column <- rowSums(d[ , c(2,4,7)])` | each row in `new.column` is sum of value in columns 2, 4, 7|
| plot `y1` vs `x` | `plot(x, y1)` | `type="l"` for line, `lty` for linetype, `col` for color, see `?plot` and `?par` for details |
| plot two columns from a data frame `d` | `plot(d$col1, d$col2)` or `plot(col2 ~ col1, data=d)` | data.frame is what is created by `read.csv`|
| add `y2` vs `x` to already-created plot      | `points(x, y1)`     |   same options as `plot` |



### Plotting multiple lines on the same plot (lab 3)

Tips: 

* plot the data with the greatest range first, using `plot` and the `type="l"` argument to create a line
* to add more data, use `points` and the `type="l"` argument but be sure to use an argument for linetype `lty` or color `col` to differentiate the lines
* using `lines` instead of `points` will save you having to write the type argument out

### Learning more about plots: 

* to understand the basics of plot, including options for the `type` argument, type `?plot` at `R` prompt
* for more information on linetypes and colors, type `?par` at the `R` prompt (there is lots of other information in this help file too)
