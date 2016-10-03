We want to add `StopwatchFragment` to the frame layout when `WorkoutDetailFragment`’s view gets created. 

![](.guides/img/20.png)

When `WorkoutDetailFragment`’s view gets created, its `onCreateView()` method gets called, so we’ll add a fragment transaction to the `onCreateView()` method to display `StopwatchFragment`. Here’s the code:

![](.guides/img/21.png)

As you can see, the code looks almost identical to the code used to display a fragment inside an activity. The key difference is that we’re displaying a fragment inside another fragment, so we need to use `getChildFragmentManager()` instead of `getFragmentManager()`.


