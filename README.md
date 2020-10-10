# Bayesian Latent Variable Model on Abalone Data
## Introduction
I am [Benjamin Chan](http://www.linkedin.com/in/benjamin-chan-chun-ho). This is my project under taking a course at [Department of Statistics](http://www.sta.cuhk.edu.hk/home.aspx) of [The Chinese University of Hong Kong](http://www.cuhk.edu.hk/english/index.html). I take the initiative to pick both data and techniques to demonstrate thorough understanding of course materials.

[Abalone](https://archive.ics.uci.edu/ml/datasets/Abalone) is the 10th most popular data in [UCI Machine Learning Repository](https://archive.ics.uci.edu/ml/index.php). The biological method for determining age of abalone is time-consuming. There is a need to predict the age from physical measurements that can be easily obtained. `Structural Equation Model (SEM)` can be used to group highly correlated variables into latent variables and assess interrelationship among latent variables.

Bayesian SEM is applied to Abalone data. Specifically, the linear SEM with `multisample data` is adopted. The R package R2WinBUGS is used to call `WinBUGS` to do the `Bayesian analysis`.

## Project Summary
* Built linear SEM for multisample data, i.e. male, female and infant abalones
* Formulated a `measurement equation` to relate observed variables to latent variables
* Combined length, diameter and height into a latent variable called size
* Combined whole/shucked/viscera/shell weight into a latent variable called weight
* Constructed a `structural equation` to regress age on explanatory latent variables
* Used WinBUGS to do Bayesian simulation by `Markov Chain Monte Carlo (MCMC)` algorithms
* Achieved convergence in simulation by inspecting running mean plots of parameters
* Gave intuitive interpretation of results:
    * Size is more related to length than diameter and height 
    * Weight is more related to whole weight than other weights
* Inferred that size is useful for predicting age of all abalones but weight is useful for infant only
* Incorporated the observation that male is on average smaller than female but larger than infant

## Reference
### STAT5020 Topics in Multivariate Analysis
#### 17-18 Term 2, Course Instructor: [Prof. Xinyuan Song](http://www.sta.cuhk.edu.hk/xysong/default.aspx)
This is an advanced course on multivariate analysis. Topics may include: Multivariate central theorem, and its applications, factor analysis, structural equation models, and latent variable models.
