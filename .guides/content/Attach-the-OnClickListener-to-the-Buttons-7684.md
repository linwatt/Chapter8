To make the views respond to clicks, you need to call each view’s `setOnClickListener()` method. The `setOnClickListener()` method takes an `OnClickListener` object as a parameter. As `StopwatchFragment` implements the `OnClickListener` interface, we can use `this` to pass the fragment as the `OnClickListener`.

As an example, here’s how you attach the `OnClickListener` to the Start button:


![](.guides/img/32.png)

The call to each view’s `setOnClickListener()` method needs to be made after the fragment’s views have been created. This means they need to go in the `StopwatchFragment` `onCreateView()` method like this:

![](.guides/img/33.png)
