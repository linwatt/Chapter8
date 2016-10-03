We’re going to add the `StopwatchFragment` inside the `WorkoutDetailFragment`. The user interface of `MainActivity` on a tablet will link together like this:


![](.guides/img/10.png)


### We need to add it Programmatically
There are two ways of adding a fragment, using a *layout* file and writing *Java code*. If you add a fragment to another fragment’s layout the result can be flaky, so we’re going to add the `StopwatchFragment` to the `WorkoutDetailFragment` using *Java code*. That means we’re going to do it in almost the same way that we added the `WorkoutDetailFragment` to the activity. 


**If you nest fragments inside fragments, you need to add the nested fragment programmatically**