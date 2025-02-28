UberGallery - The simple PHP photo gallery
==========================================
Created by, [Chris Kankiewicz](http://www.ChrisKankiewicz.com)


Introduction
------------
UberGallery is an easy to use, simple to manage, web photo gallery written in PHP and dual licensed
under the [MIT License](http://www.ubergallery.net/COPYING-MIT.txt) and 
[GNU General Public License (GPL) Version 3](http://www.ubergallery.net/COPYING-GPL.txt). UberGallery 
**does not** require a database and supports JPEG, GIF and PNG file types. Simply upload your images
and UberGallery will automatically generate thumbnails and output standards compliant XHTML markup
on the fly.


Features
--------
* Simple first time installation
* Database-less configuration
* Include galleries within pre-existing sites
* Create multiple galleries with a single installation
* Easily customize your gallery styles via CSS
* Install and update the gallery easily wth Git (optional)


Requirements
------------
UberGallery requires PHP 5.0+ and the PHP-GD image library to work properly. For more information
on PHP and the PHP-GD image library, please visit [http://php.net](http://php.net).


Simple Installation
-------------------
Copy `resources/sample.galleryConfig.ini` to `resources/galleryConfig.ini` and modify the settings
to your liking.

Upload `index.php`, `resources/` and `gallery-images/` to your web server.

Upload images to the `gallery-images/` directory.

Make the `resources/cache/` directory writable by the web server:
    
    chmod 777 -R /path/to/resources/cache
    
Open your web browser and load the page where you installed UberGallery.


Custom Installation
-------------------
Copy `resources/sample.galleryConfig.ini` to `resources/galleryConfig.ini` and modify the settings to
your liking.

Upload the `resources/` folder to your web server.

Insert the following code into the PHP page where you would like the gallery to be displayed
(be sure to change the include and image folder path to match your configuration):
    
    <?php include_once('path/to/resources/UberGallery.php'); $gallery = UberGallery::init()->createGallery('path/to/images-folder'); ?>
    
Include the UberGallery and desired Colorbox style sheet in your page header:
    
    <link rel="stylesheet" type="text/css" href="path/to/resources/UberGallery.css" />
    <link rel="stylesheet" type="text/css" href="path/to/resources/colorbox/{1-5}/colorbox.css" />
    
Include the jQuery and Colorbox javascript files in your page header:

    <script type="text/javascript" src="http://ajax.googleapis.com/ajax/libs/jquery/1.6.4/jquery.min.js"></script>
    <script type="text/javascript" src="path/to/resources/colorbox/jquery.colorbox.js"></script>
    
Include the Colorbox jquery call in your header:

    <script type="text/javascript">
    $(document).ready(function(){
        $("a[rel='colorbox']").colorbox({maxWidth: "90%", maxHeight: "90%", opacity: ".5"});
    });
    </script>
    
Upload images to your images directory.

Make the `resources/cache/` directory writable by the web server.
    
    chmod 777 -R /path/to/resources/cache
        
Open your web browser and load the page where you installed UberGallery.


Install with Git
----------------
SSH into the your server and clone the UberGallery repository:

    git clone git://github.com/UberGallery/UberGallery.git /path/to/gallery-directory

Copy `resources/sample.galleryConfig.ini` to `resources/galleryConfig.ini` and modify the settings

    cp /path/to/gallery-directory/resource/sample.galleryConfig.ini /path/to/gallery-directory/resources/galleryConfig.ini
    nano /path/to/gallery-directory/resources/galleryConfig.ini

Upload images to the `gallery-images/` folder within your gallery directory.

Make the `resources/cache/` directory writable by the web server.
    
    chmod 777 -R /path/to/resources/cache
        
Open your web browser and load the page where you installed UberGallery.

**NOTE:** When using this method to install UberGallery, you may update your installation by running
the following commands:

    cd /path/to/gallery-directory
    git pull origin master


Support
-------
If you have any questions or comments, please email me at: [Chris@ChrisKankiewicz.com](mailto:Chris@ChrisKankiewicz.com)

UberGallery updates and news can be found on our [Tumblr blog](http://news.ubergallery.net/) or by
[following us on Twitter](http://twitter.com/ubergallery).

To report a bug, visit the issue tracker on Github at: http://github.com/UberGallery/ubergallery/issues


License
-------
Copyright (C) 2011 [Chris Kankiewicz](http://www.chriskankiewicz.com)

UberGallery is dual licensed under the terms of the
[MIT License](http://www.ubergallery.net/COPYING-MIT.txt) and
[GNU General Public License (GPL) Version 3](http://www.ubergallery.net/COPYING-GPL.txt).
See `COPYING-MIT` and `COPYING-GPL` for details.
