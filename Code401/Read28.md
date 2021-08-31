# Create dynamic lists with RecyclerView.

- RecyclerView makes it easy to efficiently display large sets of data.

- You supply the data and define how each item looks, and the RecyclerView library dynamically creates the elements when they're needed.

- RecyclerView recycles those individual elements.

- When an item scrolls off the screen, RecyclerView doesn't destroy its view.

- Instead, RecyclerView reuses the view for new items that have scrolled onscreen.

- This reuse vastly improves performance, improving your app's responsiveness and reducing power consumption.

## Key classes


- `RecyclerView` is the `ViewGroup` that contains the views corresponding to your data. It's a view itself, so you add `RecyclerView` into your layout the way you would add any other UI element.

- Each individual element in the list is defined by a view holder object. When the view holder is created, it doesn't have any data associated with it. After the view holder is created, the RecyclerView binds it to its data. You define the view holder by extending `RecyclerView.ViewHolder`.

- The `RecyclerView` requests those views, and binds the views to their data, by calling methods in the adapter. You define the adapter by extending `RecyclerView.Adapter`.

- The layout manager arranges the individual elements in your list. You can use one of the layout managers provided by the `RecyclerView` library, or you can define your own. Layout managers are all based on the library's `LayoutManager` abstract class.


<br>
<hr>
<br>


* `Adapter` – Provides the data model and responsible for rendering the views for the individual cell.

* `ViewHolder` – Contains instances for all views that are filled by the data of the entry.

* `LayoutManager` – Allows us to set the `LayoutManagers` at runtime. eg. `LinearLayoutManager`, `StaggeredLayoutManager`, `GridLayoutManager`.