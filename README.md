## Description
These scripts can be used with blocktube. It can filter based on video age, narcissism, exotic charset for channel and video title and 'one minute ago' style video title.
You can put the script in 'Filter options' / 'Advanced Blocking' inside [blocktube](https://github.com/amitbl/blocktube/wiki).
![blocktubeadvancedfilters](https://github.com/user-attachments/assets/c9b745bc-a07c-44f4-9997-f468fc8032ba)

# Three scripts, pick one. You only need one.
Each script filters the same things. The only difference is the logging.
- blocktube-block-script-with-logging-always-on.js-snippet.txt has info console logging always on.
- blocktube-block-script-with-logging.js-snippet.txt has a toggle to turn on and off info console logging on and off.
- blocktube-block-script.js-snippet.txt has no logging.


## Usage
Hide by setting a constant to true, show it by setting it to false. This is case sensitive so use lowercase.
Example: To hide videos from today set the 'const hideToday = true'. 

const hideToday  = true

This will hide all videos with an age string containing the text 'hour' and '1 day'.

## Block/Hide narcicssists 
- hideNarcissists: Hides any video with a title starting with "I " or "i ". 


## Block/Hide exotic char sets
- hideExoticCharChannelsAndTitles: Hides videos with titles or channel names containing a significant amount of non-latin characters from being processed or displayed. Non-latin characters include any characters outside the range of Latin script, such as special symbols, emojis, or characters from non-Latin scripts like Arabic, Chinese, Cyrillic, Thai, etc.


## Block/Hide videos based on age
The age of a video is a text string. Some examples are '1 week', '4 weeks', '2 months', '14 years'. I refer this as the 'age text'.
- hideToday: Hide videos with an age text that contains 'hour' or 'hours' or '1 day'.
- hideDays: Hide videos with an age text that contains 'days ago'.
- hideWeek: Hide videos with an age text that contains 'week ago'.
- hideWeeks: Hide videos with an age text that contains 'weeks ago'.
- hideMonth: Hide videos with an age text that contains 'month ago'.
- hideMonths: Hide videos with an age text that contains 'months ago'.
- hideYear: Hide videos with an age text that contains 'year ago'.
- hideYears: Hide videos with an age text that contains 'years ago'.

## Block/Hide videos based on annoying one minute ago title
- hideOneminuteAgo: Hide video with the title start '1 minute ago' and 'one minute ago'

# How to see the info log in your browser when using the script with the logging.
Make sure you are using one of these two scripts:
- blocktube-block-script-with-logging-always-on.js-snippet.txt
- blocktube-block-script-with-logging.js-snippet.txt with const logInfo set to true".

Open a Youtube page:
- Press F12.
- 1: Click the tab that says 'Console'.
- 2: Make sure 'info' is enabled.
- Refresh the page.
![image](https://github.com/user-attachments/assets/e5adc1d9-8a10-46b0-9bc6-f76bba345f28)


# Code
Code was kept simple so people can change it without requireing a degree in computer science. Good luck! 
