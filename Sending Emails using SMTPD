import smtplib
from email.mime.text import MIMEText

def send_email(subject, body, sender, recipient, password):
    msg = MIMEText(body)
    msg['Subject'] = subject
    msg['From'] = sender
    msg['To'] = recipient
    
    gmail = smtplib.SMTP('smtp.gmail.com', 587)
    gmail.ehlo()
    gmail.starttls()
    gmail.login(sender, password)
    gmail.sendmail(sender, recipient, msg.as_string())
    gmail.close()
    print("Email has been sent!!")
    
sender = input("What is your gmail address?" ).split()
password = input("What is your gmail app password? ")
recipient = input("What is the recipient's gmail address? ").split()
subject = input("What would you like the subject to be? ")
body = input("What will be in the body of the email? ")

send_email(subject, body, sender[0], recipient[0], password)
