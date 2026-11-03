# Run 1
**i-0d37cbb21169a6fee**  
This was the first time I ran it on my own outside of the class. It went well, I made sure I added the correct port number for the security group as it was needed to run the lab and to select a server that had at least 2 GB ram. I even remembered to run the *'/opt/balerica-bank/venv/bin/python3 -m pip install --upgrade pip'* command to upgrade pip. It said it was able to successfully install version 26.0.1 - *'Successfully installed pip-26.0.1'*. It went just like the lab in class, I had no errors or issues. The commands that we ran related to install the COBOL was new to me. As well as the commands to do a lookup, do checks for return codes, echo, posting a payment, and starting the web API were all new to me. I want to look into those more and I know this week we are to use AI for that so I will do that after I have done the initial 3 lab runs. I had no errors or issues. 
**Unique output from code ran - INFO:     Started server process [35932]**

# Run 2
**i-029a5ea34386226bf** 
For the second run, it also went well, no error or issues. The COBOL command remain something new to me and I will explore them later this week. Nothing went differently, it happened as the lab described. 
**Unique output from code ran - INFO:     Started server process [35425]**
# Run 3
**i-09ecab979d471bf27**
For the third run, it also went well, no error or issues. Since this was the last one I ran for that day, I did look at the COBOL commands more to see what it was doing. Read the homework assignment and realize I had to do more with COBOL to modify the data to produce all the error messages. 
**Unique output from code ran - INFO:     Started server process [34982]**
# Run 4
**i-09f2e2b85ce3d4d59**
For the fourth run, I was doing it on a different day. Also had no issues or errors. I payed closer attention to the COBOL code to see what it was doing so I can better understand it. I know COBOL is an older language and is still used as some companies are hesitant to move away from it or mainframes that it resides on. It is kind of crazy how that is as some companies don't know how certain programs/code actually work and don't trust new developers to be able to replicate what they already have. 
**Unique output from code ran - INFO:     Started server process [35551]**
# Run 5
**i-0fa6f812295773c7c**
For the fifth run, it also ran well with no issues or errors. Overall I have gotten faster at creating the instance and doing the lab itself. They keys, security groups, tagging, etc. all seem second nature now. 
**Unique output from code ran - INFO:     Started server process [35068]**
# Run 6
**i-0d3b9b2225135a7d8**
For the sixth run, it also went well with no issues or errors. It ran quickly and I took the needed screenshots and went to watch more of the required videos for the week.
**Unique output from code ran - INFO:     Started server process [35079]**
# Run 7
**i-016dbfab45e1b0b8c**
Seventh and final run! Like the others, it went well with no errors or issues. At this point I knew I had to do more with the COBOL and left it running while I looked more into that. 
**Unique output from code ran - INFO:     Started server process [35336]**
# Mistakes I made
None, I was able to follow the lab successfully each and every time. 
# Commands I now know by heart
*pwd
ls
whoami
mkdir
touch
cat
mv
date
cd

# COBOL Practice
I used **i-016dbfab45e1b0b8c** (lab 7) to do the COBOL requests. 

100001Alice Johnson                 ACTIVE  000000500000USD
100002Robert Smith                  ACTIVE  000000275000USD
100003Maria Garcia                  ACTIVE  000000810000USD

copy/paste the error codes and the 
- For each return code: the command you ran, the **exact** output lines (copy-paste them, including `ERROR=` or `STATUS=` / `REASON=`), and what the code means.
- Decode Alice's balance by hand: what are the raw 12 characters, and what dollar amount do they mean? Why is there no decimal point in the file?
- Run `cat data/payments.dat`. Copy-paste **the journal lines for your own `TXN` IDs**. Then look up account `100001` again. Did the balance change after your payments? Write down what you see and your best guess why.

**Optional:** check if the SQLite command-line tool is installed with `which sqlite3`. If it is, run `sqlite3 data/bank.db ".tables"` and `sqlite3 data/bank.db ".schema"`, and describe what tables the bank keeps.
![[Pasted image 20261101144006.png]]

(venv) [ec2-user@ip-172-31-31-240 balerica-bank]$ cat data/payments.dat
TXN0001             100001000000012550USDPOSTED  INV-1001
TXN-JW-0001         100001000000000000USDREJECTEDTEST-ZERO
TXN-JW-0001         100001001000000000USDREJECTEDTEST-BIGGER
TXN-JW-0001         100001000000000000USDREJECTEDTEST-ZERO
TXN-JW-0001         100001001000000000USDREJECTEDTEST-BIGGER
(venv) [ec2-user@ip-172-31-31-240 balerica-bank]$ 


## 7.4 optional -  describe what tables the bank keeps.

(venv) [ec2-user@ip-172-31-31-240 balerica-bank]$ sqlite3 data/bank.db ".tables"
accounts      transactions
(venv) [ec2-user@ip-172-31-31-240 balerica-bank]$ sqlite3 data/bank.db ".schema"
CREATE TABLE accounts (
    account_id TEXT PRIMARY KEY,
    customer_name TEXT NOT NULL,
    status TEXT NOT NULL,
    balance REAL NOT NULL,
    currency TEXT NOT NULL
);
CREATE TABLE transactions (
    transaction_id TEXT PRIMARY KEY,
    account_id TEXT NOT NULL,
    amount REAL NOT NULL,
    currency TEXT NOT NULL,
    status TEXT NOT NULL,
    reference TEXT,
    created_at DATETIME DEFAULT CURRENT_TIMESTAMP

cd ~
whoami && TZ='Your/Zone' date && ec2-metadata -i && uptime -s
git clone https://github.com/jwalker54-tech/seir-foundations-homework.git
ls seir-foundations-homework/module1

