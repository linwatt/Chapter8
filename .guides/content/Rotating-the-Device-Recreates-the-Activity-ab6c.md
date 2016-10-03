As you already know, when you’re running an app and rotate the device, the activity that’s running gets destroyed and re-created. All variables in the activity code are set back to their default values; if you want to save these values before the activity’s destroyed, you need to use the activity’s `onSaveInstanceState()` method.

But what if the activity contains a fragment? You’ve already seen that the activity and fragment lifecycles are closely related, but what happens to the fragment when you rotate the device?

### What happens to the fragment when you rotate the device
**1) An activity contains a fragment.**

![](.guides/img/38.png)

**2) When the user rotates the device, the activity is destroyed along with the fragment.**

![](.guides/img/39.png)

**3) The activity is re-created and its onCreate() method is called.**
The `onCreate()` method includes a call to `setContentView()`.
![](.guides/img/40.png)

**4) When the activity’s setContentView() method runs, it reads the activity’s layout and replays its fragment transactions.** 
The fragment is re-created in line with its latest transaction.

### Why does ours reset the stopwatch?

When you rotate the device, the fragment *should* go back to the same state it was in before the device was rotated. So why, in our case, has the stopwatch been reset? To get some clues, let’s look at `theWorkoutDetailFragment onCreateView()` method.
