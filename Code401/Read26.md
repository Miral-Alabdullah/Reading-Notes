# Application Fundamentals 

* An Android package, which is an archive file with an .apk suffix, contains the contents of an Android app that are required at runtime and it is the file that Android-powered devices use to install the app.

* An Android App Bundle, which is an archive file with an .aab suffix, contains the contents of an Android app project including some additional metadata that is not required at runtime.

## App components : 

 App components are the essential building blocks of an Android app. Each component is an entry point through which the system or a user can enter your app.

  - Activities.

    * An activity is the entry point for interacting with the user. It represents a single screen with a user interface.

	* An activity facilitates the following key interactions between system and app: 
	  
	  1- Keeping track of what the user currently cares about (what is on screen) to ensure that the system keeps running the process that is hosting the activity.
	  
	  2- Knowing that previously used processes contain things the user may return to (stopped activities), and thus more highly prioritize keeping those processes around.
	  
	  3- Helping the app handle having its process killed so the user can return to activities with their previous state restored.
	  
	  4- Providing a way for apps to implement user flows between each other, and for the system to coordinate these flows. (The most classic example here being share.)
	
	**You implement an activity as a subclass of the Activity class.**

	**=>** `onCreate(Bundle)` is where you initialize your activity. Most importantly, here you will usually call `setContentView(int)` with a layout resource defining your UI, and using `findViewById(int)` to retrieve the widgets in that UI that you need to interact with programmatically. 

	<br>
	<br>


  - Services.

    * A service is a general-purpose entry point for keeping an app running in the background for all kinds of reasons. It is a component that runs in the background to perform long-running operations or to perform work for remote processes. A service does not provide a user interface.

	* A service is a general-purpose entry point for keeping an app running in the background for all kinds of reasons. It is a component that runs in the background to perform long-running operations or to perform work for remote processes. A service does not provide a user interface. 

	<br>
	<br>


  - Broadcast receivers.

  * A broadcast receiver is a component that enables the system to deliver events to the app outside of a regular user flow, allowing the app to respond to system-wide broadcast announcements. Because broadcast receivers are another well-defined entry into the app, the system can deliver broadcasts even to apps that aren't currently running.

  	<br>
	<br>

  - Content providers.

  * A content provider manages a shared set of app data that you can store in the file system, in a SQLite database, on the web, or on any other persistent storage location that your app can access. Through the content provider, other apps can query or modify the data if the content provider allows it. 


<br>
<br>



You can start an activity or give it something new to do by passing an Intent to `startActivity()` or `startActivityForResult()`.

With Android 5.0 (API level 21) and later, you can use the JobScheduler class to schedule actions. For earlier Android versions, you can start a service (or give new instructions to an ongoing service) by passing an Intent to `startService()`. You can bind to the service by passing an Intent to `bindService()`.

You can initiate a broadcast by passing an Intent to methods such as `sendBroadcast()`, `sendOrderedBroadcast()`, or `sendStickyBroadcast()`.

You can perform a query to a content provider by calling `query()` on a `ContentResolver.`


