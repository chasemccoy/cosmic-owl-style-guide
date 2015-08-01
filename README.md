# The Cosmic Owl Objective-C Style Guide

This guide is intended to be used as an outline of all coding conventions used by Cosmic Owl Studio when writing apps in Objective-C.

## Table of Contents
* [Documentation and Organization](#documentation-and-organization)
* [Spacing](#spacing)
* [Methods](#methods)
* [Variables](#variables)
* [Properties](#properties)
* [Conditionals](#conditionals)
* [Classes](#classes)

## Documentation and Organization
* Methods should always be documented immediately before the method is implemented.
* Document whether object parameters allow `nil` as a value.
* **Pragma Marks**
    - In `.h` files, use pragma marks to seperate properties `#pragma mark - Properties` and methods `#pragma mark - Methods`. In these sections, subdivide properties and methods into functional groups if necessary using `#pragma mark Section`.
    - In `.m` files, use pragma marks such as `#pragma mark - Grouping` to organize methods into functional groups. Always put delegate methods in their own group.
* 

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
* `NSInteger` and `NSUInteger` should be used instead of `int`, `long`, etc.
* All Apple types should be used over primitive ones. For example, if you are working with time intervals, use `NSTimeInterval` instead of `double` even though it is synonymous. 

## Properties
* Properties should be accessed using `self.propertyName`, not `_propertyName`. The only exception is inside an initializer method.
* Properties should be declared as nonatomic in thread-safe environments.
* Always declare properties using the strong keyword.

## Conditionals
* Braces aways open on the same line as the statement, and close on a new line.
* `else` and `else if` statements always start on a new line. 
* Only use the ternary condtional operator if a single condtion is being evaluated. 
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

## Classes
All class names and constants should be prefixed with `CO`.
