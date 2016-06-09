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

#### `onBeforeAdd`

Similar to the `onAdd` function, but runs at the very beginning of the `add_token` method.

**Example Usage:**

`javascripts/components/file.js.coffee`

```coffee
$(‘.js-some-input’).tokenInput AppRoutes.some_path({foo: bar}),
  onBeforeAdd: ( item ) ->
    # When false is returned the entire `add_token` method is halted — the token is not added and the dropdown is not dismissed.
    if item.is_disabled
      return false
```
