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
