The problem with using two transactions to display the workout is that weird things happen if the user presses the back button.

When a user clicks on a workout, and then clicks the back button, they will expect the screen to go back to how it looked before. But the back button simply undoes the last transaction on the back stack. That means if we create two transactions to the workout detail and the stopwatch, if the user clicks the back button then all that will happen is the stopwatch will be removed. They have to click it again to remove the workout detail section.

![](.guides/img/17.png)