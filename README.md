# Uncommon HTML Bug: Silent Failure on Non-Existent Attribute Access

This repository demonstrates an uncommon bug in HTML related to accessing non-existent attributes using the `getAttribute()` method.

## Description

When attempting to retrieve the value of a non-existent attribute using `getAttribute()`, instead of throwing an error, it silently returns `null`. This behavior can make debugging challenging because there's no immediate indication that an error has occurred.

## Bug

The `bug.html` file demonstrates this issue. We try to access a non-existent attribute (`data-nonexistent`) on a div element using `getAttribute()`.  The script does not throw an error and the output is `null`.  The commented-out code illustrates the difference; attempting to directly access the non-existent property throws an error.

## Solution

While there's no direct solution to change this fundamental HTML behavior, the best practice is to ensure that attributes are valid and exist before trying to access them.  The `solution.html` file shows adding a check before accessing attributes to avoid unexpected behavior.  Input validation before processing HTML is also strongly encouraged.
