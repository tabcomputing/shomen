# Shomen
## Standardized Documentation Format for OOPLS

[Website](http://tabcomputung.github.com/shomen) /
[Manual](http://github.com/tabcomputing/shomen/wiki) /
[Mailing List](http://groups.google.com/groups/rubyworks-mailinglist) /
[IRC Channel](http://chat.us.freenode.net/rubyworks)


## Description

Shomen is an intermediary documentation model designed for documenting
object-oriented programming languages, particularly Ruby. The specification
is a flat mapping, without internal referencing, suitable for storage in both
YAML and JSON formats.


## Why?

By using a standard intermediary format, documentation parsers need only concern
themselves with a single output target. And documentation templates in turn only
need to concern themselves with a single input format regardless of the parsing
system that was used to generate it.


## Features

* Update a single portable file to update documentation.
* Site disc footprint is extra small thanks to CDNs.
* Personalize site design to best fit your project.
* Test drive others customizations with your own remote docs!


## Instructions

To learn about Shomen in detail please visit the [User Guide](http://github.com/tabcomputings/shomen/wiki).

To utilize Shomen you will need two things: a *generator* to produce the Shomen document for your
project, and a *viewer* that can be used to view the documentation provided by the Shomen document.

There are three generators currently available:

* [Shomen YARD](http://github.com/rubyworks/shomen-yard)
* [Shomen RDoc](http://github.com/rubyworks/shomen-rdoc)
* [RDoc Shomen](http://github.com/rubyworks/rdoc-shomen)

The first and the later are currently the go to projects. Unfortunately the second project
currently is limited in capability due to some issues with RDoc, so should be avoid for
the time being.

Next you want to pair up your `doc.json` file with a viewer. 
Currently there are three views available:

* [HyperVisor](http://github.com/rubyworks/hypervisor)
* [Rebecca](http://github.com/rubyworks/rebecca)
* [Rubyfaux](http://github.com/rubyworks/rubyfaux)

You can copy any of those repos to your website (e.g. site/) and run with it.
If you want to try it out locally, we recommend using [thin](http://code.macournoyer.com/thin/)
to view the site.

    $ cd site
    $ thin start -A file

Viewers don't necessarily need to be copied. All three above can take
a `doc={url-to-shomen-json-file}` http parameter and server up the docs remotely.
You just need to publish your `doc.json` file to a publicly accessible URL on GitHub.
Note, we recommend that you name the file specifically, e.g. `myapp-1.0.0.json`.

See the viewer projects for more information.


## Copying

Copyright (c) 2010 Rubyworks

Shomen is distributed under the terms of the **BSD-2-Clause** license.

See License.txt for license details.

