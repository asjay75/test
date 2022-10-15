
## Installation

### With Docker

```
docker-compose up
```

```json
http://localhost:4000/flight/11-01-2022/DXB/LHR/

Date : MM-DD-YYYY
```

```php
<?php
require 'vendor/autoload.php';

use Carbon\Carbon;

printf("Now: %s", Carbon::now());
```

### Without Docker

Why are you not using [composer](https://getcomposer.org/)? Download the Carbon [latest release](https://github.com/briannesbitt/Carbon/releases) and put the contents of the ZIP archive into a directory in your project. Then require the file `autoload.php` to get all classes and dependencies loaded on need.

```php
<?php
require 'path-to-Carbon-directory/autoload.php';

use Carbon\Carbon;

printf("Now: %s", Carbon::now());
```


### Varnish(Cache service)

- All Requests, except authorize call from Client to API service goes via Varnish
- Varnish will Cache all the response from API service depending on the cache-control(max-age) set on the response header.



### Flight Service

- Client will call API service to get the JWT token .
- API service will make  asynchronous   calls to 5 downstream services to get the Flight Data for the input provided .
- Flight Number is Returned  to Client.






![flight4](https://user-images.githubusercontent.com/24268967/195989367-66d64457-aad2-4cb4-bdbf-47b86102a6c9.png)



### Price Service

- Client will call API service to get the JWT token .
- API service will execute Complex Rule Engine [Json Rule Engine] to fetch the price for the input data.
- Since the Rule Engine Data , the Data is stored in Application memory (Singleton Object) .
- Price Data is returned to the Client



![pricing](https://user-images.githubusercontent.com/24268967/195988103-58cc5573-daf0-4aac-882d-c56e37a95cdd.png)




###  Service at Scale


## High availably setup 

- Two AWS Region is considered 
- Each region , Two Availability Zone is Considered .
- Cluster Database is setup across each region .

## Akamai Edge Solution is Considered 


- Edge servers automatically drop network-layer DDoS attacks and protect the application layer from DDoS and application attacks. 
- Stop traffic from malicious actors based on their specific reputation score, which is derived from Akamai’s visibility into prior behavior of their IP addresses. 
- Automatically inspect API requests for malicious content and block attack tools based on device fingerprinting. 
- SSL/TLS encryption to prevent sensitive data exposure during transmission
- API Gateway validates API requests to ensure legitimate consumers can access APIs. 
- API responses can be served from cache to improve performance and reduce infrastructure and bandwidth costs. 
- Capture, retain, and deliver security information and events to your SIEM application in real time





<img width="1068" alt="fourth" src="https://user-images.githubusercontent.com/24268967/195988136-7ff4d1c1-13b8-45b2-9fb3-44f414da88fe.png">
