# MergeWordlists

This script will take two wordlist files as arguments and output their cartesian product. 
I found the need to make this script while studying Pentesting. It is useful to create custom wordlists for password cracking.

The size of the output will always be the number of lines of the first file times the number of lines of the second, so the user must be careful not to generate extremely huge files or to crash their machine.

Example use case:

```bash
root@kali:~/Documents# cat file1
ACE
2
3
4
5
6
7
8
9
10
J
Q
K
root@kali:~/Documents# cat file2
SPADES
DIAMONDS
HEARTS
CLUBS
root@kali:~/Documents# ./mergeWordlists.sh file1 file2 
ACESPADES
ACEDIAMONDS
ACEHEARTS
ACECLUBS
2SPADES
2DIAMONDS
2HEARTS
2CLUBS
3SPADES
3DIAMONDS
3HEARTS
3CLUBS
4SPADES
4DIAMONDS
4HEARTS
4CLUBS
5SPADES
5DIAMONDS
5HEARTS
5CLUBS
6SPADES
6DIAMONDS
6HEARTS
6CLUBS
7SPADES
7DIAMONDS
7HEARTS
7CLUBS
8SPADES
8DIAMONDS
8HEARTS
8CLUBS
9SPADES
9DIAMONDS
9HEARTS
9CLUBS
10SPADES
10DIAMONDS
10HEARTS
10CLUBS
JSPADES
JDIAMONDS
JHEARTS
JCLUBS
QSPADES
QDIAMONDS
QHEARTS
QCLUBS
KSPADES
KDIAMONDS
KHEARTS
KCLUBS
```
