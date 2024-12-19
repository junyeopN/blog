---
title: Fixed Size Basic Types in C 
layout: home
parent: C programming 
---

The most basic primitive types in C **are not guaranteed to have the same size in different platforms**

* int can be 32bit in one system and 8 bit in another

This hurts portability, so it is better to **use fixed-size types defined in <stdint.h> instead**

```c
#include <stdint.h>

int16_t integer_16bit;
uint16_t unsigned_integer_16bit;
```