# Digital Clock

This project is a simple digital clock that displays the current time with an AM/PM indicator. The clock updates every second and is styled with a background image and custom fonts for a clean, modern look.

## Overview

This project is a digital clock built using HTML, CSS, and JavaScript. The clock dynamically updates every second to show the current time, formatted in a 12-hour format with an AM/PM indicator.

## ScreenShots
![Digital_Clock](https://github.com/user-attachments/assets/0a273976-7e97-4c80-b117-c208a0202fef)

## Links
- Live Site Url: [Live Site](https://shivomtiwari27.github.io/Digital_Clock/)
- Sorce Code : [Source Code](https://github.com/ShivomTiwari27/Digital_Clock)

## Features

- **Dynamic Time Update**: The clock automatically updates every second.
- **12-Hour Format**: Displays the time in 12-hour format with AM/PM.
- **Styled UI**: The clock is styled with a monospace font and a semi-transparent background that overlays a background image.

## Project Structure

- **HTML**: Defines the structure of the clock, including the container for the time display.
- **CSS**: Styles the clock with fonts, colors, and background images.
- **JavaScript**: Handles the logic for updating the time every second.

## What I Learned

This project helped me reinforce my understanding of:

- **JavaScript Functions**: Writing functions to perform tasks like getting the current time and formatting it.
- **setInterval**: Using `setInterval` to repeatedly execute a function at specified intervals, which is crucial for updating the clock every second.
- **String Manipulation**: Converting numbers to strings and padding them to ensure consistent formatting.
  
Here's a snippet that shows how the clock is updated every second:

```javascript
function updateClock(){
  const now = new Date();
  let hours = now.getHours();
  const meridiem = hours >= 12 ? "PM" : "AM";
  hours = hours % 12 || 12;
  hours = hours.toString().padStart(2, 0);
  const minute = now.getMinutes().toString().padStart(2, 0);
  const second = now.getSeconds().toString().padStart(2, 0);
  const timeString = `${hours}:${minute}:${second}:${meridiem}`;
  document.getElementById("clock").textContent = timeString;
}

setInterval(updateClock, 1000);
```
## Continued Development

In the future, this project can be expanded with the following features:

- **Date Display**: Include the current date along with the time.
- **Custom Themes**: Introduce multiple themes, allowing users to switch between different styles and backgrounds.
- **Time Zones**: Add support for displaying time across various time zones.
- **Alarms and Timers**: Implement functionality for setting alarms and countdown timers.

## Useful Resources

These resources were instrumental in building this project:

- **[MDN Web Docs - Date Object](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date)**: A comprehensive guide on how to handle dates and times in JavaScript.
- **[CSS-Tricks](https://css-tricks.com/)**: A valuable resource for learning and applying CSS techniques.
- **[YouTube - Bro Code](https://www.youtube.com/@BroCodez)**: Provided the initial inspiration and tutorial guidance for this project.

## Author

- **GitHub**: [ShivomTiwari27](https://github.com/ShivomTiwari27)

## Acknowledgments

A special thanks to [Bro Code](https://www.youtube.com/@BroCodez) for their excellent tutorials that laid the foundation for this project.
