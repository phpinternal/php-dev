---
title: "Internal stuff to work on"
date: 2019-09-22
categories: [ coordination ]
---
## ext/* - Resource to object conversion in extensions

The 'resource' type was needed before PHP had classes to represent non-trivial 
types. However since PHP now has classes, it would be good to replace the 
resource types used internally.

Link: https://github.com/php-pecl/ProjectCoordination/blob/master/change_resource_to_specific_type.md

## Core - Annotate internal function types

We now have the capabilty to add type information to PHP core functions. 
The work is not difficult, but there is a large amount of it.

Link: https://github.com/php-pecl/ProjectCoordination/blob/master/annotate_internal_function_types.md

## ext/phar - Phar Extension - Need OSS Fuzz coverage

OSS Fuzz aims to find bugs by randomizing ("fuzzing") input. 
Phar has had a few bugs owing to edge cases in path processing and, 
being widely distributed form of PHP code, would benefit from fuzz testing. 
See https://github.com/google/oss-fuzz/tree/master/projects/php

Link: https://bugs.php.net/bug.php?id=78571

## ext/imap - Imap Extension - Reboot

The IMAP extension, while used across many open projects, performs poorly 
when compared to userspace implementations like Horde/Imap_Client. 
The library on which it is based (c-client) is unmaintained since 2011. 
And, there are a ton of bugs. We need to formulate a plan to either (a) accept 
the performance/features for what they are and just fix bugs or (b) reboot 
the extension from the ground up. Help wanted to steer and implement.
 
Link: https://bugs.php.net/bug.php?id=78572
