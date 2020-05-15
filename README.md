# Dynamic Base URL on Codeigniter 4

If you need make base_ur() dynamic every project with Codeigniter 4, you can config by using this code. 
You need config on 2 files: App.php and Constants.php.

On App.php change $baseUrl value with $baseURL = BASE;

On Constants.php add new line with code bellow:

$base = isset($_SERVER['HTTPS']) && $_SERVER['HTTPS'] != 'off' ? 'https://'.$_SERVER['HTTP_HOST'].dirname($_SERVER['SCRIPT_NAME']) : 'http://'.$_SERVER['HTTP_HOST'].dirname($_SERVER['SCRIPT_NAME']);

defined('BASE') || define('BASE', $base);
