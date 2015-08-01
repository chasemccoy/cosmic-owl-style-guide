# The Cosmic Owl Objective-C Style Guide

This guide is intended to be used as an outline of all coding conventions used by Cosmic Owl Studio when writing apps in Objective-C.

## Table of Contents
* [Spacing](#spacing)
* [Methods](#methods)
* [Variables](#variables)
* [Properties](#properties)
* [Conditionals](#conditionals)

## Spacing
* Indent using 2 spaces.
* Be sure to set the preference in Xcode to never indent with tabs.
* There should be exactly 4 blank lines in between methods. 
* Method braces and other braces (`if`/`else`/`switch`/`while` etc.) always open on the same line as the statement but close on a new line.

## Methods
When declaring a method signature, there should be a space after the scope symbol. There should be a space between the arguments, but not after the method name and colon.

**For Example:**
```objc
- (void)setExampleText:(NSString *)text image:(UIImage *)image;
```

Methods in the `.h` file should always be listen in the same order in the `.m` file. In addition, methods should always be documented immediately before their implementation. 

If a method has three or more arguments (or more than 80 characters), seperate arguments onto their own line, and align them at the colon. 

**For Example:**
```objc
- (id)setExampleTest: (NSString *)text
               image: (UIImage *)image
                bool: (BOOL)bool;
```  

## Variables
* Variables should be written in camel case, with the first letter always being lowercase. 
* The pointer operator should always be placed immediately before the variable name.
* Always use descriptive variable names, even if that means the name is unusually long. 

## Properties
* Properties should be accessed using `self.propertyName`, not `_propertyName`. The only exception is inside an initializer method.
* Properties should be declared as nonatomic in thread-safe environments.
* Always declare properties using the strong keyword.

## Conditionals
* Braces aways open on the same line as the statement, and close on a new line.
* `else` and `else if` statements always start on a new line. 
* Always surround conditional bodies in brackets, even when the body is a single line. 

**For Example:**
```objc
if (!error) {
    return success;
}
else {
    return error;
}
```
