# wp-nginx-docker-compose
2021 wordpress

Add to wp-config.php:

define('FORCE_SSL_ADMIN', true);
if ($_SERVER['HTTP_X_FORWARDED_PROTO'] == 'https')
 $_SERVER['HTTPS']='on';

and in the end of the file:

define('WP_HOME','https://wordpress-docker.test');
define('WP_SITEURL','https://wordpress-docker.test');