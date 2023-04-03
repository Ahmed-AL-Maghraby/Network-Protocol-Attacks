
## What's The FTP ?
FTP stands for File Transfer Protocol. It is a standard network protocol used for transferring files from one host to another over a TCP/IP-based network, such as the internet.

<br>

| Name  | OSI Layer | Port | Attack  |
| ---   | ---       | ---  | ---     |
|   FTP | Application | 20,21 |  - Brute force attacks <br> -  FTP bounce attacks <br> -  Port stealing attacks <br> - Malware attacks <br> - DOS    |



<BR>

## Several Common Attacks

1. Brute force attacks: Attackers use automated tools to repeatedly try different username/password combinations until they are able to guess the correct credentials and gain access to the FTP server.

2. FTP bounce attacks: Attackers exploit a vulnerability in the FTP server to use it as a proxy to attack other systems on the network.

3. Port stealing attacks: Attackers attempt to hijack the control port used by the FTP server to communicate with clients, in order to intercept and modify data being transferred.

4. Malware attacks: Attackers can use malware such as trojans or keyloggers to steal login credentials, intercept data, or compromise the FTP server itself.

5. Denial of Service (DoS) attacks: Attackers flood the FTP server with a large volume of traffic or requests, causing it to become overwhelmed and unable to respond to legitimate requests.

<BR>

## FTP status codes

| Code | Description |
| --- | --- |
| 100  |  The requested action is being initiated, expect another reply before proceeding with a new command |
| 200  |  The requested action has been successfully completed |
| 300  |  The command has been accepted, but the requested action requires further information or confirmation |
| 400  |  The command was not accepted and the requested action did not take place |
| 500  |  Syntax error or command unrecognized. The command could not be executed because the syntax is incorrect or the command is not recognized by the server |
| 550  |  The requested action could not be completed because the server encountered an error or the file does not exist |
| 331  |  User name OK, password required |
| 530  |  Not logged in. The user name and/or password is not valid |
| 125  |  Data connection already open; transfer starting |
| 150  |  File status okay; about to open data connection |
| 226  |  Closing data connection. Requested file action successful |
| 250  |  Requested file action okay, completed |
| 421  |  Service not available, closing control connection. This may be a reply to any command if the service knows it must shut down |
| 426  |  Connection closed; transfer aborted |
| 450  |  Requested file action not taken. File unavailable (e.g., file busy  |
| 530  |  Not logged in. The user name and/or password is not valid |
| 550  |  Requested action not taken. File unavailable (e.g., file not found, no access  |

<br>

## wireshark filters

| Filter | Description |
| ------ | ------ |
| ftp  |    This filter displays only FTP packets |
| ftp.request.command  |    This filter displays only FTP request packets and filters them based on the command used, such as RETR (retrieve a file), STOR (store a file), LIST (list files in a directory), etc |
| ftp.response  |    This filter displays only FTP response packets |
| ftp.request.arg  |    This filter displays FTP request packets and filters them based on the argument passed, such as the filename or directory path |
| ftp-data  |    This filter displays only FTP data packets |
| ftp-data.command  |    This filter displays only FTP data packets and filters them based on the command used, such as STOR (store a file) or RETR (retrieve a file) |
| ftp-data.port  |    This filter displays FTP data packets and filters them based on the port number used for the data transfer |
| ftp.request.arg.raw  |    This filter displays FTP request packets and filters them based on the raw argument passed, without decoding any special characters or formatting |
| ftp.request.command == "USER" or | ftp.request.command == "PASS"  |    This filter displays only FTP request packets that contain the USER or PASS command, which are used for authentication |
| ftp.request.command == "SYST"  |    This filter displays only FTP request packets that contain the SYST command, which is used to determine the remote system type |
| ftp.request.command == "FEAT"  |    This filter displays only FTP request packets that contain the FEAT command, which is used to request a list of features supported by the server |
| ftp.request.command == "ABOR"  |    This filter displays only FTP request packets that contain the ABOR command, which is used to abort a previous command or data transfer.


<BR>

## Protocol on Wireshark

<img src="" height="300" >
<img src="" height="300" >
<img src="" height="300" >
<img src="" height="300" >

<BR>

## Event ID


+ 3: This event ID indicates that a user has successfully logged on to an FTP server
+ 4: This event ID indicates that a user has logged off from an FTP server 
+ 5: This event ID indicates that an FTP session has been terminated due to an error or abnormal termination
+ 6: This event ID indicates that a user has uploaded a file to an FTP server 
+ 7: This event ID indicates that a user has downloaded a file from an FTP server 
+ 8: This event ID indicates that an FTP command has been executed by a user 

<br>




