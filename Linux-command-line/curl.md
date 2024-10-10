# Curl

curl (Client URL) is a versatile command-line tool used to transfer data to or from a server using various network protocols. It supports protocols like HTTP, HTTPS, FTP, SMTP, and more. curl is widely used for tasks such as downloading files, testing APIs, and interacting with web services.

## Usage

curl is used to perform data transfers, interact with APIs, download/upload files, and automate web-related tasks directly from the terminal.

## Syntax:

<pre>
curl [options] [URL]
</pre>

## Common Options:

+ -X, --request [command]: Specifies a custom request method to use when communicating with the HTTP server (e.g., GET, POST, PUT, DELETE).

<pre>
curl -X POST https://api.example.com/data
</pre>

+ -d, --data [data]: Sends the specified data in a POST request to the HTTP server.

<pre>
curl -d "param1=value1&param2=value2" -X POST https://example.com/form
</pre>

+ -H, --header [header]: Adds a custom header to the request.

<pre>
curl -H "Content-Type: application/json" https://api.example.com/data
</pre>

+ -o, --output [file]: Writes the output to a file instead of standard output.

<pre>
curl -o filename.html https://www.example.com
</pre>

+ -O, --remote-name: Saves the file with its original name from the URL.

<pre>
curl -O https://www.example.com/file.zip
</pre>

+ -I, --head: Fetches the headers only.

<pre>
curl -I https://www.example.com
</pre>

+ -u, --user [user:password]: Specifies the user name and password for server authentication.

<pre>
curl -u username:password https://secure.example.com
</pre>

+ -L, --location: Follows redirects if the server responds with a redirect status code.

<pre>
curl -L https://short.url/redirect
</pre>

+ -s, --silent: Runs curl in silent mode, hiding progress and error messages.

<pre>
curl -s https://www.example.com
</pre>

+ -v, --verbose: Provides detailed information about the request and response, useful for debugging.

<pre>
curl -v https://www.example.com
</pre>


## Difference Between curl and wget:

While both curl and wget are used for downloading files and interacting with servers, they have some differences:

+ Protocols Supported:

    + wget primarily supports HTTP, HTTPS, and FTP.
    + curl supports a broader range of protocols, including HTTP, HTTPS, FTP, FTPS, SCP, SFTP, LDAP, and more.

+ Use Cases:

    + wget is more suited for downloading files and recursively downloading directories.
    + curl is better for interacting with APIs, sending data, and more complex request scenarios.

+ Output Handling:

    + get automatically downloads files to the current directory.
    + curl outputs data to standard output by default, but can also save to files using options.
+ Recursive Downloading:

    + wget supports recursive downloading out of the box.
    + curl does not support recursive downloading; additional scripting is required.

    