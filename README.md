
# Customer Purchasing Behavior Analysis 

This assignment is two parts-

   1) Analyse and conclude your observations based on the dataset - Customer Purchasing Behaviors 

   2) Create an automated email sending service with documents attached (Analysis file and Readme file)  


   


## Assignment 1

 
 #### Customer Purchasing Behavior Analysis

 Based on the dataset provided, I bifurcated users based on age groups to study the following patterns - 

  
  1)  Purchase frequency of the different age groups
  
  2)  Total purchase of the different age groups 
  
  3)  Average Order Value of the different age groups
  
  4)  Total purchase of the different age groups Bifurcated by regions - NORTH, SOUTH, EAST AND WEST
  
  5)  Average Order Value of the different age groups Bifurcated by regions - NORTH, SOUTH, EAST AND WEST


 ### Insights Generated

   1) Based on the boxplot of purchase frequency based on age group, we can conclude that, the age group of (50 - 55) is particularly interesting - with the highest purchase frequency and sizeable population as customers fall in that category
        
        Reasons may be -
       
        a) More purchasing power
        b) More health concious

![image](https://github.com/user-attachments/assets/6d7902f6-1827-4c67-ba3f-d1a399649d35)


2) Based on the bar chart of purchase frequency based on age group, we can conclude that, the age group of (50 - 55) has an average order value of 608 approx which is much higher than dataset total average of 425

    ![image](https://github.com/user-attachments/assets/3ecbd53f-53cd-4a13-8880-53588c788e3c)

![image](https://github.com/user-attachments/assets/4045e345-4445-43d4-83f2-050bb1be6d6f)


3) The 3rd chart, in addition to the age group of (50 - 55), also shows -
    
    (40 -45) age group is very lucrative as well as it is the 3rd highest population and has above average order value and purchase rate
   
    ![image](https://github.com/user-attachments/assets/68b4a0b7-0fd5-4655-9630-a63f9da027b7)

5)  The regionwise split of average order value gives many important observations-
    
    a) East zone customers are not targeted enough or the marketing spent has been inefficient in this region to attract the most lucrative age groups
    
    b) The purchase frequency distribution shows that the majority of 50-55 age group purchases are from the west zone 
    
    c) 40-45 age group purchases - majority are from South region

![image](https://github.com/user-attachments/assets/5fa32561-72e9-439a-8744-4e75ae0616e5)

![image](https://github.com/user-attachments/assets/d42f2911-89c3-49d4-9f97-0ad72eb61347)


### Recommendations

1) Increase marketing ad spent on the (40-45) and (50-55) age groups. 
2) Root cause analysis of low East zone participation has to be performed
3) Also check if the South zone marketing spent are tailored to the above recommendations as 50-55 age group participation is low





# EMAIL SENDING USING PYTHON ASSIGNMENT

## Flow of the Program:

#### Create Email Message:

A MIMEMultipart() object is created to hold the email's components.
MIMEText() is used to attach a plain text body.
#### Attach Files:

Each file is opened in binary mode, read, encoded using encoders.encode_base64(), and attached to the email with msg.attach().

#### Send Email:

The script connects to Gmail's SMTP server via smtplib.SMTP(), starts TLS encryption (starttls()), logs in with the sender’s credentials, and sends the email using sendmail().
By using these packages and functions, the script efficiently handles email composition and file attachments, and sends the email securely through Gmail's SMTP server

### Packages Used

#### 1) smtplib:

Purpose: This is a built-in Python library that defines an SMTP client session object. It can be used to send emails to any internet machine with an SMTP or ESMTP listener daemon.

Key Functionality:

a) smtplib.SMTP: Creates an SMTP client connection to a specified SMTP server (in this case, Gmail).

b) server.starttls(): Upgrades the SMTP connection to a secure, encrypted TLS connection.

c) server.login(sender_email, password): Logs into the email server with the sender's credentials.

d) server.sendmail(sender_email, receiver_emails, msg.as_string()): Sends the email to the recipients.

e) server.quit(): Closes the connection to the SMTP server.

### 2) email.mime.multipart.MIMEMultipart:
Purpose: 
This class is used to create a MIME (Multipurpose Internet Mail Extensions) message object that can include different parts like the email body and attachments.

Key Functionality:
MIMEMultipart(): Creates a new message container for combining the email body and attachments.

#### 3) email.mime.text.MIMEText:

Purpose: It is used to represent the plain text body of the email.
Key Functionality:
MIMEText(body, 'plain'): Creates a text/plain MIME object, which is added to the email body.
#### 4) email.mime.base.MIMEBase:

Purpose: This class is used for handling binary file attachments in an email. It represents the base MIME type for binary data.

Key Functionality:
MIMEBase('application', 'octet-stream'): Initializes the binary part for the file attachment, specifying that it contains arbitrary binary data (i.e., it could be any kind of file).

#### 5) email.encoders:

Purpose: Encoders are used to encode the file attachment data into a format suitable for sending via email, typically base64 encoding.
Key Functionality:
encoders.encode_base64(part): Encodes the binary data (the attachment) into base64 so it can be safely transmitted over the internet.

#### 6) os :

Purpose: This built-in module provides a way of using operating system-dependent functionality like handling file paths, managing directories, etc.

Key Functionality:
os.path functions can be used to manipulate file paths and check if files exist, though not used directly in this particular code.

### Functions and Key Concepts
#### 1) MIMEMultipart():

Creates a container for the email message that can hold different parts like the body text and attachments.

#### 2) MIMEText():

Adds the body of the email in plain text.

#### 3) MIMEBase():

Prepares the attachment in binary format before encoding it.

#### 4) encoders.encode_base64():

Encodes the attachment to base64 so that binary data can be safely transmitted over the email.

#### 5) msg.attach():

Attaches the different parts to the email message. This is used to attach both the text body and the files to the email.

#### 6) smtplib.SMTP():

Initializes a connection to the Gmail SMTP server, allowing you to send emails.

#### 7) starttls():

Starts TLS encryption, securing the connection to the email server.

#### 8) login():

Authenticates the sender’s email with the SMTP server using the provided credentials.
#### 9) sendmail():

Sends the email with all recipients, the sender, and the content (including attachments).
#### 10) quit():

Terminates the connection to the SMTP server, cleaning up resources.



