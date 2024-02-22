___________________________________________________________________________________________________________________________________________________________________
___________________________________________________________________________________________________________________________________________________________________
___________________________________________________________________________________________________________________________________________________________________
# caseState_SQL

___________________________________________________________________________________________________________________________________________________________________
GENERAL DESCRIPTION:
This is an SQL script that imports data, and uses case statements to report specific metrics.

___________________________________________________________________________________________________________________________________________________________________
DATA DESCRIPTION:
In this example, the demographic data being used has been generated from the online source https://generate-random.org/person-identity-generator. 

An example schema of each persons information is given below: 
Gender 	female
Title 	Miss
First name 	Idella
Last name 	Willms
Birth date 	1948-01-21
Social security number 	307-86-4743
Street address 	471 Nick Forest
Secondary address 	Apt. 759
Post code 	58594
City 	Nikolauschester
State 	Washington
Latitude 	11.955515
Longitude 	123.721276
Phone number 	+1 (979) 422-6955
Email 	emilia.dooley@baumbach.com
Credit card type 	Visa
Credit card number 	4485-2232-9776-4924
Credit card expiration date 	10/26
Iban 	GI73MULAV2Z48XR687F758A
Bank account number 	31448996
Swift bic number 	ZLVCILTT
Company 	Hoeger Group
Job title 	Brake Machine Setter 



___________________________________________________________________________________________________________________________________________________________________
CODE DESCRIPTION:
This SQL code (caseState.sql) imports the data (people_data.csv), and uses case statements to calculate the percentage of patients who are in a particular generation bin (e.g. Baby Boomers, Millennials, etc.) based on the following age brackets:

    Greatest Generation (1901-1924) ...
    Silent Generation (1925-1945) ...
    Baby Boomers (1946-1964) ...
    Generation X (1965-1980) ...
    Millennials (1981-1996) ...
    Generation Z (1997-2012) ...
    Generation Alpha (2013-2025)

___________________________________________________________________________________________________________________________________________________________________
RUNNING THE CODE:
1) Download the data (people_data.csv) and the SQL script (caseState_JWK.sql)

2) In a terminal, cd into the directory that now contains the data and the script

3) In caseState.sql, change the file path on line 56 from "/home/jwkern/Downloads/" to point to your local directory containing people_data.csv

4) Run the script by typing the following into the command line:

            mysql --local-infile=1 -u username -p password < caseState_JWK.sql

(P.S. don't forget to change the username and password to your mySQL credentials)

4.1) If you wish to save the output in a .txt file, instead run the script as:
      
            mysql --local-infile=1 -u username -p password < caseState_JWK.sql > output.txt


___________________________________________________________________________________________________________________________________________________________________
___________________________________________________________________________________________________________________________________________________________________
___________________________________________________________________________________________________________________________________________________________________
