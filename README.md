defcon_badgetag
===============

Defcon 22 badge - laser tag built with @joshcano



++ iterator
Github for raw bytecode: git.io/JxQtSg

100	1
010	2 1
001	4 2
101	5 1
011	6 1
111	7 1

0000
1000 1 
0100 2 1
0010 4 2
0001 8 4
1001 9 1
0101 10 1
0011 12 2
1011 13 1
0111 14 1
1111 15 1


leds := %0
floater := %1
repeat max_floating_bit from 4 to 1
	repeat max_floating_bit
		set_leds(leds | floater)
		floater >>= 1
		pause (64)
	leds |= floater
	floater := 1
