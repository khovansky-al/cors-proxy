# CORS Proxy

This simple Node.js-based proxy allows your JavaScript application to call services that are hosted on a different domain and that don't support [CORS](http://en.wikipedia.org/wiki/Cross-origin_resource_sharing). 

Because the proxy is itself CORS-enabled, your application and the proxy don't have to be hosted on the same 
domain.

This is a fork of https://github.com/ccoenraets/cors-proxy that was modified for the needs of RC billing team

## Installation

- Clone this repository
- Install the server dependencies

    ```
    npm install
    ```

- Start the server

    ```
    node server
    ```

## Usage

When making an API call using JavaScript (using XMLHTTPRequest, $.ajax, etc):

1. Substitute the actual service URL with the Proxy URL 

2. Set the request method, query parameters, and body as usual

3. Set the actual service URL in a header named 'Target-Endpoint'

4. Send the request as usual