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

* Correct awk display error which formats integers > 4294967296 in scientific notation. 
** Was manfest in `MEMORY USAGE` section where total system RAM > 4GB.
* Fixed rounding error where mysql will lose 4K from the `join_buffer_size` value. 
** Other values may have the same issue but are not yet reported
* Added support for FreeBSD and MacOS (thanks Sam and Geert)
* Added support for Solaris
* Changed how system memory is derived on Linux. 
** Use `/proc/meminfo` vs `free -b` and avoid inclusion of swap space.
* Include note warning of instability when `key_buffer_size` > 4GB in versions 5.0.51 and lower
* Bugfix to correct InnoDB support detection in 5.5/5.6
