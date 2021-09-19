# Allowing Other Apps to Start Your Activity 

- To build a social app that can share messages or photos with the user's friends, you should support the `ACTION_SEND` intent. 

- To allow other apps to start your activity in this way, you need to add an <intent-filter> element in your manifest file for the corresponding <activity> element.

- When an app calls startActivity() or startActivityForResult(), with an implicit intent, the system finds which activity (or activities) can respond to the intent.


# Add an Intent Filter

## Action

  * A string naming the action to perform. Usually one of the platform-defined values such as `ACTION_SEND` or `ACTION_VIEW`.

  * Specify this in your intent filter with the <action> element.

## Data

  * A description of the data associated with the intent.
  
  * Specify this in your intent filter with the <data> element.

## Category

  * Provides an additional way to characterize the activity handling the intent.
  
  * All implicit intents are defined with CATEGORY_DEFAULT by default.


### In your intent filter, you can declare which criteria your activity accepts by declaring each of them with corresponding XML elements nested in the <intent-filter> element.

```
<activity android:name="ShareActivity">
    <intent-filter>
        <action android:name="android.intent.action.SEND"/>
        <category android:name="android.intent.category.DEFAULT"/>
        <data android:mimeType="text/plain"/>
        <data android:mimeType="image/*"/>
    </intent-filter>
</activity>
```

- Each incoming intent specifies only one action and one data type, but it's OK to declare multiple instances of the <action>, <category>, and <data> elements in each <intent-filter>.


## Handle the Intent in Your Activity

- As your activity starts, call `getIntent()` to retrieve the `Intent` that started the activity. You can do so at any time during the lifecycle of the activity, but you should generally do so during early callbacks such as `onCreate()` or `onStart()`.

```
@Override
protected void onCreate(Bundle savedInstanceState) {
    super.onCreate(savedInstanceState);

    setContentView(R.layout.main);

    // Get the intent that started this activity
    Intent intent = getIntent();
    Uri data = intent.getData();

    // Figure out what to do based on the intent type
    if (intent.getType().indexOf("image/") != -1) {
        // Handle intents with image data ...
    } else if (intent.getType().equals("text/plain")) {
        // Handle intents with text ...
    }
}
```