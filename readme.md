# CakePHP Image Helper

The main goal of this CakePHP helper is to give you the ability to resize an image without headache.

## Requirements

* CakePHP 2.x
* PHP Gd library 
* Keyboad + Mouse

## Installation

Load the helper at the desired controller. Or just at AppController.php.

    public $helpers = array('Image'); 

## Usage

Replace the standard function of CakePHP :
	
	~~$this->Html->image('path/image.[png|jpg|gif]', 'options' => array());~~

	$this->Image->resize('path/image.[png|jpg|gif]', width, height, 'options' => array(), 'quality' => 100);

	// Will generate a resized image path/image_widthxheight.[png|jpg|gif] (transparency is kept)
	// will output 

	<img src="path/image_widthxheight.[png|jpg|gif]" width="width" height="height"/>

The 4th parameter is the same than the 2nd parameter of **HtmlHelper::image()**

The 5th parameter is the image quality

If you only want to get the "generated" image path 

	$this->Image->resizedUrl('path/image.[png|jpg|gif]', width, height, 'quality' => 100);
