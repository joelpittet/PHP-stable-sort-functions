PHP stable sort utility methods
=========================
Version 2.0.0
[![Build Status](https://travis-ci.org/vanderlee/PHP-stable-sort-functions.svg)](https://travis-ci.org/vanderlee/PHP-stable-sort-functions)

Copyright &copy; 2015 Martijn van der Lee (http://martijn.vanderlee.com).
MIT Open Source license applies.

Introduction
------------
Collection of sort utility methods using stable sort. Equal values remain in the
original order. Only different values are sorted.

These sort utility methods follow the same interface and have the same functionality
and features as the builtin sort utility methods (except they add guaranteed sort
order). They have an "s" prefixed to the function name.

Each function has it's own file. Since you're likely to want to only include
the specific function(s) you need, this makes it easier. Just copy & paste.

Functions
---------
*	`bool SortArray::arsort ( array &$array [, int $sort_flags = SORT_REGULAR ] )`
*	`bool SortArray::asort ( array &$array [, int $sort_flags = SORT_REGULAR ] )`
*	`bool SortArray::natcasesort ( array &Sarray )`
*	`bool SortArray::natsort ( array &Sarray )`
*	`bool SortArray::uasort ( array &$array , callable $value_compare_func )`
*	`bool SortArray::uksort ( array &$array , callable $value_compare_func )`
*	`bool SortArray::usort ( array &$array , callable $value_compare_func )`

Tests
-----
PHPUnitTest testcases are included (group `stablesort`) in the `tests`
directory.

Disclaimers
-----------
Only functions that make sense are included, so no `sort` or `ksort` variants.
If you can demonstrate the case for any missing function, please let me know
and they will be included.

These are not the fastest possible implementations. In fact, I guarantee they
are not. Performance has been sacrificed for compatibility with their builtin
counterparts.

Changes
-------
### 2.0.0
* Converted to Utility class. By @joelpittet

### 1.0.3
*	Added `reset` calls to `sasort`/`sarsort` to ensure pointer. By @emilv.

### 1.0.2
*	PHP 5.3 compatibility changes by @folliked.

### 1.0.1
*	composer.json added by @thebeline.

### 1.0
*	Initial public release
