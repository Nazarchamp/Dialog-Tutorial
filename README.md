# How to Use Dialog in HTML and CSS

## What is a Dialog?
The `dialog` element is used in a similar manner as a traditional `div` modal that is commonly used when you want to get content to pop up on a users screen.

#### The Differences Between Modals and Popup Divs
A `dialog` is essentially a Popup div bundled into default styling of a browser. When creating a Popup you need to custom style your `div`
to appear in front of all the other content on your screen, move it into the desired location, add a backdrop and create a function to close your modal. A `dialog` comes with all of this preconfigured, and if you don't like some of the default styling simply override it in CSS.

## How to use it
#### HTML
In HTML you simply use `dialog` like you would a popup `div` in the following manner: `<dialog>`content`</dialog>`. Where the content is what you want to display when your dialog opens. Make sure to have a button to open your dialog, and one to close it (This is slightly optional, as dialogs will by default close when `esc` is clicked).
```html
    <button id='open'>Open Dialog</button>

    <dialog id="modal">
        <h1>This is a dialog!</h1>
        <p>Lorem Ipsum Dolor</p>
        <button id='close'>Close Dialog</button>
    </dialog>
```

#### JavaScript
In JS assign event listeners to each of the buttons that open and close the dialog.
```js
const open = document.getElementById('open');
const close = document.getElementById('close');
const dialog = document.getElementById('modal');

open.addEventListener('click', () => {
    //There are two possible methods to open your dialog, both work identically: .show(), .showModal()
    dialog.showModal();
});

close.addEventListener('click', () => {
    dialog.close();
});
```
