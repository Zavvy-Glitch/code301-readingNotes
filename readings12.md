# Reading 12

## Status Codes Based On REST Methods

### Notes Based Upon [HTTP Status Codes](https://www.moesif.com/blog/technical/api-design/Which-HTTP-Status-Code-To-Use-For-Every-CRUD-App/)

1. In your own words, describe what each group of status code represents:
      - 100’s = Informational Status Codes: equest has been received and the server will try to comply with a transmission demand of the client. Like using a different protocol or telling the client that its request will fail before they start sending the body.

      - 200’s = Succes Codes. The tell the client that their requests have been successfully accepted.
      - 300’s = Redirection Codes. They tell the client that the requests that have been made are not available or it is no longer in the location they have requested from.
      - 400’s = Client Error Codes. All invalid requests sent by the client to a server. Usually caused by incorrect inputs/parameters.
      - 500’s = Server Error Codes. Something overwhelmed the server (excessive data) or the server couldn't be reached.

2. What is a status code 202?
      - Accepted - Often used for asynchronous processing. This code tells the client that the request was valid, but its processing will finish sometime in the future. The response body should include an URL to the finished resource with some information about when it will be available, or an URL to some monitoring endpoint that tells the client when the resource is available.

3. What is a status code 308?
    - Permanent Redirect - This tells the client to use another URL to access the resource and not use the current URL anymore. It’s helpful when we have multiple endpoints for one resource, but don’t want to implement reading from all of them.

4. What code would you use if an update didn’t return data to a client?
    - 204 No Content - A proper code for updates that don’t return data to the client, for example when just saving a currently edited document.

5. What code would you use if a resource used to exist but no longer does?
    - I'd personally use a 301 for permanently moved? However the closest I can find on the site is 308 Permanent Redirect - This is the right code if the resource will now be available at a new URL and the client should directly access it via the new URL in the future. The current endpoint can’t control the clients’ behavior after the request and a subsequent redirect if the resource URL changes again have to be issued from the new URL.

6. What is the ‘Forbidden’ status code?
    - 403 Forbidden - The client has authorized or doesn’t need to authorize itself, but still has no permissions to access the resource.
