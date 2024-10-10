# arch

The arch command is used in Linux to display the machine architecture of the system (i.e., the type of processor or hardware platform that the system is running on). It is a simple command that outputs the architecture type, which is often useful when determining the appropriate version of software to install or when scripting to account for different architectures.

## Usage

#### Input:
<pre>
arch
</pre>

#### Output:

The arch command will return the system's architecture, such as:

+ x86_64: 64-bit architecture (commonly used for modern processors)
+ i386 or i686: 32-bit architecture
+ arm: ARM architecture (commonly found in mobile devices and Raspberry Pi)
+ aarch64: 64-bit ARM architecture

## Example
To display the machine architecture:
#### Input:
<pre>
arch
</pre>

Output:
<pre>
x86_64
</pre>

This output indicates that the system is running on a 64-bit architecture.