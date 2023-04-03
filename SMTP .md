
## What's The SMTP ?

SMTP stands for Simple Mail Transfer Protocol. It is a protocol used for sending email messages between servers and email clients over the Internet.


<br>

| Name  | OSI Layer | Port | Attack  |
| ---   | ---       | ---  | ---     |
|   SMTP    |   Application  |   25,587,465 tcp   |     Spoofing    |



<BR>

## Several Common Attacks

1. Phishing: Phishing attacks involve sending fraudulent emails that appear to be from a legitimate source in order to trick recipients into revealing sensitive information or clicking on malicious links.

2. Spoofing: Spoofing attacks involve sending emails with forged headers that appear to come from a trusted source, such as a legitimate organization or government agency. These emails may contain malicious attachments or links.

3. Spamming: Spamming involves sending unsolicited emails to a large number of recipients. These emails may contain fraudulent or malicious content, and can be used to distribute malware or launch phishing attacks.

4. Email bombing: Email bombing is a type of denial-of-service attack that involves sending a large number of emails to a single recipient or mail server in order to overwhelm the system and cause it to crash or become unavailable.

5. Email address harvesting: Email address harvesting involves collecting email addresses from public sources such as websites or social media platforms, with the intent of using them for spamming or other malicious activities.



<BR>

## wireshark filters

| Filter | Description |
| ------ | ------ |
| tcp.port == 25  |    This filter displays only the traffic on port 25, which is used by SMTP for email transmission |
| smtp. This filter displays all SMTP traffic, including the initial handshake, commands, responses, and data |
| smtp.command  |    This filter displays only the SMTP commands being sent by the client |
| smtp.response  |    This filter displays only the SMTP responses being sent by the server |
| smtp.contains "keyword"  |    This filter displays SMTP traffic that contains the specified keyword. For example, | smtp.contains "username" would display traffic that includes the word "username" |
| smtp.to or | smtp.from  |    This filter displays only SMTP traffic that includes either the "To" or "From" fields in the email header |
| smtp.command_code == "DATA"  |    This filter displays only SMTP traffic that includes the DATA command, which is used to transmit the email message body |
| smtp.rcpt_to  |    This filter displays SMTP traffic that includes the "RCPT TO" command, which is used to specify the email recipient(s) |
| smtp.quit  |    This filter displays SMTP traffic that includes the QUIT command, which is used to terminate the SMTP session |
| smtp.content_type contains "multipart"  |    This filter displays SMTP traffic that includes email messages with a multipart content type, which typically includes attachments |
| smtp.date  |    This filter displays SMTP traffic that includes the email message date, which can be helpful for troubleshooting message delivery issues |
| smtp.flags.push == 1  |    This filter displays SMTP traffic that has the PUSH flag set, which indicates that the sender is requesting immediate delivery of the data |
| smtp.resp_code == 550  |    This filter displays SMTP traffic that includes a response code of 550, which indicates that the email was rejected by the server |
| smtp.helo  |    This filter displays SMTP traffic that includes the HELO/EHLO command, which is used to identify the client to the server |
| smtp.auth  |    This filter displays SMTP traffic that includes authentication commands, such as LOGIN or PLAIN, used to authenticate the sender |
| smtp.rcpt_to.count == 1  |    This filter displays SMTP traffic that includes only one recipient in the email message |
| smtp.data_len >= 5000  |    This filter displays SMTP traffic that includes email messages with a data length greater than or equal to 5000 bytes |
| smtp.contains "Subject"  |    This filter displays SMTP traffic that includes the email subject line |

<BR>

## Protocol on Wireshark

  <img src="https://github.com/ahmed-kamal-el-maghraby/Images/blob/main/smtp1.PNG" height="400" >
  <img src="https://github.com/ahmed-kamal-el-maghraby/Images/blob/main/smtp2.PNG" height="400" >
  <img src="https://github.com/ahmed-kamal-el-maghraby/Images/blob/main/smtp3.PNG" height="400" >
  <img src="https://github.com/ahmed-kamal-el-maghraby/Images/blob/main/smtp4.PNG" height="400" >
  <img src="https://github.com/ahmed-kamal-el-maghraby/Images/blob/main/smtp5.PNG" height="400" >
  <img src="https://github.com/ahmed-kamal-el-maghraby/Images/blob/main/smtp6.PNG" height="400" >
  <img src="https://github.com/ahmed-kamal-el-maghraby/Images/blob/main/smtp7.PNG" height="400" >
  <img src="https://github.com/ahmed-kamal-el-maghraby/Images/blob/main/smtp8.PNG" height="400" >
  <img src="https://github.com/ahmed-kamal-el-maghraby/Images/blob/main/smtp9.PNG" height="400" >



<BR>

## Event ID

+ 1000: Indicates that the SMTP service has started successfully.
+ 12014: Indicates that there is a problem with the Transport Layer Security (TLS) certificate configured on the SMTP receive connector.
+ 15004: Indicates that there is an issue with the mailbox database or storage group, preventing the SMTP service from delivering email messages.
+ 4000: Indicates that an SMTP message has been queued for delivery.
+ 5016: Indicates that the SMTP service has accepted a message for delivery.


<br>


