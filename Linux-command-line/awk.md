# awk

awk is a powerful text-processing language used for pattern scanning and processing. It is especially useful for manipulating structured data and generating reports. It processes text line by line and splits each line into fields, allowing you to select, filter, and format the output based on your requirements.

## Usage

<pre>
awk 'pattern { action }' filename
</pre>

+ <b>pattern</b>: Specifies the text pattern or condition to match.
+ <b>action</b>: Specifies the operation to perform when a match is found.

## Syntax Structure
+ Fields in each line are separated by whitespace by default, and each field can be accessed using $1, $2, $3, etc.
+ $0 refers to the entire line.

## Common Options

+ -F 'delimiter': Specifies the field separator (delimiter) other than whitespace.

<pre>
awk -F ',' '{print $1}' file.csv
</pre>


## Examples

+ Print Entire File: To print all lines of a file:

<pre>
awk '{print}' filename
</pre>

+ Print Specific Field: To print the first field (column) of each line:

<pre>
awk '{print $1}' filename
</pre>


+ Print Multiple Fields: To print the first and third fields:

<pre>
awk '{print $1, $3}' filename
</pre>


+ Print Lines Matching a Pattern: To print lines that contain the word "error":

<pre>
awk '/error/ {print}' logfile
</pre>
