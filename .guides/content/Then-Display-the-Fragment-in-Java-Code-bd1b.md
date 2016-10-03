We want to add `StopwatchFragment` to the frame layout when `WorkoutDetailFragment`’s view gets created. We’ll do this in a similar way to how we did in Chapter 7, by replacing the fragment that’s displayed in the frame layout using a fragment transaction. Here’s a reminder of the code we used in Chapter 7:


![](.guides/img/13.png)

We used the above code to replace the fragment that’s displayed in an activity, but this time there’s a key difference. Instead of replacing the fragment that’s displayed in an *activity*, we want to replace the fragment that’s displayed in a *fragment*. This means that we need to make a small change to how we create the fragment transaction.
