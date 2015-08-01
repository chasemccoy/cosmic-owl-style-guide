# The Cosmic Owl Objective-C Style Guide

This guide is intended to be used as an outline of all coding conventions used by Cosmic Owl Studio when writing apps in Objective-C.

## Table of Contents


## Spacing
* Indent using 2 spaces.
* Be sure to set the preference in Xcode to never indent with tabs.
* There should be exactly 4 blank lines in between methods. 

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
