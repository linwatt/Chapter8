When we wanted to display a fragment in an activity, we created the fragment transaction using the activity’s fragment manager using the `getFragmentManager` call:

![](.guides/img/14.png)

The `getFragmentManager()` method gets the fragment manager associated with the **fragment’s parent activity**. This means that the fragment transaction is linked to the activity.

When you want to display fragments inside another fragment, you need to use a slightly different fragment manager. You need to use the fragment manager associated with the **parent fragment instead**. This means that any fragment transactions will be linked to the parent fragment rather than the activity.

To get the fragment manager that’s associated with the parent fragment, you use the `getChildFragmentManager()` method. This means that the code to begin the transaction now calls `getChildFragmentManager`:

![](.guides/img/15.png)