### The onClick attribute calls methods in the activity, not the fragment
There’s a big problem with using the `android:onClick` attribute to say which method should be called when a view is clicked. The attribute specifies which method should be called in the **current activity**. This is fine when the views are in an *activity*’s layout. When the views are in a *fragment* this leads to problems. Instead of calling methods in the fragment, Android calls methods in the parent activity. If it can’t find the methods in this activity, the app crashes.

![](.guides/img/27.png)

The problem occurs regardless of whether the fragment is included in an activity, or nested inside another fragment. It applies to *all* fragments.

Now we could move the methods out of the fragment into the activity, but that approach has a major disadvantage. It would mean that the fragment is no longer self-contained—if we wanted to reuse the fragment in another activity, we’d need to include the code in that activity too. Instead, we’ll deal with it in the fragment.
