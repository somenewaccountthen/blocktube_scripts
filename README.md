## Description
This is a script to be used with blocktube. It can filter based on video age, narcissism and exotic charset for channel and video title.
You can put the script in 'Filter options' / 'Advanced Blocking' inside blocktube.
![blocktubeadvancedfilters](https://github.com/user-attachments/assets/c9b745bc-a07c-44f4-9997-f468fc8032ba)

## Usage
Hide by setting a constant to true, show it by setting it to false. This is case sensitive so use lowercase.
Example: To hide videos from today set the 'const hideToday = true'. 
- const hideToday  = true


## Block/Hide narcicssists 
- hideNarcissists: Hides any video with a title starting with "I " 


## Block/Hide exotic char sets
- hideExoticCharChannelsAndTitles: Hides videos with titles or channel names containing a significant amount of non-latin characters from being processed or displayed. Non-latin characters include any characters outside the range of Latin script, such as special symbols, emojis, or characters from non-Latin scripts like Arabic, Chinese, Cyrillic, Thai, etc.


## Block/Hide videos based on age
- hideToday: Hide videos with ages that contain 'x hour', 'x hours' and '1 day'.
- hideDays: Hide videos with ages that contain 'x days'.
- hideWeek: Hide videos with ages that contain 'x week'.
- hideWeeks: Hide videos with ages that contain 'x weeks'.
- hideMonth: Hide videos with ages that contain 'x month'.
- hideMonths: Hide videos with ages that contain 'x months'.
- hideYear: Hide videos with ages that contain 'x year'.
- hideYears: Hide videos with ages that contain 'x years'.
