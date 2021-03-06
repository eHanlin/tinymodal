#
這邊只是將tiny modal 放置 npm 使用

#author
elclanrs

#link
https://github.com/elclanrs/jquery.tiny.modal


# jQuery Tiny Modal

Barebones modal dialogs.

**Demo:** [http://jsbin.com/UlusaXI/2](http://jsbin.com/UlusaXI/2)

## How to

Create a container with an ID for your modal dialog, then put any markup you want inside.

```html
<div id="mymodal">
  <h2>My Modal</h2>
  <p>Lorem ipsum dolor sit amet consectetur</p>
</div>
```

Make sure to hide the modal in your CSS:

```css
#mymodal { display: none }
```

Trigger your modal on some element, like a button for example and call the plugin:

```javascript
$('button').click(function(){
  $.tinyModal({
    title: 'My Modal',
    html: '#mymodal'
  });
});
```

Tiny Modal comes with a basic theme that you can configure in `styl/jquery.tinymodal.styl`. Make sure to run `npm install` to download the dependencies. After editing don't forget to watch your files for changes and compile with `sh compile.sh`.

## Options

```javascript
_defaults = {
  buttons: ['Ok','Cancel'],
  title: 'Alert',
  html: '<p>Alert</p>', // markup or selector
  Ok: $.noop, // callback for the "Ok" button
  Cancel: $.noop, // callback for the "Cancel" button
  onClose: $.noop, // callback after the dialog closes
  clickOutside: true // close the dialog when clicking outside
};
```
