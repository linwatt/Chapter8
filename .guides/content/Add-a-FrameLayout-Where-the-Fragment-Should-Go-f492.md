To add a fragment programmatically using Java code, you add a frame layout to your layout where you want the fragment to go. 

![](.guides/img/12.png)

We want to put our `StopwatchFragment` in `WorkoutDetailFragment` underneath the workout name and description. We’ll add a frame layout underneath the name and description text views that will be used to contain `StopwatchFragment`:


![](.guides/img/11.png)

Now we've added the frame layout to the layout, we need to add the fragment to it in our java code.