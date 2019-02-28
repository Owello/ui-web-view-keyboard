UIWebView Keyboard Fix
========================

This branch shows an temporary fix in CSS for the iOS12 / UIWebview where the keyboard covers the bottom part of the page.

The main fix is:
```
body {
    position: fixed;
}
```

Github issue: [iOS 12 / UIWebView Keyboard covers INPUT elements at the bottom of page](https://github.com/apache/cordova-ios/issues/472)

Try it yourself
---------------
```
git clone git@github.com:Owello/ui-web-view-keyboard.git
cd ui-web-view-keyboard
sudo npm install -g cordova@8
cordova platform add ios@5
cordova run ios
```

Tested on
---------
- iPhone X (12.1.4)

Known issues
------------
When the keyboard is shown, iOS automatically scrolls to the bottom (showing the input above the keyboard). When you want to scroll back to the top, you have to scroll twice. Once for the scrolling content, and once for to scroll the body/viewport.

This issue exists only if the page is longer than the body when the keyboard is hidden.