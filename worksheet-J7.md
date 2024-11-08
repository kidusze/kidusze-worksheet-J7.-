1.  All packets have a header, which stores the address or destination of a packet, and a payload which stores the data or message of the packet.

2. The internet layer in the TCP/IP protocol(roting those packet to the right places) is responsible for routing data packets across multiple networks, ensuring they reach their intended destination by utilizing IP addresses to identify devices and determine the best path to send data through.As a client, I primarily need to specify the destination IP address to send data to a specific device on the network

3. The transport layer in the TCP/IP protocol (can i be reliable and drop a packet or do i need to accoutnfor evey packet)is responsible for establishing a reliable connection between two devices, ensuring data is delivered in the correct order and without errors, by managing the flow of data between applications on different hosts, including error detection, retransmission, and sequencing. As a client, I need to specify the destination port number to identify the specific application on the receiving device you want to communicate with.

4. The main difference between SMTP and HTTP is that SMTP is used to transmit emails, while HTTP is used to transmit information between a client and a web server.HTTP is used for web pages and websites and SMTP is for emails.

5. An IP address is a numerical code that uniquely identifies a device on the internet, while a domain name is a human-readable name associated with that IP address

6. It used it to identify specific applications or services running on a computer. The port address is a way for the Operating System to divide up the data arriving from the network based on the destination process. In the operating systemt the port tells it to through a certain path to get it to the right destination."The purpose to allow th einternet traffic to got to individual ports". (route traffic to the right application)

7.
```java
import java.util.*;
import java.net.*;
import java.io.*;

public class HelloSocket{

    public static void main(String args[]){

        Socket sock=null;        
        try{
           sock = new Socket(123.45.678.900,4040);
        }catch(Exception e){
            System.err.println("Cannot Connect");
            System.exit(1);
        }

        try{
            PrintWriter pw = new PrintWriter(sock.getOutputStream());
            pw.println("red");
            pw.flush(); // Bufferr maybe print a bunch of things but it takes a while so you can flush to send them on time
            pw.close(); //close the stream
            in.close();
            sock.close();//close the socket
        }catch(Exception e){
            System.err.print("IOException");
            System.exit(1);
        }

    }
}

```
8.  InputStream:- read data from the source once at a time. OutputStream:- write data to the destination once at a time.

9.  A Socket it acts as  a communication endpoint on a network, representing a single connection between two devices, while a SocketServer is a framework that allows you to create a server application which can listen for and manage multiple incoming connections on a specific port. One makes the clinet and the other makes The server. They both have an ip address and socket server has accept() which takes as many connections as possible that is there difference.

10.  Threads are useful for servers because they allow a server to handle multiple requests at the same time, which improves performance and responsiveness. If we allow thread to handle this connections we can have a parallized connections.
   
