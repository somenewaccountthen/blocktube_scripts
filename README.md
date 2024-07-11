## Description
This is a script to be used with blocktube. It can filter based on video age, narcissism and exotic charset for channel and video title.
You can put the script in 'Filter options' / 'Advanced Blocking' inside [blocktube](https://github.com/amitbl/blocktube/wiki).
![blocktubeadvancedfilters](https://github.com/user-attachments/assets/c9b745bc-a07c-44f4-9997-f468fc8032ba)

## Usage
Hide by setting a constant to true, show it by setting it to false. This is case sensitive so use lowercase.
Example: To hide videos from today set the 'const hideToday = true'. 

const hideToday  = true

This will hide all videos with an age string containing the text 'hour' and '1 day'.

## Block/Hide narcicssists 
- hideNarcissists: Hides any video with a title starting with "I " 


## Block/Hide exotic char sets
- hideExoticCharChannelsAndTitles: Hides videos with titles or channel names containing a significant amount of non-latin characters from being processed or displayed. Non-latin characters include any characters outside the range of Latin script, such as special symbols, emojis, or characters from non-Latin scripts like Arabic, Chinese, Cyrillic, Thai, etc.


## Block/Hide videos based on age
The age of a video is a text string. Some examples are '1 week', '4 weeks', '2 months', 14 years'. We refer this as the 'age text'.
- hideToday: Hide videos with an age text that contains 'hour' or 'hours' or '1 day'.
- hideDays: Hide videos with an age text that contains 'days ago'.
- hideWeek: Hide videos with an age text that contains 'week ago'.
- hideWeeks: Hide videos with an age text that contains 'weeks ago'.
- hideMonth: Hide videos with an age text that contains 'month ago'.
- hideMonths: Hide videos with an age text that contains 'months ago'.
- hideYear: Hide videos with an age text that contains 'year ago'.
- hideYears: Hide videos with an age text that contains 'years ago'.
