# Freedoms
Freedoms is Simply and Powerful PHP Class


Project : https://gitlab.com/adyoi/freedoms

Repository : https://gitlab.com/adyoi/freedoms.git

```
Frontend: http://freedoms.pe.hu
user : demo
pass : demo

Backend : http://freedoms.pe.hu/admin
user : admin
pass : admin
```

### Directory Tree Structure

```
Freedoms
		|
		└-- app
		|	|
		|	└-- assets
		|	|	|
		|	|	└-- dist (Backend)
		|	|	|	|
		|	|	|	└-- css
		|	|	|	└-- img
		|	|	|	└-- js
		|	|	|	
		|	|	└-- main (Frontend)
		|	|	|	└-- css
		|	|	|	└-- fonts
		|	|	|	└-- images
		|	|	|	└-- js
		|	|	|
		|	|	└-- plugins
		|	|		|
		|	|		└-- (JQuery etc.)
		|	|
		|	└-- libs
		|	|	|
		|	|	└-- (PHP Library etc.)
		|	|
		|	└-- public (Controller)
		|	|	|
		|	|	└-- admin (Backend View and Menu)
		|	|	|	|
		|	|	|	└-- account
		|	|	|	└-- dashboard
		|	|	|	└-- user
		|	|	|
		|	|	└-- index (Frontend View)
		|	|	
		|	└-- template
		|
		└-- config
		└-- engine
```

### System Schema
```
Frontend :
Start --> Error Handler --> Autoload --> Route --> Controller --> Template --> View 

Backend :
Start --> Error Handler --> Autoload --> Route --> Controller --> Template --> Authorize --> View

```


### Controller Installation
```
<?php

/* 
 *	Freedoms version 0.0.1
 */
 
namespace Freedoms
{
	class Index
	{
		public function __construct()
		{	
			AutoLoad :: load('engines\Render');
		}
		
		public static function index()
		{
			$data["baseurl"] = Routes :: baseurl();
			Render :: page('index', $data);
		}
	
		public static function param ($arg)
		{	
			print_r ($arg);
		}
		
		public static function greets ($msg)
		{
			print $msg;
		}
		
	}
	if(!defined('names')) exit('forbidden access');
}
```

### Terms and Conditions of Use

Freedoms PHP Class by Adi Apriyanto is licensed under a Creative Commons Attribution-NonCommercial 4.0 International License.
