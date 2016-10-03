- Fragments can contain other fragments.

- If you’re nesting a fragment in another fragment, you need to add the nested fragment programmatically in Java code.

- When you perform transactions on a nested fragment, use `getChildFragmentManager()` to create the transaction.

- If you use the `android:onClick` attribute in a fragment, Android will look for a method of that name in the fragment’s parent activity.

- Instead of using the `android:onClick attribute` in a fragment, make the fragment implement the `View.OnClickListener` interface and implement its `onClick()` method.

- When the device configuration changes, the activity and its fragments get destroyed. When the activity is re-created, it replays its fragment transactions in the `onCreate()` method’s call to `setContentView()`.

- The fragment’s `onCreateView()` method runs after the activity has replayed its fragment transactions.
