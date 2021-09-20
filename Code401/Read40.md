# Get the last known location 

- Using the Google Play services location APIs, your app can request the last known location of the user's device. 

## Create location services client

In `onCreate()` : 

```
private FusedLocationProviderClient fusedLocationClient;

// ..

@Override
protected void onCreate(Bundle savedInstanceState) {
    // ...

    fusedLocationClient = LocationServices.getFusedLocationProviderClient(this);
}
```

## Get the last known location

- `getLastLocation()`

- `getCurrentLocation()`

### LocationRequest

* `setInterval()`

* `setFastestInterval()`

* `setPriority()`

