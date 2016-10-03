There are two things you need to do in order to get buttons in a fragment to call methods in the fragment instead of the activity:

**1) Remove references to `android:onClick` in the fragment layout.**
Buttons attempt to call methods in the activity when the `android:onClick` attribute is used, so these need to be removed from the fragment layout.
**2) Bind the buttons to methods in the fragment by implementing an `onClickListener`.**
This will ensure that the right methods are called when the buttons are clicked.


Let’s do this now in our `StopwatchFragment`.
