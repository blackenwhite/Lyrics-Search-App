# Lyrics-Search-App

## Introduction

This Web-App allows the user to search for a song in the search bar and it displays the results with pagination. Once clicked on the "Get Lyrics" button, the lyrics of the chosen song is displayed with lyrics functionality. It uses the lyrics.ovh API.

## Home(index)

The html file is a simple one containing a form to take the search input from the user.It has a placeholder to show some test. The lower part of the page will contain the results as and when the results will be loaded.

### PlaceHolder

The placeholder attribute specifies a short hint that describes the expected value of an input field (e.g. a sample value or a short description of the expected format).
The short hint is displayed in the input field before the user enters a value.

## StyleSheet

### Border Box

The box-sizing property allows us to include the padding and border in an element's total width and height.
If we set box-sizing: border-box; on an element, padding and border are included in the width and height:

```*{
	box-sizing: border-box;
}
```

### Transform
```button{
	cursor: pointer;
}

button:active{
	transform:scale(0.955);
}

input:focus,button:focus{
	outline:none;

}
```

##### Explanation

Cursor is set to be pointer. And when the button is active we are scaling down the size of the button to 0.95 . Focus is also added. Outline is an element property which draws a line around element but outside the border. It does not take space from the width of an element like border.

### Header styling

A suitable image is selected for background in the header. Display is set to be flex. Flex direction to be column. Text clor to be white. Items are aligned at center. rgba() is used to set how much bright the background image would be.

### Script

First of all we need to grab all elements and assign relatable variable-names to them. This can be done document.getElementById().
```const form = document.getElementById('form');
const search = document.getElementById('search');
const result = document.getElementById('result');
const more = document.getElementById('more');
```

## References

https://lyricsovh.docs.apiary.io/#
https://www.w3schools.com/tags/att_input_placeholder.asp
https://www.geeksforgeeks.org/how-to-remove-focus-around-buttons-on-click/
