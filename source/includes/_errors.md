# Errors

<aside class="notice">
This error section is stored in a separate file in <code>includes/_errors.md</code>. Slate allows you to optionally separate out your docs into many files...just save them to the <code>includes</code> folder and add them to the top of your <code>index.md</code>'s frontmatter. Files are included in the order listed.
</aside>

Provide API use the following error codes:


Error Code | Meaning
---------- | -------
200 | OK -- Invoked `contract` method does not modify state.
202 | Accepted -- Request has been accepted for asynchronous processing.
204 | No Content -- Microservice instance is up and ready. Request away!
401 | Unauthorized -- The `bearer` token does not resolve to an application.
404 | Not Found -- Microservice instance is unavailable.
