## Description
This is a script to be used with blocktube.
You can put it under 'Filter options' / 'Advanced Blocking' inside blocktube.

## Usage
Hide by setting a constant to true, show it by setting it to false. This is case sensitive so use lowercase.
Example: To hide videos from today set the 'const hideToday = true'. 
- const hideToday  = true


## Toggles for video age
### Hide videos with ages that contain 'x hour', 'x hours' and '1 day'
- const hideToday  = false
### Hide videos with ages that contain 'x days'
- const hideDays   = false
### Hide videos with ages that contain 'x week'
- const hideWeek   = true
### Hide videos with ages that contain 'x weeks'
- const hideWeeks  = true
### Hide videos with ages that contain 'x month'
- const hideMonth  = true
### Hide videos with ages that contain 'x months'
- const hideMonths = true
### Hide videos with ages that contain 'x year'
- const hideYear   = true
### Hide videos with ages that contain 'x years'
- const hideYears  = true


## Block narcicssists 
hideNarcissists blocks any video with a title starting with "I " 
- const hideNarcissists  = true


## Block exotic char sets
hideExoticCharChannelsAndTitles blocks videos with titles or channel names containing a significant amount of non-latin characters from being processed or displayed. Non-latin characters include any characters outside the range of Latin script, such as special symbols, emojis, or characters from non-Latin scripts like Arabic, Chinese, Cyrillic, Thai, etc.

- const hideExoticCharChannelsAndTitles = true
