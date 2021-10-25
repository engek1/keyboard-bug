# Keyboard Bug

This Project describes an unexpected and extremly unpleasant behavior of the WebKit Web View on iPad OS 14.0/14.1 we experienced in one of our Customers PWA.
I created this Project in order to demonstrate the behavior without any unneccessary content around, that could have influenced the behaviour unindentedly.
Unfortunately the Bug only appears when the App is installed on the Homescreen but not in any of the available Browsers (which all use WebKit engine on iPad OS) like Chrome or Firefox. 

Steps to reproduce the Problem:
  1.  open the example site (link below) in Safari on a iPad
  2.  add the Page to the Homescreen (PWA) and open it
  3.  type anything into one of the Input fields on the lower part of the page (e.g. into Nr. 7)
  4.  then close the Soft Keyboard on your iPad with the 'close Keyboard' Button
  5.  try to click (without scrolling or anything) into Input field Nr. 1 for example
  6.  Then it comes; instead of Input Nr. 1, any of the Input Fields underneath will gain focus, for example Nr. 2 or 3 (not constantly the same)

I guess the View Port is shifted somehow when the soft keyboard dismiss. The effect is that the wrong Elements gain the User Input events.

## start locally

clone repository -> /keyboard-bug
run `cd keyboard-bug`
run `npm install`
run `http-server`
open http://localhost:8080

## open hosted Example

https://engek1.github.io/keyboard-bug/index.html
