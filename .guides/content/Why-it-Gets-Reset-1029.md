The `onCreateView()` method includes a fragment transaction that replaces the stopwatch fragment with a brand-new one. This means that two things happen:

**1)** The activity replays its fragments transactions, putting the stopwatch fragment in the state it was in before the device was rotated.

**2)** The `onCreateView()` method gets rid of the stopwatch fragment the activity reinstated, and replaces it with a brand-new one. As it’s a new version of the fragment, the stopwatch is reset to 0.

To stop this from happening, we need to make sure we only replace the fragment if the `savedInstanceState Bundle` is null. This will mean that a brand-new `StopwatchFragment` is only displayed when the activity is first created.

![](.guides/img/42.png)