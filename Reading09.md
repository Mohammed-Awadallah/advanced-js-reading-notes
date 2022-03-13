# Reading09

## QUESTIONS :




- What header(s) are used in authentication and authorization

>Authorization request header can be used to provide credentials that authenticate a user agent with a server, allowing access to a protected resource.
>If a client makes a request for which the server expects authentication information, the server sends an HTTP response with a 401 status code, a reason phrase indicating an authentication error, and a WWW-Authenticate header. Most web clients handle this response by requesting a user ID and password from the end user.

- What is safe to put into a JWT
>Only the server should know the "secret" that is used to generate the JWT. If someone modifies the data contained in the JWT, the server will fail to decode it. So the server can trust any JWT that it can decode.
However, if a hacker got access to your computer, they could see the JWT that is stored in the browser and use it. This same threat exists w/cookies, so it's not really a flaw of the JWT.
One way to mitigate this threat is the expiration date of the JWT. For a banking app, your JWT might expire after a few minutes. For Facebook, it might expire after a few months. However, there's no bullet proof solution to this if someone gets access to your browser.
Another approach for hackers would be a "man in the middle" attack to intercept the network traffic between client and server and get at the cookie/JWT. The cookie/JWT should always be sent over HTTPS to prevent this.
- How are JWTs validated
>JWTs are signed so they can't be modified in transit. When an authorization server issues a token, it signs it using a key. When the client receives the ID token, the client validates the signature using a key as well.
 When you make a claim using a JWT, it's signed off by a server that has a secret key. The server reading the key can easily verify that the claim is valid, even without knowing the secret that was used.

## Terms



RBAC

Role-based access control refer to the levels of access that employees have to the network. Employees are only allowed to access the information necessary to effectively perform their job duties. Access can be based on several factors, such as authority, responsibility, and job competency

User Roles

permission sets that control access to areas and features within the Professional Archive Platform. Each User account requires a Role assignment.

JWT Token

a proposed Internet standard for creating data with optional signature and/or optional encryption whose payload holds JSON that asserts some number of claims. The tokens are signed either using a private secret or a public/private key.

## Preview

-   Which 3 things had you heard about previously and now have better clarity on?

> RBAC, User Roles, JWT Token

-   Which 3 things are you hoping to learn more about in the upcoming lecture/demo?

> 

-   What are you most excited about trying to implement or see how it works?

