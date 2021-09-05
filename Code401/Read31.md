# Espresso 

- Use Espresso to write concise, beautiful, and reliable Android UI tests.

- Examaple : 

```
@Test
public void greeterSaysHello() {
    onView(withId(R.id.name_field)).perform(typeText("Steve"));
    onView(withId(R.id.greet_button)).perform(click());
    onView(withText("Hello Steve!")).check(matches(isDisplayed()));
}
```

- Each time your test invokes `onView()`, Espresso waits to perform the corresponding UI action or assertion until the following synchronization conditions are met:

  - The message queue is empty.
  
  - There are no instances of AsyncTask currently executing a task.
  
  - All developer-defined idling resources are idle.

<br>
<hr>
<br>


# Packages

- **espresso-core** - Contains core and basic `View` matchers, actions, and assertions. See Basics and Recipes.

- **espresso-web** - Contains resources for `WebView` support.

- **espresso-idling-resource** - Espresso's mechanism for synchronization with background jobs.

- **espresso-contrib** - External contributions that contain `DatePicker`, `RecyclerView` and `Drawer` actions, accessibility checks, and `CountingIdlingResource`.

- **espresso-intents** - Extension to validate and stub intents for hermetic testing.

- **espresso-remote** - Location of Espresso's multi-process functionality.