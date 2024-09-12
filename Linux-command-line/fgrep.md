# fgrep

<b>To find the exect word(same to same)</b>

fgrep is a variant of the grep command in Linux/Unix systems. It stands for "fixed grep" or "fast grep." Unlike the standard grep command, fgrep searches for fixed string patterns instead of interpreting them as regular expressions. This makes fgrep faster for simple string searches because it doesn't need to parse and evaluate regular expressions.

## Key Features

<b>Literal String Matching:</b> fgrep treats the search pattern as a simple string of characters, without any special meaning assigned to characters like . or *.

<b>Speed:</b> Because fgrep does not process regular expressions, it can be faster for large files or large numbers of files when you only need to search for literal strings.

## Basic Syntax

fgrep [options] string [file...]

## Example: 

There is a file named “cpfile1.txt”.
Now reading this file via “cat” command.

### Input: 

cat cpfile2.txt

### output: 

rashik-chy

rashik*chy

rashik_chy

rashik=chy

## Now using the “fgrep” command to find the exect pattern.

### Input: 

<b>fgrep rashik_chy cpfile2.txt</b>

### output: 

<b>rashik_chy</b>


