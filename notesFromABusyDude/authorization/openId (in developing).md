Conceptual overview of OpenId Connect

![[openIdConnect.png]]

Implicit grant
- identity token is intended for the frontend application
- allows establishing the user's identity in the frontend only
Authorization code grant
- identity token is intended for the backend application
- allows connecting the identity of the user to an internal user concept
Hybrid
- identity token is intended for the backend application
- allows connecting the identity of the user to an internal user concept
- the backend must check if the audience of the token matches its client id