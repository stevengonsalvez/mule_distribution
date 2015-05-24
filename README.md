# mule_distribution

This contains the enterprise edition of the mule distribution  WHich is split archives . 

To join it follow the below steps.

* navigate to the mule_ee
* cat mule_ee* > mule_ee.tar.gz

## steps for creating a split archive 

#### first need to create the compressed archive.
* tar -cvvzf <archive-name>.tar.gz /path/to/folder

*This command file archive our folder to *.tar.gz. We can use file instead of path to folder for the argument. Then we will split up our file archive into small parts.*

* split -b 1M <archive-name>.tar.gz "parts-prefix"

*-b 1M will split the file into 1 Megabytes size of file.The "part-prefix" will give the prefix name of our parts of file.*

