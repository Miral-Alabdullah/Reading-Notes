# Save data in a local database using Room :

- When the device cannot access the network, the user can still browse that content while they are offline.

- The Room persistence library provides an abstraction layer over SQLite to allow fluent database access while harnessing the full power of SQLite. => **What Is SQLite?**

SQLite is a C-language library that implements a small, fast, self-contained, high-reliability, full-featured, SQL database engine. SQLite is the most used database engine in the world. SQLite is built into all mobile phones and most computers and comes bundled inside countless other applications that people use every day.

<br>
<br>

To use Room in the app, add the following dependencies to the app's build.gradle file:

```
dependencies {
    def room_version = "2.3.0"

    implementation "androidx.room:room-runtime:$room_version"
    annotationProcessor "androidx.room:room-compiler:$room_version"

    // optional - RxJava2 support for Room
    implementation "androidx.room:room-rxjava2:$room_version"

    // optional - RxJava3 support for Room
    implementation "androidx.room:room-rxjava3:$room_version"

    // optional - Guava support for Room, including Optional and ListenableFuture
    implementation "androidx.room:room-guava:$room_version"

    // optional - Test helpers
    testImplementation "androidx.room:room-testing:$room_version"

    // optional - Paging 3 Integration
    implementation "androidx.room:room-paging:2.4.0-alpha04"
}

```

<br>
<br>

## Primary components :

1- **database class** => that holds the database and serves as the main access point for the underlying connection to your app's persisted data.

2- **Data entities** => that represent tables in your app's database.

3- **Data access objects (DAOs)** that provide methods that your app can use to query, update, insert, and delete data in the database.


- The database class provides your app with instances of the DAOs associated with that database.

- The app can use the DAOs to retrieve data from the database as instances of the associated data entity objects.

- The app can also use the defined data entities to update rows from the corresponding tables, or to create new rows for insertion.


## The relationship between the different components of Room

![!](https://developer.android.com/images/training/data-storage/room_architecture.png)


<br>
<hr>
<br>

# Defining data using Room entities 

## Anatomy of an entity :

```
@Entity
public class User { //tableName to change the table name (it's a property).
    @PrimaryKey
    public int id; //@ColumnInfo to change the field name (it's an annotation).

    public String firstName;
    public String lastName;
}
```

## Define a composite primary key : 

```
@Entity(primaryKeys = {"firstName", "lastName"})
public class User {
    public String firstName;
    public String lastName;
}

```

## Ignore fields

```
@Entity
public class User {
    @PrimaryKey
    public int id;

    public String firstName;
    public String lastName;

    @Ignore
    Bitmap picture;
}

```

<br>
<hr>
<br>


# Define relationships between objects :


one-to-one => We create a new class to hold the relation

```
public class UserAndLibrary {
    @Embedded public User user;
    @Relation(
         parentColumn = "userId",
         entityColumn = "userOwnerId"
    )
    public Library library;
}


@Transaction
@Query("SELECT * FROM User")
public List<UserAndLibrary> getUsersAndLibraries();

```

<br>

one-to-many => each instance of the parent entity corresponds to zero or more instances of the child entity, but each instance of the child entity can only correspond to exactly one instance of the parent entity.

```
public class UserWithPlaylists {
    @Embedded public User user;
    @Relation(
         parentColumn = "userId",
         entityColumn = "userCreatorId"
    )
    public List<Playlist> playlists;
}

@Transaction
@Query("SELECT * FROM User")
public List<UserWithPlaylists> getUsersWithPlaylists();
```

<br>

many-to-many => 

```
public class PlaylistWithSongs {
    @Embedded public Playlist playlist;
    @Relation(
         parentColumn = "playlistId",
         entityColumn = "songId",
         associateBy = @Junction(PlaylistSongCrossref.class)
    )
    public List<Song> songs;
}

public class SongWithPlaylists {
    @Embedded public Song song;
    @Relation(
         parentColumn = "songId",
         entityColumn = "playlistId",
         associateBy = @Junction(PlaylistSongCrossref.class)
    )
    public List<Playlist> playlists;
}


@Transaction
@Query("SELECT * FROM Playlist")
public List<PlaylistWithSongs> getPlaylistsWithSongs();

@Transaction
@Query("SELECT * FROM Song")
public List<SongWithPlaylists> getSongsWithPlaylists();

```

