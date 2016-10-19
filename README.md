# Memcache Object Cache

## Installation

1. Install [memcached](http://danga.com/memcached) on at least one server. Note the connection info. The default is `127.0.0.1:11211`.

1. Install the [PECL memcache extension](http://pecl.php.net/package/memcache)

1. Copy object-cache.php to wp-content

## Frequently Asked Questions

**How can I manually specify the memcached server(s)?**

Add something similar to the following to wp-config.php above:

```
$memcached_servers = array(
	'default' => array(
		'10.10.10.20:11211',
		'10.10.10.30:11211'
	)
);
```

## How to run tests locally

```
cd {memcache-object-cache folder}
composer install
bin/install-wp-tests.sh wordpress_test root root wp-rwdbhost latest
vendor/bin/phpunit
```
