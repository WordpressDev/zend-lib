# Zend-lib integration of ZF 1.12 libraries with Codeigniter

## Requirements

* CodeIgniter 2
* [CodeIgniter Sparks](http://getsparks.org/)

## Setup

1. [Install Sparks](http://getsparks.org/install) if you haven't done so already.
2. Install the zend-lib spark (see [here](http://getsparks.org/get-sparks) if you don't know how).

## Info

Zend-lib is a spark that allows the Zend Framework libraries to be loaded into codeiginiter as additional libraries. The list of libraries available come from the Zend Framework version 1.12.
Most of the available libraries have been tested for correct functionality within codeigniter..

## Usage

### $this->load->spark('my_zend/x.x.x');

To load the my_zend spark..

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
