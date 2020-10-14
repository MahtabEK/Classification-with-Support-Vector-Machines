# Classification-with-Support-Vector-Machines

**The Dataset:** 

This dataset consists of 3921 e-mails to a single account, some of which are spam. These data represent incoming emails for the first three months of 2012 for an email account.  The table has 3921 (1252) observations on the following 21 variables:

- spam: Indicator for whether the email was spam. 
- to_multiple: Indicator for whether the email was addressed to more than one recipient. 
- from: Whether the message was listed as from anyone (this is usually set by default for regular outgoing email). 
- cc: Indicator for whether anyone was CCed. 
- sent_email: Indicator for whether the sender had been sent an email in the last 30 days. 
- time: Time at which email was sent. image: The number of images attached. 
- attach: The number of attached files. 
- dollar: The number of times a dollar sign or the word “dollar” appeared in the email. 
- winner: Indicates whether “winner” appeared in the email. 
- inherit: The number of times “inherit” (or an extension, such as “inheritance”) appeared in the email. 
- viagra: The number of times “viagra” appeared in the email. 
- password: The number of times “password” appeared in the email. 
- num_char: The number of characters in the email, in thousands. 
- line_breaks: The number of line breaks in the email (does not count text wrapping). 
- format: Indicates whether the email was written using HTML (e.g. may have included bolding or active links). 
- re_subj: Whether the subject started with “Re:”, “RE:”, “re:”, or “rE:” 
- exclaim_subj: Whether there was an exclamation point in the subject. 
- urgent_subj: Whether the word “urgent” was in the email subject. 
- exclaim_mess: The number of exclamation points in the email message. 
- number: Factor variable saying whether there was no number, a small number (under 1 million), or a big number. 

The data are from this R package: https://cran.r-project.org/web/packages/openintro/openintro.pdf

**Part 1:**

I read in the email.txt dataset.

**Part 2:**

I split the data into train and test holding out 50% of observations as the test set. I pass random_state=0 to train_test_split to ensure I get the same train and tests sets as the solution.

**Part 3:**

I create a pipeline for the support vector machine. Here, I start with a kernel="linear" and gamma="auto".

**Part 4:**

I use my model to construct a confusion matrix by fitting and predicting on the training data. I calculate the model's training accuracy, precision, and recall using the confusion matrix.

**Part 5:**

I estimate my support vector machine's out of sample recall by using 5 fold cross validation.

**Part 6:**

I used sklearn's GridSearchCV to search over the kernel and gamma. This search is over kernel = ['rbf','sigmoid'] and gamma = np.linspace(1e-5, 1e-2). I used recall as my metric for scoring.

It should be noted that GridSearchCV is a way to cross validate your models for a variety of parameters. You can read more about GridSearchCV at https://scikit-learn.org/stable/modules/generated/sklearn.model_selection.GridSearchCV.html

**Part 7:**

I calculate the cross validated recall for my regularized model by calling my model with best_score_.

**Part 8:**

I access the results of the cross validation by .cv_results_ method. This returns a dictionary that can be turned into a dataframe using pandas.DataFrame.

I also plotted how the mean test error changes as gamma changes. The lines are colored according to kernel. 

Here is a question for you:
What do you see happening to the cross validated error as gamma increases?

You can check out my thoughts on this question in the jupyter notebook provided: "Classification with Support Vector Machines.ipynb"
