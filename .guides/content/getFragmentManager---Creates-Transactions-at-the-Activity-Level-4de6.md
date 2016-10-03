If we look at what would happen if our `WorkoutDetailFragment` used `getFragmentManager()` to create the fragment transaction to display `StopwatchFragment`.

When someone clicks on a workout, we want the app to display the details of the workout and the stopwatch. `MainActivity` creates a transaction to display `WorkoutDetailFragment`. If we use `getFragmentManager()` to display the `StopwatchFragment` as well, we’ll have two transactions on the back stack.

![](.guides/img/16.png)



