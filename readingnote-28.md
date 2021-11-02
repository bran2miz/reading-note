# Reading 14 - Authentication

## What is OAuth

1.What is OAuth?
  **OAuth** is an *open standard authorization protocol*, allowing servers and services access without releasing any personal logon "credentials".

2. Give an example of what using OAuth would look like.
  ie when there are multiples times in which the user can log on using another website's logon.

3. How does OAuth work? What are the steps that it takes to authenticate the user?
  a.Upon given user's credentials, the first website connects to the second website.
  b.Second site creates a token to all parties involved.
  c.First site gives token to client software.
  d.Request token is shown by the client software privately to the authorization provider.
  e.User given token to first website.
  f.First website gives access token to second website.
  g.Second website allows first website access to the site.

4. What is OpenID?
  OpenID is authentication essentially for "humans" to log on into "machines".

## Authorization and Authentication flows

1. What is the difference between authorization and authentication?
  Authentication **verifies** who a user is, authorization **verifies** what they have access to.

2. What is Authorization Code Flow?
  Trades Authorization code for an access token.

3. What is Authorization Code Flow with Proof Key for Code Exchange (PKCE)?
  Calling application creates a **secret** that potentially can be verified by authorization server.

4. What is Implicit Flow with Form Post?
  With the help of **OpenId Connect(OIDC)**, Implicit Flow with Form Post implements web sign-in, without having to obtain, maintain, use, and protect a secret in the app.
5. What is Client Credentials Flow?
  Pass Client ID and secret to authenticate oneself and receive a token.
6. What is Device Authorization Flow?
  Device passes along Client ID and secret to authenticate oneself and receive a token.
7. What is Resource Owner Password Flow?
  Not recommended, but request user to provide credentials with an interactive *form*.

## Things I want to know more about

**secrets**

[<==BACK](README.md)
