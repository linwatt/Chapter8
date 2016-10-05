We’ll use the same layout for `StopwatchFragment` as we used in our original Stopwatch app. Replace the contents of *fragment_stopwatch.xml* with the code below:


![](.guides/img/7.png)
```
<Button
  android:id="@+id/reset_button"
  android:layout_width="wrap_content"
  android:layout_height="wrap_content"
  android:layout_below="@+id/stop_button"
  android:layout_centerHorizontal="true"
  android:layout_marginTop="10dp"
  android:onClick="onClickReset"
  android:text="@string/reset" />
</RelativeLayout>
```