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


## Script

First of all we need to grab all elements and assign relatable variable-names to them. This can be done document.getElementById().
```const form = document.getElementById('form');
const search = document.getElementById('search');
const result = document.getElementById('result');
const more = document.getElementById('more');
```
### Document.getElementById()

The Document method getElementById() returns an Element object representing the element whose id property matches the specified string. Since element IDs are required to be unique if specified, they're a useful way to get access to a specific element quickly.

apiURL is 'https://api.lyrics.ovh';

### Async and await

A promise is a special JavaScript object that links the “producing code” and the “consuming code” together. In terms of our analogy: this is the “subscription list”. The “producing code” takes whatever time it needs to produce the promised result, and the “promise” makes that result available to all of the subscribed code when it’s ready.
There’s a special syntax to work with promises in a more comfortable fashion, called “async/await”.

The word “async” before a function means one simple thing: a function always returns a promise. Other values are wrapped in a resolved promise automatically.For example,
```async function searchSongs(term) {
  const res = await fetch(`${apiURL}/suggest/${term}`);
  const data = await res.json();

  showData(data);
}
```

So, async ensures that the function returns a promise, and wraps non-promises in it. Simple enough, right? But not only that. There’s another keyword, await, that works only inside async functions, and it’s pretty cool.

Await

The syntax:

// works only inside async functions
let value = await promise;

The keyword await makes JavaScript wait until that promise settles and returns its result.


## References

https://lyricsovh.docs.apiary.io/#

https://www.w3schools.com/tags/att_input_placeholder.asp

https://www.geeksforgeeks.org/how-to-remove-focus-around-buttons-on-click/

https://javascript.info/async-await
