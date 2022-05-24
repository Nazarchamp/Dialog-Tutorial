# How to Use Dialog in HTML and CSS

## Explaination

The `dialog` element is used in a similar manner as a traditional `div` modal that is commonly used when you want to get content to pop up on a users screen.

#### The Differences Between Modals and Popup Divs
A `dialog` is essentially a Popup div bundled into default styling of a browser. When creating a Popup you need to custom style your `div`
to appear in front of all the other content on your screen, move it into the desired location, add a backdrop and create a function to close your modal. A `dialog` comes with all of this preconfigured, and if you don't like some of the default styling simply override it in CSS.

## How to use it
##### HTML
In HTML you simply use `dialog` like a `div`. Typing it like this; `<dialog>`, `</dialog>`. Don't forget to add an open button and close button for the `dialog` to open and close!
```html
    <button id='open'>open</button>

    <dialog>
        <h1>This is a dialog!</h1>
        <button id='close'>close</button>
        <p>Put some content here</p>
    </dialog>
```

##### JavaScript
In JS we should be making the buttons to work, so that the `dialog` element opens and closes. Just like the below.
```js
open.addEventListener('click', function () {
    /*
        Apperently there are alternatives to do the same thing; opening the dialog.
        Here are the recommended to use:
            .show()
            .showModal()
    */
    dialogModal.showModal();
});

close.addEventListener('click', function () {
    dialogModal.close();
});
```

<br>

## Browser compatability
The `dialog` element is surprisingly compatible with all browsers except Interent Explorer. Both `.showModal` and `.close` code are compatible with the same browsers mentioned right before. 

Here's a visual example I found from MDN web docs.

![Table of compatibility](Screenshot%202022-05-16%20152000.png)

<br>

## Example
- [HTML](examplehere/index.html)
- [JS](examplehere/js/index.js)

<br>

## References 
- [MDN web docs dialog](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/dialog)
- [MDN web docs dialog.close()](https://developer.mozilla.org/en-US/docs/Web/API/HTMLDialogElement/close)
- [MDN web docs dialog.show()](https://developer.mozilla.org/en-US/docs/Web/API/HTMLDialogElement/show)
- [MDN web docs dialog.showModal()](https://developer.mozilla.org/en-US/docs/Web/API/HTMLDialogElement/showModal)
