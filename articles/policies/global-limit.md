---
title: Global Rate Limit Policy For Authentication API
description: This page details Authentication API Rate Limit Policy for free subscribers
toc: true
topics:
    - auth0-policies
    - rate-limits
    - testing
contentType:
  - reference
useCase:
  - support
---
# Authentication API: Global Rate Limit Policy
To ensure the quality of Auth0's services, the Authentication API is subject to several levels of rate limiting.

This document describes the global rate limiting policy applicable to __free tenants__. Please visit [Rate limits](policies/rate-limits) for more information on other applicable limits.

## Limits
For all __free tenants__, Authentication API usage is restricted to __300 requests per minute__.

It is important to consider that the limit is set globally by tenant and not by endpoint.

### Affected endpoints
The global rate limit applies to all the [Authentication API](/api/authentication) endpoints, below you will find a complete list of endpoints that are affected by this limit and the associated response in case the rate limit is exceeded.

Endpoint | Response
---------|---------
`GET /authorize` |  [Error Page](#error-page)
`GET /passwordless/verify_redirect` |  [Error Page](#error-page)
`POST /dbconnections/change_password` | [JSON Error](#json-error) (`too_many_requests`)
`GET /dbconnections/change_password` | [JSON Error](#json-error) (`too_many_requests`)
`POST /dbconnections/self_change_password` | [JSON Error](#json-error) (`too_many_requests`)
`POST /co/authenticate` |  [JSON Error](#json-error) (`access_denied`)
`POST /delegation` | [JSON Error](#json-error) (`too_many_requests`)
`GET /delegation` | [JSON Error](#json-error) (`too_many_requests`)
`GET /activate` | [Error Page](#error-page)
`POST /activate` | [Error Page](#error-page)
`POST /oauth/device/code` |  [JSON Error](#json-error) (`access_denied`)
`POST /oauth/ro` |  [JSON Error](#json-error) (`access_denied`)
`GET /oauth/ro` |  [JSON Error](#json-error) (`access_denied`)
`POST /oauth/token` |  [JSON Error](#json-error) (`access_denied`)
`POST /oauth/introspect` |  [JSON Error](#json-error) (`access_denied`)
`GET /passwordless/start` | [JSON Error](#json-error) (`too_many_requests`)
`POST /passwordless/start` | [JSON Error](#json-error) (`too_many_requests`)
`POST /u/reset-password/request/:connection` | [Error Page](#error-page)
`GET /u/consent` | [Error Page](#error-page)
`POST /u/consent` | [Error Page](#error-page)
`GET /u/login` | [Error Page](#error-page)
`POST /u/login` | [Error Page](#error-page)
`GET /u/mfa-country-codes` | [Error Page](#error-page)
`POST /u/mfa-country-codes` | [Error Page](#error-page)
`GET /u/mfa-email-challenge` | [Error Page](#error-page)
`POST /u/mfa-email-challenge` | [Error Page](#error-page)
`GET /u/mfa-email-enrollment` | [Error Page](#error-page)
`POST /u/mfa-email-enrollment` | [Error Page](#error-page)
`GET /u/mfa-email-enrollment-verify` | [Error Page](#error-page)
`POST /u/mfa-email-enrollment-verify` | [Error Page](#error-page)
`GET /u/mfa-email-list` | [Error Page](#error-page)
`POST /u/mfa-email-list` | [Error Page](#error-page)
`GET /u/mfa-enroll-options` | [Error Page](#error-page)
`POST /u/mfa-enroll-options` | [Error Page](#error-page)
`GET /u/mfa-guardian-list` | [Error Page](#error-page)
`POST /u/mfa-guardian-list` | [Error Page](#error-page)
`GET /u/mfa-guardian-welcome` | [Error Page](#error-page)
`POST /u/mfa-guardian-welcome` | [Error Page](#error-page)
`GET /u/mfa-login-options` | [Error Page](#error-page)
`POST /u/mfa-login-options` | [Error Page](#error-page)
`GET /u/mfa-otp-challenge` | [Error Page](#error-page)
`POST /u/mfa-otp-challenge` | [Error Page](#error-page)
`GET /u/mfa-otp-enrollment` | [Error Page](#error-page)
`POST /u/mfa-otp-enrollment` | [Error Page](#error-page)
`GET /u/mfa-push-challenge` | [Error Page](#error-page)
`POST /u/mfa-push-challenge` | [Error Page](#error-page)
`GET /u/mfa-push-enrollment` | [Error Page](#error-page)
`POST /u/mfa-push-enrollment` | [Error Page](#error-page)
`GET /u/mfa-recovery-code-challenge` | [Error Page](#error-page)
`POST /u/mfa-recovery-code-challenge` | [Error Page](#error-page)
`GET /u/mfa-recovery-code-challenge-new-code` | [Error Page](#error-page)
`POST /u/mfa-recovery-code-challenge-new-code` | [Error Page](#error-page)
`GET /u/mfa-recovery-code-enrollment` | [Error Page](#error-page)
`POST /u/mfa-recovery-code-enrollment` | [Error Page](#error-page)
`GET /u/mfa-sms-challenge` | [Error Page](#error-page)
`POST /u/mfa-sms-challenge` | [Error Page](#error-page)
`GET /u/mfa-sms-enrollment` | [Error Page](#error-page)
`POST /u/mfa-sms-enrollment` | [Error Page](#error-page)
`GET /u/mfa-sms-enrollment-verify` | [Error Page](#error-page)
`POST /u/mfa-sms-enrollment-verify` | [Error Page](#error-page)
`GET /u/mfa-sms-list` | [Error Page](#error-page)
`POST /u/mfa-sms-list` | [Error Page](#error-page)
`GET /u/reset-password` | [Error Page](#error-page)
`POST /u/reset-password` | [Error Page](#error-page)
`GET /u/reset-password/request/:connection` | [Error Page](#error-page)
`GET /u/signup` | [Error Page](#error-page)
`POST /u/signup` | [Error Page](#error-page)
`GET /tokeninfo` | Text: "Rate limit exceed"
`POST /tokeninfo` | Text: "Rate limit exceed"
`POST /userinfo` | Text: "Rate limit exceed"
`GET /userinfo` | Text: "Rate limit exceed"
`POST /usernamepassword/login` | [JSON Error](#json-error) (`too_many_requests`)
`GET /usernamepassword/login` | [JSON Error](#json-error) (`too_many_requests`)
`GET /.well-known/jwks.json` | Text: "Rate limit exceed"
`GET /.well-known/openid-configuration` |  [JSON Error](#json-error) (`access_denied`)
`GET /cer/:clientID?` | Text: "Rate limit exceed"
`GET /pb7/:clientID?` | Text: "Rate limit exceed"
`GET /pem/:clientID?` | Text: "Rate limit exceed"
`GET /rawpem/:clientID?` | Text: "Rate limit exceed"
`GET /:tenant_ignored?/samlp/:clientID` | Text: "Rate limit exceed"
`POST /:tenant_ignored?/samlp/:clientID` | Text: "Rate limit exceed"
`GET /:tenant_ignored?/samlp/metadata` | Text: "Rate limit exceed"
`GET /:tenant_ignored?/samlp/metadata/:clientID` | Text: "Rate limit exceed"
`GET /:clientID/trust/mex` | XML Error (`wst:RequestFailed`)
`POST /:clientID/trust/usernamemixed` | XML Error (`wst:RequestFailed`, Status Code: 500)
`GET /decision` | [Error Page](#error-page)
`POST /decision` | [Error Page](#error-page)
`POST /drwatson` | Text: "Rate limit exceed"
`POST /mfa/associate` |  [JSON Error](#json-error) (`access_denied`)
`GET /mfa/authenticators` |  [JSON Error](#json-error) (`access_denied`)
`DELETE /mfa/authenticators/:authenticator_id` |  [JSON Error](#json-error) (`access_denied`)
`POST /mfa/challenge` |  [JSON Error](#json-error) (`access_denied`)
`GET /oauth/access_token` |  [JSON Error](#json-error) (`access_denied`)
`POST /oauth/access_token` |  [JSON Error](#json-error) (`access_denied`)
`GET /p/:strategy/:ticket` | Text: "Rate limit exceed"
`POST /p/:strategy/:ticket` | Text: "Rate limit exceed"
`GET /p/:strategy/:ticket/info` | Text: "Rate limit exceed"
`GET /passwordless/verify` | [JSON Error](#json-error) (`too_many_requests`)
`POST /passwordless/verify` | [JSON Error](#json-error) (`too_many_requests`)
`GET /rms` | [Error Page](#error-page)
`GET /rms/:clientID/adfs/fs/federationserverservice.asmx` | XML Error (`fed:BadRequest`)
`POST /rms/:clientID/adfs/fs/federationserverservice.asmx` | XML Error (`fed:BadRequest`)
`GET /rms/:clientID/FederationMetadata/2007-06/FederationMetadata.xml` | [JSON Error](#json-error) (`too_many_requests`)
`GET /samlp/:clientID/logout` | [Error Page](#error-page)
`POST /samlp/:clientID/logout` | [Error Page](#error-page)
`GET /samlp/idp/slo` | Text: "Rate limit exceed"
`GET /sso_dbconnection_popup/:clientID` |  [JSON Error](#json-error) (`access_denied`)
`GET /wsfed` | [Error Page](#error-page)
`GET /wsfed/:clientID` | [Error Page](#error-page)
`GET /wsfed/:clientID/FederationMetadata/2007-06/FederationMetadata.xml` | [Error Page](#error-page)
`GET /wsfed/FederationMetadata/2007-06/FederationMetadata.xml` | [Error Page](#error-page)
`GET /.well-known/apple-app-site-association` |  [JSON Error](#json-error) (`access_denied`)
`GET /.well-known/assetlinks.json` |  [JSON Error](#json-error) (`access_denied`)
`GET /adfs/fs/federationserverservice.asmx` | XML Error (`fed:BadRequest`)
`POST /adfs/fs/federationserverservice.asmx` | XML Error (`fed:BadRequest`)
`GET /apple-app-site-association` |  [JSON Error](#json-error) (`access_denied`)
`GET /aws-saml/metadata` | Text: "Rate limit exceed"
`GET /changepwd/completed` | [JSON Error](#json-error) (`too_many_requests`)
`GET /changepwd/form` | [Error Page](#error-page)
`POST /changepwd/reset` | [JSON Error](#json-error) (`too_many_requests`)
`POST /co/verify` | Text: "Rate limit exceed"
`GET /continue` | [Error Page](#error-page)
`POST /continue` | [Error Page](#error-page)
`GET /custom-login/preview` | [JSON Error](#json-error) (`too_many_requests`)
`POST /dbconnections/delete` | [JSON Error](#json-error) (`too_many_requests`)
`GET /dbconnections/login` | [JSON Error](#json-error) (`too_many_requests`)
`POST /dbconnections/login` | [JSON Error](#json-error) (`too_many_requests`)
`GET /dbconnections/signup` | [JSON Error](#json-error) (`too_many_requests`)
`POST /dbconnections/signup` | [JSON Error](#json-error) (`too_many_requests`)
`POST /dbconnections/verify_email` | [JSON Error](#json-error) (`too_many_requests`)
`GET /FederationMetadata/2007-06/FederationMetadata.xml` | XML Error (`fed:BadRequest`)
`GET /i/login` | [Error Page](#error-page)
`GET /i/login/sso/:provider` | Text: "Rate limit exceed"
`GET /i/oauth2/authorize` |  [JSON Error](#json-error) (`access_denied`)
`GET /login` | [Error Page](#error-page)
`GET /login/callback` | [Error Page](#error-page)
`POST /login/callback` | [Error Page](#error-page)
`GET /logout` | [Error Page](#error-page)
`POST /logout` | [Error Page](#error-page)
`GET /mf` | [Error Page](#error-page)
`POST /mf` | [Error Page](#error-page)
`POST /oauth/reverse` |  [JSON Error](#json-error) (`access_denied`)
`POST /oauth/revoke` |  [JSON Error](#json-error) (`access_denied`)
`POST /state/introspect` | [JSON Error](#json-error) (`too_many_requests`)
`GET /unblock` | [Error Page](#error-page)
`POST /unlink` | [JSON Error](#json-error) (`too_many_requests`)
`GET /user/ssodata` | Text: "Rate limit exceed"
`GET /users/:id/impersonate` | [JSON Error](#json-error) (`too_many_requests`)
`POST /users/:id/impersonate` | [JSON Error](#json-error) (`too_many_requests`)
`GET /v2/logout` | [Error Page](#error-page)

## Exceeding the Rate Limit
If you exceed the provided rate limit for a given API endpoint, you will receive a response with [HTTP Status Code 429 (Too Many Requests)](http://tools.ietf.org/html/rfc6585#section-4) except for the cases documented above. The response will also contain the [HTTP Response Headers](policies/rate-limits#http-response-headers) which you can refer to for more information on the rate limits applicable to that endpoint.

### Response body
The response body depends on the endpoint and, in particular, the response the endpoint was meant to render originally. For example, if the response was meant to render JSON, then a JSON error response will be sent.

The particular response per endpoint is stated in [Affected endpoints](#affected-endpoints) section, below you will find a description for each case.

#### Error Page
This response is sent for endpoints that render HTML content to the end user. When the rate limit is exceeded the [Error Page](https://auth0.com/docs/universal-login/custom-error-pages) will be rendered instead of the usual content.

#### JSON Error
JSON formatted response containing error code and description.
The error code depends on the endpoint:
* `access_denied`: for endpoints associated with OAuth
* `too_many_requests`: for the rest of endpoints that return JSON.

```json
{
  "error": "access_denied or too_many_requests",
  "error_description": "Global rate limit exceeded",
  "error_uri": "https://.../... documentation url"
}
```

#### XML Error
This response is redered for endpoints that normally return XML.
The error code depends on the endpoint:
- `fed:BadRequest` will be sent for WSFED-related endpoints.
- `wst:RequestFailed` will be used in for WSTrust-related endpoints.

```xml
<env:Envelope xmlns:env="http://www.w3.org/2003/05/soap-envelope" ...>
 <env:Body>
  <env:Fault>
   <env:Code>
     <env:Value>env:Sender</env:Value>
     <env:Subcode>
      <env:Value>fed:BadRequest or wst:RequestFailed</env:Value>
     </env:Subcode>
   </env:Code>
   <env:Reason>
     <env:Text xml:lang="en">Global rate limit exceeded</env:Text>
   </env:Reason>
   <env:Detail>
   </env:Detail>
  </env:Fault>
 </env:Body>
</env:Envelope>
```

## FAQ

#### How do I know if I have exceeded the rate limit?
For every hour when the global rate limit is exceeded you will find a log with description: "You have reached the global limit for your account." written to your account logs.

You can search for them from the [Dashboard](${manage_url}#/logs). If you see one of those logs it means you have exceeded the rate limit at least once.

#### I am exceeding the rate limit. How can I reduce my call rate to Auth0?
Whereas the exact answer depends on your use case, there are some common patterns you can follow in many cases to reduce the call rate:
- Cache `/.well-known/*` information: this information does not change frequently, you can usually cache it to reduce call rate to Auth0.
- If your use case allows it, consider requesting an `id_token` instead of calling `/userinfo` to get information about the user.