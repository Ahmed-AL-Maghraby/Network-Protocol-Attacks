
## What's The Telnet ?
Telnet is a protocol used for interactive communication between two devices over a network ( Remote Login )

| Name  | OSI Layer | Port | Attack  |
| ---   | ---       | ---  | ---     |
| Telnet | Application  | 23 TCP     |  - Password sniffing <br> - Brute force attacks <br> - MitM <br> - DOS   |

<BR>

## Several Common Attacks 

1. Password sniffing: Since TELNET sends all communication in plain text, an attacker can easily sniff network traffic and capture usernames and passwords.

2. Brute force attacks: Attackers can attempt to guess usernames and passwords by using automated tools to try a large number of possible combinations.

3. Man-in-the-middle (MitM) attacks: An attacker can intercept and modify TELNET traffic between a client and server, allowing them to steal data, inject malicious code, or hijack the session.

4. Denial-of-service (DoS) attacks: Attackers can flood a TELNET server with a large number of connection requests, overwhelming the server and causing it to crash or become unavailable.


<BR>
  

## wireshark filters

| Filter  | Description |
| -------- | --- |
| telnet    |    This filter will display all packets that contain TELNET traffic  |
| telnet .password   |    This filter will display packets that contain TELNET traffic and also contain a password  |
| telnet .username   |    This filter will display packets that contain TELNET traffic and also contain a username  |
| telnet .data   |    This filter will display packets that contain TELNET traffic and also contain data (commands, responses, etc.) sent over the TELNET session  |
| telnet .port   |    This filter will display packets that are sent or received on the TELNET port (port 23 by default  |
tcp.port == 23   |    This filter will display all packets that are sent or received on the TELNET port  |
| telnet .option   |    This filter will display packets that contain TELNET options, which are used to negotiate settings such as terminal type, window size, and character encoding  |
| telnet .escape   |    This filter will display packets that contain TELNET escape sequences, which are used to send special commands such as interrupt or abort  |
| telnet .command   |    This filter will display packets that contain TELNET commands, which are the actual commands being sent to the remote system (such as ls, cd, or dir)  |
| telnet .response   |    This filter will display packets that contain TELNET responses, which are the output generated by the remote system in response to the TELNET commands  |
| telnet .naws   |    This filter will display packets that contain TELNET NAWS (Negotiate About Window Size) options, which are used to negotiate the size of the terminal window  |
| telnet .status   |    This filter will display packets that contain TELNET status messages, which can include notifications about changes in terminal settings, errors, or other events  |
| telnet .control   |    This filter will display packets that contain TELNET control characters, which are used to perform actions such as moving the cursor, erasing characters, or scrolling the terminal window  |
| telnet .timing   |    This filter will display packets that contain TELNET timing marks, which are used to measure the time it takes for commands and responses to be sent and received  |
| telnet .eof   |    This filter will display packets that contain TELNET end  |   of  |   file (EOF) markers, which indicate the end of a TELNET session or file.


 <BR>

## Protocol on Wireshark
  
<img src="https://raw.githubusercontent.com/ahmed-kamal-el-maghraby/Images/main/TEL1.PNG" height="300" >
<img src="https://raw.githubusercontent.com/ahmed-kamal-el-maghraby/Images/main/tel3.png" height="300" >

  
<BR>

## Event ID
  
+ 592  :  (a new process has been created) where the image base filename is tlntsess.exe
+ 528  : successful logon <BR>
User Name in event ID 528 identifies who logged on using the Telnet service
  
 <BR>