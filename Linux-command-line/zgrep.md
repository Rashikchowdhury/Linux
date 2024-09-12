# zgrep

<b>It is used to read zipped files</b>

zgrep is a command in Linux used to search within compressed files, particularly those that are compressed with gzip (having a .gz extension). 
It works similarly to grep, but it can handle compressed files directly without the need to manually decompress them first.

## Basic syntax

zgrep [options] pattern file.gz

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
