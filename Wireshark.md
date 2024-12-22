# Wireshark - Analyzing Packets 

## Scenario

In this scenario, I'm a security analyst investigating traffic to a website.

Here, I analyze a network packet capture file that contains traffic data related to a user connecting to an internet site.


## Solutions 
1. Identifing the source and destination IP addresses involved in this web browsing session.
* On the title bar, I typed in `ip.addr == 142.250.1.139` to filter for traffic associated with that specific IP address. Then I selected the first packet that contains `TCP` on the info field.I used `addr` to indicate either the source or the destination IP. 

![chrome_clrxVrSKGe](https://github.com/Kwangsa19/Ketmanto-Cybersecurity-Portfolio/assets/135963482/0027d233-ae17-49a6-979c-1b8f3f003637)

![chrome_poRy9LUK7I](https://github.com/Kwangsa19/Ketmanto-Cybersecurity-Portfolio/assets/135963482/d2e2507c-ba58-4c4d-a6b5-43e511068100)

* On the title bar, I then typed `ip.src == 142.250.1.139` to filter for traffic associated with that specific IP address. I used `src` to indicate it is where the packet comes from.
  
![chrome_rKsf4FgKQK](https://github.com/Kwangsa19/Ketmanto-Cybersecurity-Portfolio/assets/135963482/48b3d84d-e5b1-4dc9-a6d8-363546b697bc)

  
* On the title bar, next I typed `ip.dst == 142.250.1.139` to filter for traffic associated with that specific IP address, using `dst` to indicate it is where the packet goes to.
  
![chrome_0BcQ5U6PID](https://github.com/Kwangsa19/Ketmanto-Cybersecurity-Portfolio/assets/135963482/19394509-d60b-48eb-9d41-176d5bffbc00)

* On the title bar, I inputted `eth.addr == 42:01:ac:15:e0:02` to filter for traffic associated with that specific Ethernet MAC address. Using `addr` to inicate it can be either the source or the destination IP. 

![chrome_FNyXuNAoQH](https://github.com/Kwangsa19/Ketmanto-Cybersecurity-Portfolio/assets/135963482/4385847b-0f9f-4fe5-99af-2dc3792f64f1)

2. Examining the protocols that are used when the user makes the connection to the website.
* The TCP destination port of this TCP packet is 80 when `ip.addr == 142.250.1.139` which contains the initial web request to an HTPP website that will typically be listening on TCP port 80.

![chrome_v0w4jPKpnG](https://github.com/Kwangsa19/Ketmanto-Cybersecurity-Portfolio/assets/135963482/5ce9594c-e9c3-49a2-9d93-cd0da4cb1e3b)

* The protocol destination port is TCP when Etherenet address was `42:01:ac:15:e0:02`. Source address is `172.21.224.2` and the destination address is `35.235.244.34`. 

![chrome_PAHlQSZJOk](https://github.com/Kwangsa19/Ketmanto-Cybersecurity-Portfolio/assets/135963482/263e55d9-e6e7-4204-b4c3-1215a69c98a1)

3. Analyzing the data packet to identify the type of information sent and received by the systems that connect to each other when the network data is captured.
* On the title bar, I typed `tcp.port == 80` to filter for traffic associated with that specific port number. `tcp.port == 80` means only the tcp port is 80 will be shown. 
  
![chrome_MNHnvAhm6o](https://github.com/Kwangsa19/Ketmanto-Cybersecurity-Portfolio/assets/135963482/28081462-b634-4838-a307-b9574e7f3234)

* When the filter `tcp.port == 80` sets in play, the time to live is 64.
  
![chrome_iI9QT2BqWs](https://github.com/Kwangsa19/Ketmanto-Cybersecurity-Portfolio/assets/135963482/1fe9ba32-926b-42f3-a39e-49da54240058)


* When the filter `tcp.port == 80` sets in play, the Frame Number is 37 and Frame Length is 54 bytes.

![chrome_xSk2HRghJg](https://github.com/Kwangsa19/Ketmanto-Cybersecurity-Portfolio/assets/135963482/107d084b-361e-4f74-98ea-c90c93fe1cae)

<h3>I have now analyzed and filtered this netowrk's traffic and sniffed the necessary packets using wireshark to gather relevant information, which is an essential anility as a security analyst!</h3>
