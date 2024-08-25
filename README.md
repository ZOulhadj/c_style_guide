# C Style Guide

This is my own personal style guide that I use for my personal projects. It is
based mostly off of my experience and trying to understand the significance and
implications of different programming styles. My style is heavily influenced by
[Linux kernel coding
style](https://www.kernel.org/doc/html/v4.10/process/coding-style.html) with a
few slight changes. Particularly with capitalisation of structure types.

## Comments
```
// Single line comment

//
// Multi-line comment
//
```

## Indentation
Four spaces are used for indentation.

## Types
All struct declarations must be preceded by the ```struct``` keyword.
```struct This_Is_My_Type```

## Pointer position

The pointer should be on the name and not the type. In assembly where types are
not a thing but the registers ```eax``` and memory loads ```[eax]``` are it just
makes more sense. C is based on the "declarations follow use" principle so for
example, an array which is really just a pointer is defined as such: ```int
numbers[200];```. Not, ```int[200] numbers;``` and the same goes for function
pointers or any other construct.

```struct This_Is_My_Type *type = NULL;```

## Functions
```
int my_function(struct This_Is_My_Type *type)
{
    if (true) {

    } else {

    }
}

```
