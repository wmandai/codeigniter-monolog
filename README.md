Codeigniter-Monolog
===================

Simple integration of the Monolog Package (https://github.com/Seldaek/monolog) into CodeIgniter by overwriting the CI_Log class.

Based on https://github.com/stevethomas/codeigniter-monolog, but added support for slack and Sentry

This library registers Monolog as the PHP error handler to catch all errors and adds support for IntrospectionProcessor for additional meta data.

Supports File (RotatingFileHandler), New Relic (NewRelicHandler), Slack (SlackWebhookHandler), Sentry (RavenHandler) and HipChat (HipChatHandler).

Installation
------------
* Install monolog with ```composer require monolog/monolog```
* To use Sentry install it with ```composer require sentry/sentry```
* Make sure your index.php contains  ```include_once './vendor/autoload.php';```
* Copy application/core/MY_Log.php to application/core folder
* Copy application/config/monolog.php into your CodeIgniter application/config folder

Usage
-----
Use log_message() as per normal in CodeIgniter to log error, debug and info messages. Log files are stored in the application/logs folder in format ci-YYYY-MM-DD.log

License
-------

codeigniter-monolog is licensed under the MIT License - see the LICENSE file for details
