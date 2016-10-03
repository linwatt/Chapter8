To make the buttons call methods in `StopwatchFragment` when they are clicked, we’ll make the fragment implement the `View.OnClickListener` interface like this:

![](.guides/img/29.png)

This turns `StopwatchFragment` into a type of `View.OnClickListener` so that it can respond to when views are clicked.

You tell the fragment how to respond to clicks by implementing the `View.OnClickListener onClick()` method. This method gets called whenever a view in the fragment is clicked.

![](.guides/img/30.png)

The `onClick()` method has a single `View` parameter. This is the view that the user clicks on. You can use the `View getId()` method to find out which view the user clicked on, and then decide how to react.
