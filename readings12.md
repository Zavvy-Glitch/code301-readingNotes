
Reading 10: OAuth
- Citation: Information recieved from (https://auth0.com/docs/flows)

# Oauth Definition:
- Open Standard authorization protocol or framework.
- Describnes how unrelated servers and services safely allow authenticated access to their assets.
  - Will not share:
    - initial,
    - related
    - single log-on credential
  - AKA: Secure, third-party, user-agent, delegated authorization.

## Examples:
-  user sending cloud-stored files to another user via email
-  end-user using a third-party printing service to print picture files stored on an unrelated web server

## How does it work?
- Authentication is the process of a user/subject proving its ownership of a presented identity, by providing a password or some other uniquely owned or presented factor. Authorization is the process of letting a subject access resources after a successful authentication, oftentimes somewhere else.
- Authorization vs. Authentication
- OAuth essentially allows the user, via an authentication provider that they have previously successfully authenticated with, to give another website/service a limited access authentication token for authorization to additional resources
   - The cycle:
    1. The first website connects to the second website on behalf of the user, using OAuth, providing the user’s verified identity.
    2. The second site generates a one-time token and a one-time secret unique to the transaction and parties involved.
    3.The first site gives this token and secret to the initiating user’s client software.
    4.The client’s software presents the request token and secret to their authorization provider (which may or may not be the second site).
    5. If not already authenticated to the authorization provider, the client may be asked to authenticate. After authentication, the client is asked to approve the authorization transaction to the second website.
    6.The user approves (or their software silently approves) a particular transaction type at the first website.
    7. The user is given an approved access token (notice it’s no longer a request token).
    8. The user gives the approved access token to the first website.
    9. The first website gives the access token to the second website as proof of authentication on behalf of the user.
    10. The second website lets the first website access their site on behalf of the user.
    11.The user sees a successfully completed transaction occurring.
    12. OAuth is not the first authentication/authorization system to work this way on behalf of the end-user. In fact, many authentication systems, notably Kerberos, work similarly. What is special about OAuth is its ability to work across the web and its wide adoption. It succeeded with adoption rates where previous attempts failed (for various reasons).

## What is OpenID?
- "OpenID is for humans logging into machines, OAuth is for machines logging into machines on behalf of humans."
-  The idea of Web 2.0 was that rather than having multiple logins for multiple websites, OpenID would serve as a single sign-in, vouching for the identities of users.

# Authorization vs. Authentication

## The Differences:
  - Auth0 uses the OpenID Connect (OIDC) Protocol and OAuth 2.0 Authorization Framework to authenticate users and get their authorization to access protected resources. With Auth0, you can easily support different flows in your own applications and APIs without worrying about OIDC/OAuth 2.0 specifications or other technical aspects of authentication and authorization.
 
## Authorization Code Flow:
  1. The user clicks Login within the regular web application.

  2. Auth0's SDK redirects the user to the Auth0 Authorization Server (/authorize endpoint).

  3. Your Auth0 Authorization Server redirects the user to the login and authorization prompt.

  4. The user authenticates using one of the configured login options and may see a consent page listing the permissions Auth0 will give to the regular web application.

  5. Your Auth0 Authorization Server redirects the user back to the application with an authorization code, which is good for one use.

  6. Auth0's SDK sends this code to the Auth0 Authorization Server (/oauth/token endpoint) along with the application's Client ID and Client Secret.

  7. Your Auth0 Authorization Server verifies the code, Client ID, and Client Secret.

  8. Your Auth0 Authorization Server responds with an ID Token and Access Token (and optionally, a Refresh Token).

  9. Your application can use the Access Token to call an API to access information about the user.

  10. The API responds with requested data.

## Authorization Code Flow with PKCE
  1. The user clicks Login within the application.

  2. Auth0's SDK creates a cryptographically-random code_verifier and from this generates a code_challenge.

  3. Auth0's SDK redirects the user to the Auth0 Authorization Server (/authorize endpoint) along with the code_challenge.

  4. Your Auth0 Authorization Server redirects the user to the login and authorization prompt.

  5. The user authenticates using one of the configured login options and may see a consent page listing the permissions Auth0 will give to the application.

  6. Your Auth0 Authorization Server stores the code_challenge and redirects the user back to the application with an authorization code, which is good for one use.

  7. Auth0's SDK sends this code and the code_verifier (created in step 2) to the Auth0 Authorization Server (/oauth/token endpoint).

  8. Your Auth0 Authorization Server verifies the code_challenge and code_verifier.

  9. Your Auth0 Authorization Server responds with an ID Token and Access Token (and optionally, a Refresh Token).

  10. Your application can use the Access Token to call an API to access information about the user.

  11. The API responds with requested data.

## Implicit flow:
- uses OIDC to implement web sign-in that is very similar to the way SAML and WS-Federation operates. The web app requests and obtains tokens through the front channel, without the need for secrets or extra backend calls. With this method, you don’t need to obtain, maintain, use, and protect a secret in your application.

