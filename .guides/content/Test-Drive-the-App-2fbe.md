What happens when we run the code?

![](.guides/img/44.png)

The stopwatch keeps going. Even though rotating the device means that the activity is destroyed, the fragment transactions replay successfully. We’re no longer replacing `StopwatchFragment` with a brand-new fragment.
