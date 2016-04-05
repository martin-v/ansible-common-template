ansible-common-template
=======================

This project is a template with several basic configuration for ansible setups.
This includes general etckeeper support and unattended upgrades for debian.


Usage
-----

To get a clean "normal" setup and to allow merges of future updates from
this repository use the following commands:

With new remote `origin` repository:

	git clone --origin template_origin https://github.com/martin-v/ansible-common-template.git MY_FIRST_ANSIBLE_PROJECT
	git checkout -b master
	git remote add origin https://MY_GIT_SERVER/MY_GIT_REPO
	git branch --set-upstream-to origin

Without remote `origin`

	git clone --origin template_origin https://github.com/martin-v/ansible-common-template.git MY_FIRST_ANSIBLE_PROJECT
	git checkout -b master
	git remote add origin .
	git branch --set-upstream-to origin


Open tasks
----------

* Write more documentation.
* Download fix version of grml zshrc and add checksum test.


Credits
-------

This module is heavily base on work of several [Entropia](http://entropia.de/) members.

Special thanks to:
* [fxkr](https://github.com/fxkr)
* [florolf](https://github.com/florolf)
* [problame](https://github.com/problame)


License
-------

Licensed under [MIT License](LICENSE)

Copyright (c) 2016 Martin Vietz <opensource@martin.vietz.eu>
