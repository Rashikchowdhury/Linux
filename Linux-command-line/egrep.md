# egrep 

<b>To search multiple word in one the same time.</b>

Equivalent to grep -E, which allows the use of extended regular
expressions. Egrep is deprecated but still commonly found. Modern usage
prefers grep -E.

### Usages: 

egrep "pattern" file.txt

## Example: 

There is a file named “cpfile1.txt”.
Now reading this file via “cat” command.

### Input: 

cat cpfile1.txt

### output: 

this is second line
Life is a journey, not a destination. Along the way, you'll encounter challenges, 
but each obstacle is an opportunity for growth. Embrace the ups and downs, for they 
shape who you are. Remember, it's not about the speed at which you reach your goals,
but the lessons you learn and the experiences you gain along the way. Keep pushing forward,
stay positive, and trust that everything will work out in the end.


## Now using the “egrep” command to find a pattern.

### Input: 

<b>egrep this cpfile1.txt</b>

### output: 

<b>this</b> is a test file for copy paste
<b>this</b> is second line

## To find multiple pattern:

### input: 

<b>egrep "gain|this" cpfile1.txt</b>


### output: 

<b>this</b> is a test file for copy paste
<b>this</b> is second line
Life is a journey, not a destination. Along the way, you'll encounter challenges,
but each obstacle is an opportunity for growth. Embrace the ups and downs, 
for they shape who you are. Remember, it's not about the speed at which you reach your goals,
but the lessons you learn and the experiences you <b>gain</b> along the way. Keep pushing forward,
stay positive, and trust that everything will work out in the end.
