# REST API Design Cheat Sheet

##  Copyright 

All the contents are from the book  "REST API Design Rulebook" .
All rights reserved by the author and publisher

## Design Rules

### URI Format

* Forward slash separator (/) must be used to indicate a hierarchicalrelationship 
* A trailing forward slash (/) should not be included in URIs
* Hyphens (-) should be used to improve the readability of URIs
* Underscores (_) should not be used in URIs
* Lowercase letters should be preferred in URI paths
* File extensions should not be included in URIs
### URI Authority Design
* Consistent subdomain names should be used for your APIs
* Consistent subdomain names should be used for your client developer portal
### URI Path Design
* A singular noun should be used for document names
* A plural noun should be used for collection names
* A plural noun should be used for store names
* A verb or verb phrase should be used for controller names
* Variable path segments may be substituted with identity-basedvalues
* CRUD function names should not be used in URIs
### URI Query Design
* The query component of a URI may be used to filter collections or stores
* The query component of a URI should be used to paginate collection or store results
### Request Methods
* GET and POST must not be used to tunnel other request methods
* GET must be used to retrieve a representation of a resource
* HEAD should be used to retrieve response headers
* PUT must be used to both insert and update a stored resource
* PUT must be used to update mutable resources
* POST must be used to create a new resource in a collection
* POST must be used to execute controllers
* DELETE must be used to remove a resource from its parent
* OPTIONS should be used to retrieve metadata that describes a resource’s available interactions
### Response Status Codes
* 200 (“OK”) should be used to indicate nonspecific success
* 200 (“OK”) must not be used to communicate errors in the response body
* 201 (“Created”) must be used to indicate successful resource creation
* 202 (“Accepted”) must be used to indicate successful start of anasynchronous action
* 204 (“No Content”) should be used when the response body isintentionally empty
* 301 (“Moved Permanently”) should be used to relocate resources
* 302 (“Found”) should not be used
* 303 (“See Other”) should be used to refer the client to a different URI
* 304 (“Not Modified”) should be used to preserve bandwidth
* 307 (“Temporary Redirect”) should be used to tell clients to resubmit the request to another URI
* 400 (“Bad Request”) may be used to indicate nonspecific failure
* 401 (“Unauthorized”) must be used when there is a problem with the client’s credentials
* 403 (“Forbidden”) should be used to forbid access regardless ofauthorization state
* 404 (“Not Found”) must be used when a client’s URI cannot be mapped to a resource
* 405 (“Method Not Allowed”) must be used when the HTTP method is not supported
* 406 (“Not Acceptable”) must be used when the requested media type cannot be served
* 409 (“Conflict”) should be used to indicate a violation of resource state
* 412 (“Precondition Failed”) should be used to support conditionaloperations
* 415 (“Unsupported Media Type”) must be used when the media type of a request’s payload cannot be processed
* 500 (“Internal Server Error”) should be used to indicate APImalfunction
### HTTP Headers
* Content-Type must be used
* Content-Length should be used
* Last-Modified should be used in responses
* ETag should be used in responses
* Stores must support conditional PUT requests
* Location must be used to specify the URI of a newly created resource
* Cache-Control, Expires, and Date response headers should be used to encourage caching
* Cache-Control, Expires, and Pragma response headers may be used to discourage caching
* Caching should be encouraged
*  Expiration caching headers should be used with 200 (“OK”) responses
* Expiration caching headers may optionally be used with 3xx and 4xx responses
* Custom HTTP headers must not be used to change the behavior ofHTTP methods
### Media Type Design
* Application-specific media types should be used
* Media type negotiation should be supported when multiple representations are available
* Media type selection using a query parameter may be supported
### Message Body Format
* JSON should be supported for resource representation
* JSON must be well-formed
* XML and other formats may optionally be used for resourcerepresentation
* Additional envelopes must not be created
### Hypermedia Representation
* A consistent form should be used to represent links
* A consistent form should be used to represent link relations
* A consistent form should be used to advertise links
* A self link should be included in response message bodyrepresentations
* Minimize the number of advertised “entry point” API URIs
* Links should be used to advertise a resource’s available actions in a state-sensitive manner
### Media Type Representation
* A consistent form should be used to represent media type formats
* A consistent form should be used to represent media type schemas
### Error Representation
* A consistent form should be used to represent errors
* A consistent form should be used to represent error responses
* Consistent error types should be used for common error conditions
### Versioning
* New URIs should be used to introduce new concepts
* Schemas should be used to manage representational form versions
* Entity tags should be used to manage representational state versions
### Security
*  OAuth may be used to protect resources
* API management solutions may be used to protect resources
### Response Representation Composition
* The query component of a URI should be used to support partialresponses
* The query component of a URI should be used to embed linkedresources
### JavaScript Clients
* JSONP should be supported to provide multi-origin read access from JavaScript
* CORS should be supported to provide multi-origin read/write access from JavaScript


