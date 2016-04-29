## Statistics

Statistics is what separates analysts* *from data managers. But statistics doesn’t need to be scary, and you don’t need a PhD to succeed in this industry. Below, I go over a few basic categories of statistical skills: inferential statistics, predictive modeling, and experimentation. 

Different organizations will have different requirements for core skills, and you should feel comfortable asking organizations what type of statistics are most useful for them. If the organization specializes in modeling, then you brush up on that, etc. As a junior analyst, you only *need *to understand inferential statistics, probably.

### Inferential Statistics

This is the type of statistics that you should know from your basic Stats 101 class:

* Mean, Median, Mode, Standard Deviation

* How to use T-Tests

* Linear Regression (Ordinary Least Squares)

* Logistic Regression

* Interaction Terms

Resources:

* [Khan Academy](https://www.khanacademy.org/math/probability)

* [Statistics One from Princeton](https://www.coursera.org/course/stats1)

### (Predictive) Modeling

Predictive modeling is something that most social science or even statistics students will never work with. Usually, social scientists and other researchers use modeling for *inference*, i.e., trying to tease out substantive relationships between two or more variables. However, we can also use modeling for *prediction*. 

When you’re trying to build a good predictive model, you don’t care about things like coefficient interpretation. Your goal is to try to predict outcomes, and your model is evaluated by how well it predicts those outcomes through a number of different metrics. Your job is to pick the right metric and see if you can generate the right **features** (also known as covariates, independent variables, or x variables) to make those types of predictions. The actual value of the coefficients is meaningless. 

If you want to have a job that involves building models, here are some basic concepts that you should know. These concepts *aren’t *required for everyone who wants to work in analytics, and a lot of this will be learned on the job. But if you want to focus on modeling in particular, this is the stuff you should know. Especially at the junior levels, you won’t need to understand the statistical theory or proofs behind this stuff, but you should know how to with apply them (perhaps with a lot of Googling):

* *k-*fold* *cross-validation and why it’s superior to hold-out sets

* Regularization (especially LASSO and Ridge regression) and why it’s useful

* Know how to apply some standard machine learning algorithms: gradient boosting, random forest, LASSO/ridge/elastic net.

* Accuracy metrics: root mean squared error, AUCROC, precision, recall

Resources:

* [Statistical Learning](http://online.stanford.edu/course/statistical-learning-winter-2014)

* [Elements of Statistical Learning](http://statweb.stanford.edu/~tibs/ElemStatLearn/)

### Experimentation

Experimentation is often the only way to answer the questions we care about most. Any time that you have a question along the lines of "What is the *impact* or *effect *of X on Y?", that question ought to be answered with an experiment. In some cases, it won’t be possible to answer it with an experiment, but in most cases, it will be answered by something that’s not an experiment is therefore likely to be wrong.

For example, we might want to know the impact of getting canvassed--when someone knocks on your door---on voter turnout. You might be tempted to just let a campaign conduct its normal canvassing program and compare people who were successfully **treated** and those who weren’t. But people who were reached might be different than others who weren’t in ways *other *than just getting canvassed: for example, they might be older (so they’re more likely to be home), or they’re friendlier. These qualities (age, personality, etc.) can impact the outcome we’re trying to measure (e.g., turnout), so we don’t know if the difference between the two groups is due to differences in age/personality or because of the canvass itself. When you **randomly** assign people to get canvassed or not, by contrast, you can ensure that the only difference between the groups is the treatment itself. 

If you understand the paragraph above, you probably know enough about experiments for most jobs. But if your role will focus on experimentation, you’ll want a more sophisticated methodological understanding:

* A/B Testing

* Intent to Treat versus Treatment on Treated

* Average Treatment Effect

* Differential Attrition

Resources:

* [Introduction to Program Evaluation by J-PAL](http://www.povertyactionlab.org/methodology/what-randomization)

* *[Field Experiments: Design, Analysis, and Interpretation](http://www.amazon.com/Field-Experiments-Design-Analysis-Interpretation/dp/0393979954)* by Don Green and Alan Gerber