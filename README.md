
## Installation

### With Docker

```
$ composer require nesbot/carbon
```

```json
{
    "require": {
        "nesbot/carbon": "^2.16"
    }
}
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



### Flight Service

Client will call API service to get the JWT token .
API service will make  asynchronous   calls to 5 downstream services to get the Flight Data for the input provided .





![flight4](https://user-images.githubusercontent.com/24268967/195989367-66d64457-aad2-4cb4-bdbf-47b86102a6c9.png)






![pricing](https://user-images.githubusercontent.com/24268967/195988103-58cc5573-daf0-4aac-882d-c56e37a95cdd.png)








**Consuming a RESTful API in React
A simple implementation on how to use a RESTful API in React.

To follow along, this application has been documented as an article on Pusher blog. You can read about it here


















**Consuming Service at Scale
A simple implementation on how to use a RESTful API in React.




<img width="1068" alt="fourth" src="https://user-images.githubusercontent.com/24268967/195988136-7ff4d1c1-13b8-45b2-9fb3-44f414da88fe.png">
