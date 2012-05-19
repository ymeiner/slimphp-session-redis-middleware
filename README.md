slimphp-redis-session-middleware
================================

Middleware to use Redis as your PHP Session store in SlimPHP

use
================================

```php
$app->add($session = new Slim_Middleware_SessionRedis(array(
	'session.expires'	=> 3600,
	'session.id'		=> $_COOKIE['session_cookie_name'],
	'session.name'		=> 'session_cookie_name'
)));

$app->get('/', function()
use ($app, $session){
	// this will be saved in redis
	$_SESSION['key'] = 'value';
});
```
