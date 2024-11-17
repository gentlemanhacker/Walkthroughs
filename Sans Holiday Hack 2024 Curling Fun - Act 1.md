# Sans Holiday Hack 2024 Curling Fun - Act 1

**To use curl and ignore certificate validation (not recommended for production due to security risks), you can use the -k or --insecure flag.**

curl -k <https://example.com>

Explanation:

\-k or --insecure: Tells curl to bypass SSL certificate checks, ignoring problems such as self-signed certificates, expired certificates, or mismatched domain names.

Use Case Warning:

Disabling certificate validation exposes you to man-in-the-middle attacks and other security risks. Use this flag only in secure, controlled environments (e.g., development or testing).

**Working with APIs and embedded devices often requires making HTTP POST requests. Use curl to send a request to <https://curlingfun:9090/> with the parameter "skip" set to the value "alabaster", declaring Alabaster as the team captain.**

curl --insecure --data "skip=alabaster" <https://curlingfun:9090/>

Explanation:

\--insecure: Bypasses SSL certificate validation.

\--data "skip=alabaster": Sends the HTTP POST parameter skip with the value alabaster in the request body.

<https://curlingfun:9090/>: The target URL for the request.

This command declares alabaster as the team captain by passing the skip parameter to the server.

**Use curl to send a request to <https://curlingfun:9090/> with a cookie called "end" with the value "3", indicating we're on the third end of the curling. To send a request with a cookie using curl, you can use the --cookie option. Here's the command to include a cookie named end with the value 3:**

curl --insecure --cookie "end=3" <https://curlingfun:9090/>

Explanation:

\--insecure: Bypasses SSL certificate validation (use only in non-production environments).

\--cookie "end=3": Adds a cookie named end with the value 3 to the HTTP request.

<https://curlingfun:9090/>: The target URL for the request.

**Use curl to view the HTTP headers returned by a request to** [**https://curlingfun:9090/**](https://curlingfun:9090/) **To view the HTTP headers returned by a request using curl, use the -I (uppercase "i") or --head option. Here's the command:**

curl --insecure -I <https://curlingfun:9090/>

Explanation:

\--insecure: Bypasses SSL certificate validation (use only in safe environments).

\-I or --head: Requests only the headers from the server instead of the full response body.

<https://curlingfun:9090/>: The target URL.

**Use curl to send a request to <https://curlingfun:9090/> with an HTTP header called "Stone" and the value "Granite". To send a request with a custom HTTP header using curl, you can use the -H or --header option. Here's how to include the Stone header with the value Granite:**

curl --insecure -H "Stone: Granite" <https://curlingfun:9090/>

use curl to retrieve the following URL containing special characters: <https://curlingfun:9090/../../etc/hacks>

When a URL contains special characters like .., &, or ?, you should use URL encoding or quote the entire URL to ensure proper handling by curl.

curl --insecure "<https://curlingfun:9090/../../etc/hacks>"

Explanation:

Quoting the URL: The double quotes (") ensure that special characters like .. are not interpreted by the shell but are passed directly to curl.

Alternatively

\--path-as-is

curl -k --insecure "<https://curlingfun:9090/../../etc/hacks>" --path-as-is
