# Understand Tasks and Back Stack 

- A task is a collection of activities that users interact with when performing a certain job.

- The activities are arranged in a stack—the back stack)—in the order in which each activity is opened.

- The device Home screen is the starting place for most tasks.

- When the user touches an icon in the app launcher (or a shortcut on the Home screen), that app's task comes to the foreground.

- If no task exists for the app (the app has not been used recently), then a new task is created and the "main" activity for that app opens as the root activity in the stack.

![](https://developer.android.com/images/fundamentals/diagram_backstack.png)

- When all activities are removed from the stack, the task no longer exists.

![](https://developer.android.com/images/fundamentals/diagram_multitasking.png)

- A task can then return to the "foreground" so users can pick up where they left off.

- Suppose, for example, that the current task (Task A) has three activities in its stack—two under the current activity. 

- The user presses the Home button, then starts a new app from the app launcher.

- When the Home screen appears, Task A goes into the background.

- When the new app starts, the system starts a task for that app (Task B) with its own stack of activities.

- After interacting with that app, the user returns Home again and selects the app that originally started Task A. Now, Task A comes to the foreground—all three activities in its stack are intact and the activity at the top of the stack resumes.

- At this point, the user can also switch back to Task B by going Home and selecting the app icon that started that task (or by selecting the app's task from the Recents screen)


<hr>
<br>


-When Activity A starts Activity B, Activity A is stopped, but the system retains its state (such as scroll position and text entered into forms).

- If the user presses the Back button while in Activity B, Activity A resumes with its state restored.


- When the user leaves a task by pressing the Home button, the current activity is stopped and its task goes into the background.

- The system retains the state of every activity in the task. If the user later resumes the task by selecting the launcher icon that began the task, the task comes to the foreground and resumes the activity at the top of the stack.


- If the user presses the Back button, the current activity is popped from the stack and destroyed. The previous activity in the stack is resumed.

- When an activity is destroyed, the system does not retain the activity's state.


- Activities can be instantiated multiple times, even from other tasks.




<hr>
<br>

The way Android manages tasks and the back stack, as described above—by placing all activities started in succession in the same task and in a "last in, first out" stac. 

However, you might decide that you want to interrupt the normal behavior. Perhaps you want an activity in your app to begin a new task when it is started (instead of being placed within the current task); or, when you start an activity, you want to bring forward an existing instance of it (instead of creating a new instance on top of the back stack); or, you want your back stack to be cleared of all activities except for the root activity when the user leaves the task.

You can do these things and more, with attributes in the `<activity>` manifest element and with flags in the intent that you pass to `startActivity()`.

In this regard, the principal `<activity>` attributes you can use are:

  `taskAffinity`

  `launchMode`

  `allowTaskReparenting`

  `clearTaskOnLaunch`
 
  `alwaysRetainTaskState`

  `finishOnTaskLaunch`

And the principal intent flags you can use are:

  `FLAG_ACTIVITY_NEW_TASK`

  `FLAG_ACTIVITY_CLEAR_TOP`

  `FLAG_ACTIVITY_SINGLE_TOP`
