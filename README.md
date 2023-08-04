# ublockscripts

## Description
The "Block non-latin char videos" script ublock-origin-block-non-latin.js is designed to prevent videos with titles or channel names containing a significant amount of non-latin characters from being processed or displayed. Non-latin characters include any characters outside the range of Latin script, such as special symbols, emojis, or characters from non-Latin scripts like Arabic, Chinese, Cyrillic, etc.

## Usage
The script takes two parameters: video and objectType, and it will return a boolean value indicating whether the video should be blocked or not.
This is for [uBlock](https://github.com/gorhill/uBlock) a popular ad blocker for various browsers.

Easy install if you have no advanced scripts yet; Just replace the default script with this script.
Refer to the current uBlock documentation on details how to install an extended filter script.

``
(video, objectType) => {
    // Script code here
}``

## Blocking Criteria

The script blocks videos if their title or channel name contains more than 10% non-latin characters. The calculation of the percentage is done using the following formula:

``(nonLatinCharactersCount / totalCharactersCount) > 0.1``

Here, nonLatinCharactersCount represents the number of non-latin characters in the title or channel name, and totalCharactersCount represents the total number of characters in the respective title or channel name.

## Implementation Details

The script uses a regular expression (unicodeRegExp) to identify non-latin characters in the input strings. The regular expression /[\u0080-\uFFFF]/g matches all characters in the Unicode range from \u0080 to \uFFFF, which includes non-latin characters. It then replaces these non-latin characters with an empty string to get the title and channel name without any non-latin characters.

##Optimization for Speed

To optimize the script for speed, we calculate the length of the title and channel name without non-latin characters once and reuse it in the condition checks. This avoids redundant processing of the same regular expression for both checks.

## How to Interpret the Output

  - If the script returns true, it means the video should be blocked because its title or channel name contains more than 10% non-latin characters.
  - If the script returns false, it means the video is allowed, and its title or channel name does not exceed the 10% threshold for non-latin characters.

# Examples

Here are some examples of how the script works:

## Example 1 - Block Video:

```javascript
const video = {
    title: "My Video Title 🎥",
    channelName: "Cool Channel 🌟"
};

console.log(blockNonLatinCharVideos(video)); // Output: true
```

In this example, both the title and channel name contain emojis, which are non-latin characters. As the percentage of non-latin characters in both the title and channel name exceeds 10% (more than 1.1), the script returns true, and the video should be blocked.

## Example 2 - Allow Video:

```javascript
const video = {
    title: "Summer Vacation Vlog",
    channelName: "Travel Enthusiast"
};

console.log(blockNonLatinCharVideos(video)); // Output: false
```

In this example, both the title and channel name only contain Latin characters, and there are no non-latin characters. As the percentage of non-latin characters in both the title and channel name is 0% (less than 1.1), the script returns false, and the video is allowed.

## Important Note

Please ensure that you provide valid input values for video.title and video.channelName when using the script to get accurate and reliable results. If the input is invalid or missing, the script will return false by default, indicating that the video should be blocked to avoid potential issues with incomplete data.
