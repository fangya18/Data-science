## Background Info
In casino, we are interested in the outcome of a dice or a flip of a coin. The study and model to explore the Binary outcomes is Logistic Regression.

#### Application: 
In Clinical Trials we use factors to predict Responder and Non-Responders 

If we let the outcome of probability of success be p (head), then the none success is 1-p ,(tail).

#### Formula:
One predictor 
$$logit[P(x)]=\frac{log(P(x)}{1−P(x))}= ax+b$$ 


Mutliple Predictors:
$$logit[P(x)]=\frac{log(P(xi)}{1−P(xi))}= a1x1+a2x2+a3x3+a4x4+...b$$

When a>0 , then p(x) and the log odds increases as x increase 

when  a<0,  then p(x) and the log odds decrease as x increase


## Arthritis Data Processing
Binary **Response Variable** For Logistic Model: 
**Better** : *Improved, None* 

If the variable Improved is is "Some" or "Marked", we consider the patients' Arthritis symptom is Improved If the variable Improved is "None", we consider the patients Arthritis problem remains.

**Goal**: 
We want to know how the factors affect the outcome of the Arthritis Symptom: **Treatment, Sex, Age **:

**Treatment** (Categorical Data): Treated, Placebo 
**Sex** (categorical Data) : Male, Female 
**Age** (Continuous Data) : 18-85

```{r}
data<- Arthritis

#Treatment
data$better <- as.numeric(data$Improved >"None")
data[35:45, ]
```
##    ID Treatment    Sex Age Improved better
## 35 58   Treated Female  66   Marked      1
## 36 13   Treated Female  67   Marked      1
## 37 61   Treated Female  68     Some      1
## 38 65   Treated Female  68   Marked      1
## 39 11   Treated Female  69     None      0
## 40 56   Treated Female  69     Some      1
## 41 43   Treated Female  70     Some      1
## 42  9   Placebo   Male  37     None      0
## 43 14   Placebo   Male  44     None      0
## 44 73   Placebo   Male  50     None      0
## 45 74   Placebo   Male  51     None      0

## Logistic Regression

### Logistic Regression Model: Age

We want to investigate the relationship between Age and Treatment Outcome variable: Better. 
As the graph and statistical model suggested: when Age gets Older,
Arthritis is harder to cure, and Age is quite significant Factor in the treatment of Arthritis, as p-value=0.011

## Logistic Regression

### Logistic Regression Model: Age

We want to investigate the relationship between Age and Treatment Outcome variable: Better. As the graph and statistical model suggested: when Age gets Older, Arthritis is harder to cure, and Age is quite significant Factor in the treatment of Arthritis, as p-value=0.011

```{r }

#Age
artha.log <-glm(better ~Age, data=data, family=binomial)
artha.log
summary(artha.log)

xyvalues <- seq(15, 85, 5)
(pred.logistic <- predict(artha.log, newdata= data.frame(Age= xyvalues), type="response", se.fit= TRUE))
(upper <- pred.logistic$fit + 1.96 * pred.logistic$se.fit)
(lower <- pred.logistic$fit - 1.96 * pred.logistic$se.fit)


plot(jitter(better, .1) ~ Age, data= data, xlim = c(15,85), pch= 16, ylab= "Probability (Btter)", main="Probability of Arthritis Response respect to Age")
polygon(c(xyvalues, rev(xyvalues)), c(upper, rev(lower)), col= rgb(0, 0, 1, .2), border= NA)
lines(xyvalues, pred.logistic$fit, lwd= 4, col= "pink")
```
## 
## Call:  glm(formula = better ~ Age, family = binomial, data = data)
## 
## Coefficients:
## (Intercept)          Age  
##    -2.64207      0.04925  
## 
## Degrees of Freedom: 83 Total (i.e. Null);  82 Residual
## Null Deviance:       116.4 
## Residual Deviance: 109.2     AIC: 113.2

## 
## Call:
## glm(formula = better ~ Age, family = binomial, data = data)
## 
## Deviance Residuals: 
##      Min        1Q    Median        3Q       Max  
## -1.51065  -1.12772   0.07936   1.06771   1.76109  
## 
## Coefficients:
##             Estimate Std. Error z value Pr(>|z|)  
## (Intercept) -2.64207    1.07317  -2.462   0.0138 *
## Age          0.04925    0.01936   2.544   0.0110 *
## ---
## Signif. codes:  0 '***' 0.001 '**' 0.01 '*' 0.05 '.' 0.1 ' ' 1
## 
## (Dispersion parameter for binomial family taken to be 1)
## 
##     Null deviance: 116.45  on 83  degrees of freedom
## Residual deviance: 109.16  on 82  degrees of freedom
## AIC: 113.16
## 
## Number of Fisher Scoring iterations: 4
