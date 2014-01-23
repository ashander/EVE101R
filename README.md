EVE101R
=======

Quick reference for R commands useful for lab assignments in EVE 101.



| To ...        | ...use the command   | more arguments / details  |
| :--------------------- |:-------------:| :-----:|
| set working directory | `setwd("/path/to/working/dir")` | use `getwd()` to see current working directory|
| read in csv   | `read.csv(file.choose())` | or replace `file.choose()` with file name if it's in current working directory |
| create new column that's sum of columns| `d$new.column <- rowSums(d[ , c(2,4,7)])` | each row in `new.column` is sum of value in columns 2, 4, 7|
| plot `y1` vs `x` | `plot(x, y1)` | `type="l"` for line, `lty` for linetype, `col` for color, see `?plot` and `?par` for details |
| add `y2` vs `x` to already-created plot      | `points(x, y1)`     |   same options as `plot` |
