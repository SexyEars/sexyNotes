**Self-contained tokens** are using a protected, time-limited data structure that contains metadata and claims to communicate the identity of the user or client over the wire. A popular format would be JSON Web Tokens (JWT). The recipient of a self-contained token can validate the token locally by checking the signature, expected issuer name and expected audience or scope.

Self-contained tokens
- the token itself contains the metadata used by the authorization server
- stored on the client, so out of reach from the authorization server
- can be used independently by the resource server after integrity check
- hard or impossible to revoke

**Reference tokens** (sometimes also called opaque tokens) on the other hand are just identifiers for a token stored on the token service. The token service stores the contents of the token in some data store, associates it with an infeasible-to-guess id and passes the id back to the client. The recipient then needs to open a back-channel to the token service, send the token to a validation endpoint, and if valid, retrieves the contents as the response.

Reference tokens
- an identifier pointing to metadata kept by the authorization server
- authorization server retains full control over the metadata
- require a backchannel request when received by the resource server
- easy to revoke if needed

Token Introspection ???