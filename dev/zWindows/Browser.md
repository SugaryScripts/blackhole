# Bypass Expired SSL Certificate
## Internet Explorer
1. In Internet Explorer, navigate to Tools / Internet options
2. Click the Advanced tab
3. Scroll down to the bottom of the list and uncheck Warn about certificate address mismatch (3rd option from bottom)
4. Reboot your computer
## Chrome
1. Right-click the Google Chrome shortcut on your desktop and select Properties.
2. In the Target field simple append the following parameter after the quoted string: --ignore-certificate-errors
3. The whole field should now look something like this:  "C:\Program Files\Google\Chrome\Application\chrome.exe" --ignore-certificate-errors
## Firefox
1. In Firefox, enter about:config into the address bar
2. If prompted with a This might void your warranty! warning, simply click on the I'll be careful, I promise! button
3. Type browser.ssl_override_behavior within the Filter: field - then double-click on the found parameter to edit:
4. Change Enter integer value from 2 to 1 - then click the OK button:
5. Close Firefox and restart it.