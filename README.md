jQuery Tokeninput: A Tokenizing Autocomplete Text Entry
=======================================================

Overview
--------
Tokeninput is a jQuery plugin which allows your users to select multiple items from a predefined list, using autocompletion as they type to find each item. You may have seen a similar type of text entry when filling in the recipients field sending messages on facebook.

Documentation, Features and Demos
---------------------------------
Full details and documentation can be found on the project page here:

<http://loopj.com/jquery-tokeninput/>

Custom WeSpire Functions
---------------------------------

#### `onBeforeAdd`, `onAfterAdd`

Both replace the default `onAdd` function, but run at either the beginning or end of the `add_token` method.

**Example Usage:**

`javascripts/components/file.js.coffee`

```coffee
$(‘.js-some-input’).tokenInput AppRoutes.some_path({foo: bar}),
  onBeforeAdd: ( item ) ->
    if item.is_disabled
      return false
  onAfterAdd: ( item ) ->
    if item.is_super_cool
      alert("Wowie, this is one cool item!")
```
