```php
<?php
    if ( function_exists( 'mysqli_connect' ) ) {
			if ( defined( 'USE_EXT_MYSQL' ) ) {
				$use_mysqli = ! WP_USE_EXT_MYSQL;
			} elseif ( version_compare( phpversion(), '5.5', '>=' ) || ! function_exists( 'mysql_connect' ) ) {
				$use_mysqli = true;
			} elseif ( false !== strpos( $GLOBALS['wp_version'], '-' ) ) {
				$use_mysqli = true;
			}
		}
```
