# grep

The grep command in Linux is used to search for specific patterns within files or text. It stands for "global regular expression print." Here’s a basic guide to using the grep command:

## Basic syntax

grep [options] pattern [file...]

## Common Options

+ -i : Ignore case distinctions in the pattern.
+ -v : Invert the match, showing lines that do not match the pattern.
+ -r or -R : Recursively search subdirectories.
+ -l : Show the names of files with matching lines, not the lines themselves.
+ -n : Prefix each line of output with the line number within its file.
+ -c : Print only a count of matching lines per file.
+ -w : Match whole words only.
+ -o : Show only the part of a line matching the pattern.

## Example:

There is a file named “cpfile1.txt”. Now reading this file via “cat” command.

### Input:

<b>cat cpfile1.text</b>

### Output:

this is second line Life is a journey, not a destination. Along the way, you'll encounter challenges, but each obstacle is an opportunity for growth. Embrace the ups and downs, for they shape who you are. Remember, it's not about the speed at which you reach your goals, but the lessons you learn and the experiences you gain along the way. Keep pushing forward, stay positive, and trust that everything will work out in the end.

## Now using the “grep” command to find a pattern.

### Input:

<b>grep this cpfile1.txt</b>

### Output:

<b>this</b> is a test file for copy paste <br>
<b>this</b> is second line