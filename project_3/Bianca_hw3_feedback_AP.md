For all of question 3, it seems you still had used the older numbers for calculating the odds after we figured out how to do the proper crosstab tables. (ie. Q3.1 should've been 33/28 odds)
Q4.6: Students who attended a teir 2 undergraduate school had 0.50 the odds of being admitted to graduate school compared to students who attend a teir 1 undergraduate school.
For section 5, I figured out that the error we were experiencing was when we were recreating the dummy variables, section 5.1 should've looked like this (notice the get_dummies is performed on 'combos' and not the original 'df' that we were doing:
combos.columns = ['gre','gpa','prestige','intercept']
dummy_ranks = pd.get_dummies(combos['prestige'], prefix='prestige')
cols_to_keep = ['gre','gpa','prestige','intercept']
combos = combos[cols_to_keep].join(dummy_ranks.ix[:,'prestige_2':])
combos.head()

After that fix to Q5, the predictions come in line. The interpretation of the predictions:  Given the same GPA and GRE scores, students who attended a tier 4 undergraduate school had a 37% probablity of being admitted into grad school, while student who attended a tier 1 school had a 73% likelihood of being admitted into grad school.
I've sent you back a corrected version of your IPython notebook via slack.