# Clear documentation

---------------------------------------------------------------------------------------------------------------------------------------------------
### How to get list of available routes?

Run this command inside your symfony project root folder

`php bin/console debug:router`

---------------------------------------------------------------------------------------------------------------------------------------------------
### How to generate url to route inside functional test?

https://symfony.com/doc/current/testing.html#making-requests

`
Hardcoding the request URLs is a best practice for application tests. If the test generates URLs using the Symfony router, it won't detect any change made to the application URLs which may impact the end users.
`

---------------------------------------------------------------------------------------------------------------------------------------------------
### How to set headers inside $this->client->request() method in application tests? 

```
$this->client->request(
            'GET', 
            '/url/resource',
            [],
            [],
            [ // server params
                'HTTP_AUTHORIZATION' => 'Bearer token'
            ]
        );
```

---------------------------------------------------------------------------------------------------------------------------------------------------
### How to get 'real' service inside application test

Example for getting jwt encoder service

```
$this->jwtEncoder = static::getContainer()->get('lexik_jwt_authentication.encoder.lcobucci');
```
