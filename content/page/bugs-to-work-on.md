---
title: "Bugs to Work On"
date: 2019-09-22
categories: [ coordination ]
---
## PDO -> PDO driver error conditions

There is an oversight between PDO and some PDO drivers on how certain 
error conditions are missed. This leads to some error conditions having 
their error message or exception not triggered: https://bugs.php.net/bug.php?id=77490

Link: https://github.com/php/php-src/pull/4288
