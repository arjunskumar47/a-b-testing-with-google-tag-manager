A/B testing script for Google Tag Manager
=========================================

It is a pretty simple script for A/B testing with [Google Tag Manager](https://www.google.com/tagmanager/) and [Google Analytics](http://www.google.com/analytics/) for measuring. It uses the [random macro](https://support.google.com/tagmanager/answer/2644341?hl=en#RandomNumber) of Google Tag Manager, that returns a number between 0 and 2147483647. It is [pseudo random](http://www.random.org/randomness/), but I run some tests and find that is random enough for A/B testing.

The script will send events to the classic (ga.js) or universial (analytics.js) version Google Analytics. You can change that for your own needs.

Use the rules in Google Tag Manager to set where the test on the website should be running and how much of the traffic is included in the test.

The traffic is equally distributed among the two variations of the A/B test.

### Requirements
* Google Tag Manager
  * Random Number macro
* [jQuery Cookie by carhartl](https://github.com/carhartl/jquery-cookie) - A minified version is included in the script.

## Create the Random Number macro in Google Tag Manager
_To use the script, you need te make the Random Number macro._

1. Click on the Read button New and select Macro.
2. Give the macro the name Randon Number.
3. Select from the dropdown Random Number.
4. Save the macro.

## How to use this script
1. Create a custom HTML tag in your Google Tag Manager container.
2. Past the code from [testing.js](https://github.com/simonvreeman/A-B-testing-with-Google-Tag-Manager/blob/master/testing.js) to the tag. Make sure you use `<script>` and `</script>` before and after.
3. Set a unique *test id*.
4. Set a unique *test name*.
5. Create a optimization version.
6. Set the rules for the test in Google Tag Manager.
7. Test is with debug on. Set debug in the script to 1 and use the debug option in Google Tag Manager.
8. Make sure the correct event tracking is working.
9. Turn the debug off. 
9. Create a new version and publish it.

## License
The MIT License (MIT)

Copyright (c) 2014 Simon Vreeman

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.