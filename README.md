Download Link: https://assignmentchef.com/product/solved-csci2275-assignment-4-communication-between-towers
<br>
In the Lord of the Rings trilogy, there is a scene where the first beacon is lit in the towers of Minas Tirith. The second beacon then sees the fire, and knows to light its fire to send a signal to the third beacon, and so forth. This was a means of communicating in the days before telegraphs were invented as it was much faster than sending a human rider to deliver a message. Communication towers were equipped with signaling mechanisms, such as mirrors, that could spell out messages using the positions of the mirrors.

Today, there are several examples of communication networks that are conceptually similar, but much more technically advanced, that route messages through multiple hubs between the sender and the receiver. For example, when you type a URL into a web browser, a request is sent through a network of service providers to the destination, and then packets of information are sent back to your machine. If I type <a href="https://www.google.com">www.google.com</a> from my home in Boulder, my request follows this path:

1  192.168.2.1 (192.168.2.1)

2 <a href="http://c-24-9-60-1.hsd1.co.comcast.net">c-24-9-60-1.hsd1.co.comcast.net</a> (24.9.60.1)

3 <a href="http://te-9-7-ur02.boulder.co.denver.comcast.net">te-9-7-ur02.boulder.co.denver.comcast.net</a>

4 <a href="http://xe-13-3-1-0-ar01.aurora.co.denver.comcast.net">xe-13-3-1-0-ar01.aurora.co.denver.comcast.net</a>

5 <a href="http://he-3-10-0-0-cr01.denver.co.ibone.comcast.net">he-3-10-0-0-cr01.denver.co.ibone.comcast.net</a> (68.86.92.25)

te<u> 1 1 0 4 </u><a href="http://cr01.chicago.il.ibone.comcast.net">cr01.chicago.il.ibone.comcast.net</a> (68.86.95.205)

6 xe2<u> 0 0 0 </u><a href="http://pe01.910fifteenth.co.ibone.comcast.net">pe01.910fifteenth.co.ibone.comcast.net</a> (68.86.82.2)

7 <a href="http://as15169-1-c.910fifteenth.co.ibone.comcast.net">as15169-1-c.910fifteenth.co.ibone.comcast.net</a> (23.30.206.106)

8  72.14.234.57 (72.14.234.57)

9 209.85.251.111 (209.85.251.111)

10 <a href="http://den03s06-in-f16.1e100.net">den03s06-in-f16.1e100.net</a> (74.125.225.208)

Each IP address is a hop in the network for my request, which is received at each service provider and then forwarded to the next service provider in the network, depending on the final destination of the message.

(Note: I got this path by typing traceroute <a href="https://www.google.com">www.google.com</a> in a terminal window. From campus, you will see a different path.)

<strong>Build your own communications network</strong>

I n this assignment, you’re going to simulate a communications network using a linked list. Each node in your linked list will represent a city and you need to be able