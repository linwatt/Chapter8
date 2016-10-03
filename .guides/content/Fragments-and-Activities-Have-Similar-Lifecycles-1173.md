If we look at the lifecycles of fragments and activities, we’ll see that they’re very similar:

<table style="width:100%">
  <tr>
    <th>Lifecycle Method</th>
    <th>Activity?</th>
    <th>Fragment?</th>
  </tr>
  <tr>
    <td>onAttach()</td>
    <td></td>
    <td>X</td>
  </tr>
  <tr>
    <td>onCreate()</td>
    <td>X</td>
    <td>X</td>
  </tr>
  <tr>
    <td>onCreateView()</td>
    <td></td>
    <td>X</td>
  </tr>
  <tr>
    <td>onActivityCreated()</td>
    <td></td>
    <td>X</td>
  </tr>
  <tr>
    <td>onStart()</td>
    <td>X</td>
    <td>X</td>
  </tr>
  <tr>
    <td>onPause()</td>
    <td>X</td>
    <td>X</td>
  </tr>
  <tr>
    <td>onResume()</td>
    <td>X</td>
    <td>X</td>
  </tr>
  <tr>
    <td>onStop()</td>
    <td>X</td>
    <td>X</td>
  </tr>
  <tr>
    <td>onDestoryView()</td>
    <td></td>
    <td>X</td>
  </tr>
    <tr>
    <td>onRestart()</td>
    <td>X</td>
    <td></td>
  </tr>
  <tr>
    <td>onDestroy()</td>
    <td>X</td>
    <td>X</td>
  </tr>
  <tr>
    <td>onDetach()</td>
    <td></td>
    <td>X</td>
  </tr>
</table>

Fragment lifecycle methods are almost the same as activity lifecycle methods, but there’s one major difference: activity lifecycle methods are **protected** and fragment lifecycle methods are **public**. And we’ve already seen that the way fragments create a layout from a layout resource file is different. 

Also, in a fragment, we can’t call methods like `findViewById()` directly. Instead, we need to find a reference to a `View` object, and then call `view.findViewById()`.
