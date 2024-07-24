Определение:
	The OAuth 2.0 authorization framework enables a third-party
	application to obtain limited access to an HTTP service, either on
	behalf of a resource owner by orchestrating an approval interaction
	between the resource owner and the HTTP service, or by allowing the
	third-party application to obtain access on its own behalf.

OAuth defines four roles:

   `resource owner`
      An entity capable of granting access to a protected resource.
      When the resource owner is a person, it is referred to as an
      end-user.

   `resource server`
      The server hosting the protected resources, capable of accepting
      and responding to protected resource requests using access tokens.

   `client` (backend system)
      An application making protected resource requests on behalf of the
      resource owner and with its authorization. The term "client" does
      not imply any particular implementation characteristics (e.g.,
      whether the application executes on a server, a desktop, or other
      devices).

   `authorization server`
      The server issuing access tokens to the client after successfully
      authenticating the resource owner and obtaining authorization.

## Client perspective:
The Authorization Code Grant Flow
![[authCodeGrant.png]]
How the user sees it
![[userAuthCodeGrant.png]]

Client credentials grant
- direct access by the client application
- access token obtained using client credentials 
Authorization code grant
- delegated access to a backend application
- access token obtained by exchanging code with client credentials
- refresh token can be used with client credentials
Implicit grant
- delegated access to a frontend application
- access token directly obtained through the redirect
- not supposed to have access to refresh tokens

## Refs
1. [спецификация](https://www.rfc-editor.org/rfc/rfc6749#section-1.1)
2. ролик на [youtube](https://www.youtube.com/watch?v=GyCL8AJUhww&t=213s&ab_channel=GOTOConferences) с прекрасной [презентацией](https://files.gotocon.com/uploads/slides/conference_12/653/original/20181101%20-%20Introduction%20to%20OAuth%202.0%20and%20OpenID%20Connect.pdf)
