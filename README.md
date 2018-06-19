# ╱╱╱╱╱╱╱╱╲╲╲╱╲╱╱╱╱╲╲╲╱╲╲╲╱╱╱╱╲╱╱╱╱╱╲╲╱╱╲╱╱╲╱╱╲╲╲╲╱╱╱╲╲╱╲╲╲╱╲╱╲╱╱╱╲╲╲╲╲╲╱╱╲╱╲╲╲╱╱╲╲

## 10PRINT.js
This is a program I wrote in Node.js that recreates the terse single line
program 10PRINT using a single statement.

10PRINT is a 30-some year old program written in BASIC on the Commodore 64.  It
randomly writes forward- or back-slashes to the screen one at a time until the
user stops the program.  10PRINT is typically shown in this form:

```
10 PRINT CHR$(205.5+RND(1)); : GOTO 10
```

My translation of this program into Node.js looks like this:

```
while(1){process.stdout.write(String.fromCharCode(9585+Math.random()*2))}
```

# Getting Started
You'll need a terminal with git and node.js installed

Clone this repository to your local environment.  
In the project directory use the following command:

```
node .
```

The program will write characters to the screen until you stop the program by
pressing 'Control-C' in the terminal.  Depending on your terminal you'll have
other options to stop the program, but 'Control-C' is pretty universal.

A previous version of my program printed a finite number of characters to the
screen and then stopped.  Previous versions also printed the entire sequence
of characters at once.  In the spirit of 10PRINT I revised it to the unbounded
loop you see above which prints characters one at a time.

Here is one previous version, scrapped because it printed all 10,000 characters
at once:

```
s='';while(s.length<1e4){s+=Math.round(Math.random())?'/':'\\'}console.log(s)
```

This was an improvement but I scrapped it in favor of writing the characters
using their charCode instead of string literals:

```
while(1){process.stdout.write(Math.round(Math.random())?'╱':'╲')}
```

# Making it look good
The output of this program may look better if you can change your font.  In
my terminal it looked best when I chose the font Futura, though there were
several almost identical choices.

Picking a font that displays the slashes at 45 degrees is ideal.

# Other neato burrito variations

```
while(1){process.stdout.write(String.fromCharCode(9585.95+Math.random()*1))}
```

```
while(1){process.stdout.write(String.fromCharCode(9585+Math.random()*3))}
```

```
while(1){process.stdout.write(String.fromCharCode(9487+Math.round(Math.random()*56)))}
```

```
while(1){process.stdout.write(String.fromCharCode(9138+Math.random()*2))}
```

```
while(1){process.stdout.write(String.fromCharCode(9144+Math.random()*4))}
```

```
while(1){process.stdout.write(String.fromCharCode(5177+Math.random()*16))}
```

```
while(1){process.stdout.write(String.fromCharCode(10548+Math.random()*4))}
```



# Like to read?
There is a book written by Nick Montfort and others and is available to [read
online](http://nickm.com/trope_tank/10_PRINT_121114.pdf).  It covers the back-
ground, variations, ports to other languages (like mine!), influences of 10PRINT
and topics like randomness, art, other one-line-programs, and other esoterica.

Enjoy!

# ╲╲╱╲╱╲╱╱╱╱╲╱╱╲╱╲╱╱╲╲╲╲╱╱╲╲╱╱╱╲╱╲╱╲╱╲╲╱╱╲╲╱╱╱╲╲╱╱╱╲╲╲╱╲╲╲╱╲╱╲╲╱╱╱╱╱╲╱╲╲╱╱╱╲╲╱╲╱╱╲╱
