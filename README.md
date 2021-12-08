# symfony5-readable-docs

1. How to get list of available routes:

Run this command inside your symfony project root folder

`php bin/console debug:router`

2. How to generate url to route inside functional test

https://symfony.com/doc/current/testing.html#making-requests

`
Hardcoding the request URLs is a best practice for application tests. If the test generates URLs using the Symfony router, it won't detect any change made to the application URLs which may impact the end users.
`
