## L8.3: Big text file handling

Searching in a a text file consisting of many lines of phone numbers.
```Python
f = open('directory.txt', 'r')
s = '0'
flag = 0
while(s != ''): # When fp reaches end, s will be `""`.
	s = f.readline()
	if (n == "9284903982"):
		print("The number was found")
		flag = 1
		break
if (flag == 0):
print("The number was not found")
```

## L8.4: Very big files -- a tip

No matter how big the file is, we can always read from it line by line.

`#######
	⬆️`
## L8.5: Caesar Cipher

This program considers an input file and encrypts it by using a caeser file, shifting the letters by 3 units (a -> d, b -> e, ... , x -> a, y -> b, z -> c)
```Python
import string

def create_caesar_dictionary():
	l = list(string.ascii_lowercase)
	# convert i-th letter to (i+3)%26-th letter
	d = {}
	for i in range(len(l)):
		d[l[i]] = l[(i+3)%26]
	return d	

def main():
	instr = input("Enter the string to be encrypted: ")
	
	d = create_caesar_dictionary()
	f = open("sherlock.txt", 'r')
	g = open("encrypted_sherlock.txt', 'w')
	c = f.read(1) # reads 1 character
	while (c != ''):
		g.write(d[c]) # writes corresponding character to g
		c = f.read(1) # reads next character of f		
	f.close()
	g.close()

main()
```
## L8.6 File handling, genetic sequences

The human genetic sequence contains of A,C,T,G.
input `human.txt`
```Python
f = open("human.txt", 'r')
seq = f.read() # puts entire contents into a string seq
diab = "GTATGAC" # some substring causing diabetes
if diab in seq:
	print("You are predisposed to diabetes.")
```