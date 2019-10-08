# backdropcms-features

A library of config features/recipes for export / experimentation

As a start, each directory in the library should contain the config files for one recipe/feature. In theory, we should be able to add the config files from any feature directory to an existing Backdrop project and then synchronize the config files, to add that feature to the site. 

As of this time, we done very little experimentation to test how this works. 

This "library" currently includes:
* FAQ - A recipe to create a FAQ content type and view
* People - Creates a "people" content type that can easily be used for a staff directory. One sample view is already included.  

Currently, I am just importing the files one at a time. Would love suggestions on how to make this better. Files must be loaded in a logical order, for example you must import the node.type file before the field.field.field file and must load the field.field.field file before the field.instance file.

Here is the rough order in which I expect files must/should be loaded:

* node.type
* image.style
* field.field
* field.instance
* views.view

Please, help make this documentation better.

Related core issue for Backdrop CMS:

* [Add 'recipe' project type to Backdrop](https://github.com/backdrop/backdrop-issues/issues/3763)


