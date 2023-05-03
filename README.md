Download Link: https://assignmentchef.com/product/solved-cs3700-homework1-a-client-and-a-server-programs
<br>
<strong>Part I: Write a client program and a server program to implement the following protocol on top of UDP. </strong>

<ul>

 <li><strong>Client Program</strong>:

  <ol>

   <li>Display a message to ask the User to input the DNS or IP of the machine on which the Server Program runs.</li>

   <li>Display the following table on the standard output:</li>

  </ol></li>

</ul>

Item ID                  Item Description

00001                     New Inspiron 15

00002                     New Inspiron 17

00003                     New Inspiron 15R

00004                     New Inspiron 15z Ultrabook

00005                     XPS 14 Ultrabook

00006                     New XPS 12 UltrabookXPS

<ol start="3">

 <li>Display a message on the standard output to ask the User to input an Item ID, and validate the user input. If the input is not a valid Item ID, ask the User to re-type it.</li>

 <li>Once getting a valid item ID from the User, send a request including this Item ID (e.g., 00005 or “00005”) to the Server program to ask for a quote, and record the local time right before sending such request.</li>

 <li>Receive and interpret the response from the Server program, get the local time right after such response is received, and display the following information on the standard output, (e.g., if 00005 were provided by the User earlier on)</li>

</ol>

Item ID                  Item Description                  Unit Price              Inventory               RTT of Query

00005                     XPS 14 Ultrabook               $999.99                 261                         … ms where “RTT of Query” is the difference between the time in Steps 5 and 4 in millisecond.

<ol start="6">

 <li>Display a message on the standard output to ask the User whether to continue. If yes, repeat steps 2 through 5. Otherwise, close the socket and terminate the Client program.</li>

</ol>

<ul>

 <li><strong>Server Program</strong>:

  <ol>

   <li>Maintain the following information using an appropriate data structure of your choice (i.e., an array of a Class you defined).</li>

  </ol></li>

</ul>

You do not have to place it in a file although you certainly can if you like.

<strong>Item ID                 Item Description                                Unit Price            Inventory </strong>

00001                     New Inspiron 15                                  $379.99                 157

00002                     New Inspiron 17                                  $449.99                 128

00003                     New Inspiron 15R                               $549.99                 202

00004                     New Inspiron 15z Ultrabook             $749.99                 315

00005                     XPS 14 Ultrabook                               $999.99                 261

00006                     New XPS 12 UltrabookXPS             $1199.99               178

<ol start="2">

 <li>Wait for receiving a packet from a Client.</li>

 <li>Once a packet is received from a Client, retrieve the information relevant to the requested Item ID from the data structure you used in Step 1 and send back such information to the Client.</li>

 <li>Repeat Steps 2 and 3 infinitely until an exception is caught.</li>

 <li>Close the datagram socket.</li>

</ol>

<strong>Part II : Test your programs on the Virtual Servers in the cloud and your laptop/home computer. </strong>

<strong>Warning</strong>: to complete this part, especially when you work at home, you must first (1) <strong>connect to GlobalProtect </strong>using your NetID account (please read “<strong>how to connect to GlobalProtect …</strong>” at <u>https://msudenver.edu/vpn/</u>); then (2) <strong>connect to the virtual servers cs3700a and cs3700b</strong> using <strong><em>sftp</em></strong> and <strong><em>ssh</em></strong> command on MAC/Linux or <strong><em>PUTTY</em></strong> and <strong><em>PSFTP</em></strong> on Windows.

<table width="720">

 <tbody>

  <tr>

   <td colspan="2" width="720">ITS only supports GlobalProtect on MAC and Windows machines.  If your home computer has a different OS, it is your responsibility to figure out how to connect to cs3700a and cs3700b for programming assignments and submit your work by the cutoff deadline.  Such</td>

  </tr>

  <tr>

   <td width="320">issues cannot be used as an excuse to request any extension.</td>

   <td width="400"><strong> </strong></td>

  </tr>

 </tbody>

</table>




<ol>

 <li>MAKE a directory “<strong>HW02</strong>” under your home directory on <strong>cs3700a</strong>.msdenver.edu and <strong>cs3700b</strong>.msudenver.edu, a subdirectory “<strong>server</strong>” under “<strong>HW02</strong>” on <strong>msudenver.edu</strong>, and a subdirectory “<strong>client</strong>” under “<strong>HW02</strong>” on <strong>cs3700b.msudenver.edu</strong>.</li>

 <li>UPLOAD and COMPILE the <strong><em>server</em></strong> program under “<strong>HW02/server</strong>” and the <strong><em>client</em></strong> program under “<strong>HW02/client</strong>” on the VMs.</li>

 <li>TEST <strong><em>the</em></strong> <strong><em>server program</em></strong> running on <strong>cs3700a</strong>.msudenver.edu together with <strong><em>a client program</em></strong> running on your laptop or lab computer and <strong><em>another client program</em></strong>, simultaneously, running on <strong>cs3700b</strong>.msudenver.edu to test all the possible cases.</li>

 <li>SAVE a file named <strong><em>txt</em></strong> under “<strong>HW02/client</strong>” on <strong>cs3700b</strong>.msudenver.edu, which captures the outputs of your <strong><em>client</em></strong> program when you test it. You can use the following command to redirect the standard output (stdout) and the standard error</li>

</ol>

(stderr) to a <strong>file</strong> on UNIX, Linux, or Mac, and view the contents of the file

<strong>java prog_name_args | tee testResultsClient.txt //copy stdout to the .txt file cat file-name     //display the file’s contents.  </strong>