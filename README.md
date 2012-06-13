NameTerrific API Documentation
==============================

NameTerrific API is a RESTful API using JSON for data serialization. Developers can utilize NameTerrific API to read and write domain name information and DNS records.

This documentation will outline the usage of all API actions with actual examples.

Available API
-------------

* [Domains](https://github.com/nameterrific/api/blob/master/domains.md)
* [Records](https://github.com/nameterrific/api/blob/master/records.md)
* [Profiles](https://github.com/nameterrific/api/blob/master/profiles.md)

Endpoint and URIs
-----------------

NameTerrific API URIs start with `https://www.nameterrific.com/api/`, followed by version identifier, such as `v1`.

Resources, actions and/or IDs will follow in a RESTful style and logical order.

SSL is required for all API requests. 

### Example URI
`
https://www.nameterrific.com/api/v1/domains/1.json
`

Authentication
--------------

NameTerrific provides two types of authentication system: HTTP Basic and OAuth 2. Depending on your needs, you can choose either if you are building an application for yourself. However, if your application uses someone else's NameTerrific account, you must use OAuth 2, and you should never ask your users for account credentials.

Read more on [Authentication](#)


Rate Limiting
-------------

Currently NameTerrific does not rate-limit your application. However you should use HTTP caching as much as possible to reduce delays for your application.

Error Handling
--------------

All normal requests should return either `200 OK` or `204 No Content` depending on the request type.

### 401 Unauthorized
If you get a `401 Unauthorized` error, it means that you do not have the privilege to access the resource and/or the action. 

**If you are using HTTP Basic Authentication**, check your email and password and make sure they are correct.

**If you are using OAuth**, make sure the access token is valid, and also the scopes of access are correctly requested.

### 404 Not Found
You will receive `404 Not Found` when the URI you are accessing does not exist, or out of privilege (such a domain name that does not belong to the authenticated user).

### 500 Internal Server Error
Under normal circumstances, you should not be getting this error. If you experience any technical difficulties interacting with NameTerrific API, you can create a ticket in [Issues](https://github.com/nameterrific/api/issues).

3rd Party Libaries
------------------

We will list some 3rd party libaries of various programming languages here.

Improving this documentation
----------------------------

You're welcome to fork this documentation and send pull requests to contribute to NameTerrific API Documentation. If you find any errors in the documentation or any bugs with the API itself, you can use [Issues](https://github.com/nameterrific/api/issues).
