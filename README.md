# tuning-primer.sh
## About this repository
Matthew Montgomery's Tuning-Primer.sh, downloaded from Day32.com.

This repository will be used to handle ongoing development and bugfixes for this script.  Please file bug reports <a href="https://github.com/BMDan/tuning-primer.sh/issues">here</a>.

Copied to Github with Matthew's permission.  That said, please don't bug him with questions about this repository!

## About this script
This script takes information from `SHOW STATUS LIKE...` and `SHOW VARIABLES LIKE...` 
to produce sane recomendations for tuning server variables. 
It is compatible with all versions of MySQL 3.23 and higher (including 5.x).
Currently it handles recomendations for the following:

Slow Query Log
Max Connections
Worker Threads
Key Buffer
Query Cache
Sort Buffer
Joins
Temp Tables
Table (Open & Definition) Cache
Table Locking
Table Scans (read_buffer)
Innodb Status

### Recent Changes

* Updated to (at least mostly) support MySQL 5.7+ and MariaDB
* A lot of cleanup of the underlying code
* Better handling of terminals and redirection (got rid of the hardcoded color sequences, switched to proper terminfo)
* Fixed the old ``./tuning-primer.sh: line 402: export: `2097152': not a valid identifier`` bug (https://github.com/BMDan/tuning-primer.sh/commit/6b5d866f7525b250bb4ecb0deffd66531e375143)

More, as always, in the <a href="https://github.com/BMDan/tuning-primer.sh/commits/master">changelog</a>.
