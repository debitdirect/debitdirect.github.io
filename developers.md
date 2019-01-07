[Home](/) - [Getting Started](/getting-started) - [Developers](/developers)

## API

### Getting Started

There are a few key parts to an integration with the API - you can do one, two or all three of them:

* Setting up mandates with your creditors bank accounts
* Collecting payments against your mandates
* Staying up-to-date with changes using webhooks

This guide will help you get started with the API.

### Making requests
The base URLs for the DebitDirect API is - https://api.debitdirect.io/ for live. The API is only available over HTTPS. Attempting to access the API over an unsecured HTTP connection will return a an error.

### Authentication
You must provide a valid API token in the Authorization request header (using the basic authentication scheme) when making API requests. Use the API Token as username and provide an empty password for the request.

`Authorization: Basic base64({APITOKEN}:)`

### Media types
All requests and responses are JSON-formatted and UTF-8 encoded. An Accept header is required for all requests, for example:

`Accept: application/json`
`Content-Type: application/json`

A Content-Type and Content-Length header must be given when sending data to the API (using POST and PUT endpoints), for example:

`Content-Type: application/json`
`Content-Length: 104`

For the Accept and Content-Type headers, you may give either the standard JSON MIME type (application/json), or the JSON-API variant (application/vnd.api+json).

You will receive an error if you attempt to make a POST/PUT request without one of these media types.

In the case of a missing Content-Length header, you will receive an Error 411 (Length Required) error message. Although, the majority of HTTP clients should send the header by default.

### Time zones / dates
All date/time are formatted as ISO8601 with timezone information. For API calls that allow for a date/time to be specified, we use that exact date/time. These date/times look something like 2018-06-22T11:21:43.123Z.

### Response Codes
DebitDirect return the following response codes:

| Code | Response |
|---|---|
| 200 | OK. The request has succeeded |
| 201 | Created. Returned upon creating new entities, mainly POST. |
| 204 | No content. Returned upon updating entities, mainly PUT and DELETE. |
| 401 | Unauthorized. The client has not provided a valid Authentication HTTP header or the user making the request has been disabled. |
| 403 | Forbidden. The client has provided a valid Authentication header, but does not have permission to access this resource. |
| 404 | Not Found. The requested resource was not found or the authenticated user cannot access the resource. The response body will explain which resource was not found. |
| 500 | Internal Server Error. The server encountered an error while processing your request and failed. DebitDirect will be alerted on this issue. |

## Core Resources

## Webhooks
