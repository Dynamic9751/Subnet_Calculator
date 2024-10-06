# Vohala_Subnet_Calculator

This is a simple web-based subnet calculator designed to help users calculate subnet information such as the network address, usable host range, broadcast address, and the total number of hosts based on an IP address and CIDR (Classless Inter-Domain Routing) notation.
Features

    Input an IP address and choose the CIDR notation to calculate the subnet information.
    Displays the network address, usable host IP range, broadcast address, total hosts, and usable hosts.
    Provides the corresponding subnet mask for the given CIDR notation.
    Easy-to-use interface with clear inputs and results displayed in real-time.

Usage

    Clone the repository or download the files.
    Open the index.html file in any modern web browser.
    Enter the IP address (e.g., 192.168.1.1).
    Select the CIDR notation from /1 to /32.
    Click the "Calculate" button to get the subnet information.

Example

For example, if you enter:

    IP Address: 192.168.1.1
    CIDR Notation: /24

The calculator will display:

    Network Address: 192.168.1.0
    Usable Host IP Range: 192.168.1.1 - 192.168.1.254
    Broadcast Address: 192.168.1.255
    Total Number of Hosts: 256
    Number of Usable Hosts: 254
    Subnet Mask: 255.255.255.0

Code Explanation

    HTML: The structure of the page includes input fields for the IP address and CIDR notation. The dropdown for CIDR options is populated dynamically.
    CSS: Styles are provided to create a clean, modern user interface with clearly visible input fields and results.
    JavaScript: The core logic for subnet calculation, including:
        CIDR to Subnet Mask Conversion: Converts CIDR notation into the corresponding subnet mask.
        Network and Broadcast Address Calculation: Determines the network and broadcast address based on the IP and subnet mask.
        Host Range Calculation: Calculates the first and last usable IPs and the total number of hosts in the subnet.

Calculation Logic:

    Subnet Mask Calculation: Converts CIDR to the appropriate 32-bit subnet mask.
    Network Address: AND operation between the IP and subnet mask.
    Broadcast Address: OR operation between the network address and the inverted subnet mask.
    Usable Hosts: Range between network address + 1 and broadcast address - 1 (special cases for /31 and /32).

Contributing

Feel free to fork this repository and contribute by submitting pull requests with improvements, additional features, or optimizations.
