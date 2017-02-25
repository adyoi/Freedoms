# Freedoms
Freedoms is Simply and Powerful PHP Class
```
Project
-------
link : https://gitlab.com/adyoi/freedoms

Repository
----------
link : https://gitlab.com/adyoi/freedoms.git

Live Demo Frontend
------------------
link : http://freedoms.pe.hu
user : demo
pass : demo

Live Demo Backend
-----------------
link : http://freedoms.pe.hu/admin
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
Frontend : Start --> Error Handler --> Autoload --> Route --> Controller --> Template --> View 

Backend : Start --> Error Handler --> Autoload --> Route --> Controller --> Template --> Authorize --> View
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
		var $function = array("greets");
		
		public function __construct()
		{	
			AutoLoad :: load('engines\Render');
		}
		
		public static function index()
		{
			Render :: page('index', null);
		}
	
		public static function param ($arg)
		{	
			print_r ($arg);
		}
		
		public static function greets ($msg)
		{
			echo $msg;
		}
		
	}
	if(!defined('names')) exit('forbidden access');
}
```


### Terms and Conditions of Use

Freedoms PHP Class by Adi Apriyanto is licensed under a Creative Commons Attribution-NonCommercial 4.0 International License.
