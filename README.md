# tuning-primer.sh
## About this repository
MySQL Tuning-Primer.sh

This is the script originally developed by Matthew Montgomery, and previously hosted at Day32.com.  This version has been updated and improved for newer versions of MySQL, Percona Server, and MariaDB.  This Github repository was created with Matthew's permission by Dan Reif, but Matthew has no control over it; in other words, please don't bother Matthew with questions about this repository!

This repository will be used to handle ongoing development and bugfixes for this script.  Please file bug reports <a href="https://github.com/BMDan/tuning-primer.sh/issues">here</a>.

## About this script
This script takes information from `SHOW STATUS LIKE...` and `SHOW VARIABLES LIKE...` to produce sane recomendations for tuning server variables. 

It is compatible with all versions of MySQL 3.23 and higher (including 5.x).

Currently it handles recomendations for the following:

* Slow Query Log
* Max Connections
* Worker Threads
* Key Buffer [MyISAM only]
* Query Cache
* Sort Buffer
* Joins
* Temp Tables
* Table (Open & Definition) Cache
* Table Locking
* Table Scans (`read_buffer`) [MyISAM only]
* InnoDB Status

### Recent Changes

* Updated to (at least mostly) support MySQL 5.7+ and MariaDB
* A lot of cleanup of the underlying code
* Better handling of terminals and redirection (got rid of the hardcoded color sequences, switched to proper terminfo)
* <a href="https://github.com/BMDan/tuning-primer.sh/commit/6b5d866f7525b250bb4ecb0deffd66531e375143">Fixed</a> the old ``./tuning-primer.sh: line 402: export: `2097152': not a valid identifier`` bug

More, as always, in the <a href="https://github.com/BMDan/tuning-primer.sh/commits/master">changelog</a>.
