# Config Recipes

## This module is deprecated.

We recommend searching for "recipes" on BackdropCMS.org for stand alone recipes that can be installed directly to Backdrop sites. 

## A library of config recipes for Backdrop CMS

This is intended to be the first step towards a much better solution to move features from one backdrop site to another (Drupal 7 had the Features module - https://www.drupal.org/project/features). 

Each directory contains a specific recipe that can be used to import a feature into an existing Backdrop CMS site. Recipes may include things like Content Types, Fields, Field Instances, Views, and anything else that is created in config files.  

For more information aboout creating recipes, see: https://github.com/backdrop-contrib/config_recipes/wiki/Creating-Recipes

## This "library" currently includes:
* FAQ - A recipe to create a FAQ content type and view
* People - Creates a "people" content type that can easily be used for a staff directory. One sample view is already included for a view of your "Team" built off the "people" content type. Works best with Tatsu theme. 
* Locations - Requires Addressfield, Geofield, Geocoder, and GeoPHP modules. (Under development - PR welcome). 
* Testimonials - A recipe to create a testimonial content type and view.
* Events - A simple events recipe with date and venue fields
* Info blocks- A recipe to create a content type without a path for use with blocks (designed specifically to work with Opera theme). 

Each directory contains:
* A README file that includes information regarding dependencies.
* The individual .json files included in that recipe
* A clean .tar archive of the files included in that recipe

## Installation

We have created a very rough module that will upload recipes compressed into a .tar format. 
This development project [https://github.com/backdrop-contrib/config_batch_upload] is working,
but has very limited features and is still being tested. 

### Intall multiple files at once 

You can import one or more recipes in as a batch using the following process. 

1) Full export of existing site config 
2) Add recipes to site config 
3) Full import of existing site config plus the added recipes

Using this process, Backdrop CMS should be able to process the new config files in the correct order. 

NOTE: If you have easy access to the config directories, you can drop ALL the files directly into the staging directory. To use the UI to import the full config, you will need to create a tar.gz file and you must be sure to EXCLUDE the partent directory from the file. 

See discussion: https://forum.backdropcms.org/forum/how-add-bundle-or-group-config-files-site

### Install individual files

Intially, we installed these recipes one config file at a time using the single file import feature in the UI - admin/config/development/configuration/single/import. This is a little tricky, because you must import the files in the correct order or you will generate errors. For example you must import the node.type file before the field.field.field file and must load the field.field.field file before the field.instance file.

Here is the rough order in which I expect files must/should be loaded:

* node.type
* image.style
* field.field
* field.instance
* views.view

## Related issues and projects:

* [Add 'recipe' project type to Backdrop](https://github.com/backdrop/backdrop-issues/issues/3763)

## Maintainers

- Tim Erickson (https://github.com/stpaultim).
- Seeking co-maintainers

## LICENSE

This project is GPL v2 software. See the LICENSE.txt file in this directory for
complete text.
