mass-delete v0.1
==========

Efficiently deletes large directories containing many thousands of files. This script is intend to provide a memory efficient and performant way to delete large directories when commands like 

	rm -rf .

fail. The script can also add a delay to every delete operation to reduce the load on production systems.

Requirements
------------

* Linux
* php5-cli or php7-cli package installed
* curl installed (for webinstall)

		#On Debian run
		sudo apt-get install php5-cli curl



Installation and Downloads
--------------------------

Run the following command to install the script:

	sudo curl -O /usr/bin/mass-delete \
	https://raw.githubusercontent.com/markus-perl/mass-delete/master/mass-delete \
	&& sudo chmod +x /usr/bin/mass-delete


Usage
-----

Delete the current folder recursive
	
	mass-delete .
	
Delete the current folder recursive with a 100 ms delay after each operation

	mass-dete . 100
	
Output
======

````
$ mass-delete . 50

mass-delete V0.1 - Markus Perl 2016
=====================================
Project Home: https://github.com/markus-perl/mass-delete
License: https://github.com/markus-perl/mass-delete/LICENSE
=====================================

Delete Operations are delayed by 50ms

/srv/gfs_images.old/data/public
/srv/gfs_images.old/data/public/user
/srv/gfs_images.old/data/public/user/medium
/srv/gfs_images.old/data/public/user/medium/5583
..........
/srv/gfs_images.old/data/public/user/medium/53fd
Files removed: 11
....................

(truncated)
````
