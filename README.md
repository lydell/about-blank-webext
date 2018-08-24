# Firefox WebExtension about:blank iframe bug

1. Go to about:debugging and load this folder as a temporary add-on.
2. Open test.html.

Expected results: All five links should be given a red background color, and "content.js starting" should be logged five times in the console.

Actual results: Only four links are given a red background color, and "content.js starting" is only logged four times in the console.

The content script does not appear to run at all for the iframe with no src inserted after 1 second.

- Tested with: Firefox Nightly 63.0a1 (2018-08-24) (64-bit)
- Verified working with: Chromium Version 68.0.3440.106

https://bugzilla.mozilla.org/show_bug.cgi?id=1415539
