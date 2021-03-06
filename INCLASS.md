

## In-class assigments


### In-class 1

Enter the following data into excel or R


| ID | X | Y |
|-----|----|----|
|1 |	4.55	| 4.99 |
|2	| 4.95 |	5.65 |
| 3	| 4.64 |	5.50 |
| 4 |	4.97	| 5.10 |
| 5	| 4.00 |	4.51 |
| 6	| 4.47	| 5.13 |
| 7	| 4.87 |	5.27 |
| 8	| 4.38	| 4.53 |
| 9	| 4.87	| 5.39 |
| 10 | 4.59 |	5.08 |

Produce a excel file or an R-script that computes the mean and variance of each variable and the covariance between the two.

Use only sums, differences, products and power functions (i.e., do not use the excel functions `average()`, `correl()`, etc. or the R-functions `mean()`, `var()`, `cov()` )

Turn your assigment into D2L

**Proposed solution**

```r
X=c(4.55, 4.95, 4.64, 4.97, 4, 4.47, 4.87, 4.38, 4.87, 4.59)

Y=c(4.99, 5.65, 5.5, 5.1, 4.51, 5.13, 5.27, 4.53, 5.39, 5.08)

mX=mean(X)
mY=mean(Y)
dX=X-mX
dY=Y-mY
dXdY=dX*dY
sum(dXdY)/(length(X)-1)

cov(X,Y)

```

### In-class 2

Using the following data:

```r
 set.seed(195021)
 n=50
 x=runif(n)
 y=x+rnorm(n)/8
 cor(x,y)
```

1) Use `cor.test` to compute the p-value for H0: r>0 Vs Ha: r<=0
2) Compute the same p-value using `pt` (Hint: see code available in Github, in [CORRELATION.md](https://github.com/gdlc/EPI809/blob/master/CORRELATION.md)


### In-class 3

Using Galton's data set compute and report:
  - Correlation between offspring height and mid-parental hight (report point estimate, p-value and 95% CI)
  - The estimated intercept and slope from the regression of offsping height on mid-parental height (use the `lm()` R-function).
  - Summarize your conclusions in no more than 2 sentences.
