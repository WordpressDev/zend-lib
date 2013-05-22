# Zend-lib integration of ZF 1.12 and 2.2 libraries with Codeigniter

## Requirements

* CodeIgniter 2
* [CodeIgniter Sparks](http://getsparks.org/)

## Setup

1. [Install Sparks](http://getsparks.org/install) if you haven't done so already.
2. Install the zend-lib spark (see [here](http://getsparks.org/get-sparks) if you don't know how).

## Info

Zend-lib is a spark that allows the Zend Framework libraries to be loaded into codeiginiter as additional libraries. The list of libraries available come from the Zend Framework version 1.12 and version 2.2.
Most of the available libraries have been tested for correct functionality within codeigniter..

## Usage

### $this->load->spark('my_zend/x.x.x');

To load the my_zend spark..



## ZF Version 2.2

Version 2.2 of the Zend Framework makes use of PHP 5.3 namespace convention. New in version 2.2 of ZF is the autoload_classmap.php which is script created to load all class in the Zend directory.. I have already run the script and the classmap file is located in the Zend directory. It is an assoc array with class names and location of all Zend classes.. This file can be edited to remove classes from becoming available after calling the ZF_loader().


1. $this->my_zend->ZF_Loader();
2. $my_zf2_class = new Zend\package name\class name i.e.($di = new Zend\Di\Di();)

## ZF Version 1.12

Version 1.12 is also available in the zend_1.12 directory and the my_zend loader has been updated. This directory will be deprecated after further testing has been completed with version 2.2

### load('Loader');

Use the my_zend library to load the zend autoloader class.

Example: $this->my_zend->load('Loader');

### loadClass('ZEND Class to load', 'DIR path');

to load zend library classes you call the static method from the loader class and pass the library class to load.. All class files are prefixed with Zend_

Example: Zend_Loader::loadClass('Zend_EventManager_Event');


The following is an example of the steps to load a zend library...


Test:

$this->load->spark('zend-lib/x.x.x);

$this->my_zend->load('Loader');

Zend_Loader::loadClass('Zend_EventManager_Event');

   $event = new Zend_EventManager_Event('Event_name');
        echo $event->getName();
