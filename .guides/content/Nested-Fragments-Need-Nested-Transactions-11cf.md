The problem of having multiple transactions for nested fragments was why the child fragment manager was created. The transactions created by the child fragment manager fit inside the main transactions. So when we add the `StopwatchFragment` to the `WorkoutDetailFragment` using a transaction created by `getChildFragmentManager().beginTransaction()`, the transactions are nested like this:

![](.guides/img/18.png)

The back stack has one transaction that contains the second transaction. When someone presses the back button, the *display-the-detail-fragment* transaction is undone, and that will mean that the *display-the-stopwatch-fragment* transaction is undone at the same time. When the user presses the back button, the app behaves correctly:

![](.guides/img/19.png)