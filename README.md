<html>
<body>

<h1>Port Scanner</h1>

<p>This is a port scanner that can scan a single or multiple IP addresses and ports, and check for vulnerabilities. It has the following functions:</p>

<ul>
  <li><strong>scan_port(ip_address, port)</strong>: This function scans a single port on a given IP address and checks for vulnerabilities. It does this by creating a socket and connecting to the target port, sending a request to the server, and receiving a response. It then parses the response to extract the status line, and prints it. It also uses the <strong>nmap</strong> library to scan the port and check for vulnerabilities. If a vulnerability is found, it prints the name of the vulnerability. If the port is closed or there is no response from the port, it prints an appropriate message.</li>
  <li><strong>scan_ports(ip_address, ports)</strong>: This function scans a list of ports on a given IP address and checks for vulnerabilities. It does this by iterating over the list of ports and calling the <strong>scan_port()</strong> function for each port.</li>
  <li><strong>scan_all_ports(ip_address)</strong>: This function scans all ports on a given IP address and checks for vulnerabilities. It does this by using the <strong>nmap</strong> library to scan all ports on the target, printing the detected operating system, and then iterating over the ports and calling the <strong>scan_port()</strong> function for each port.</li>
  <li><strong>main()</strong>: This is the main function of the program. It prompts the user to enter target IP addresses and port numbers, converts the input into lists of IP addresses and ports, and then scans the targets by either calling the <strong>scan_all_ports()</strong> function if a single target is entered, or iterating over the list of targets and calling the <strong>scan_ports()</strong> function for each target.</li>
</ul>

<p>The code begins by importing the <strong>socket</strong> and <strong>nmap</strong> libraries. The <strong>socket</strong> library is used to create sockets and communicate with servers, while the <strong>nmap</strong> library is used to scan ports and check for vulnerabilities.</p>

<p>The main function is called at the end of the code, and it starts the program by prompting the user for the targets and ports to scan. The program then scans the targets and prints the results.</p>

</body>
</html>
