Per documentation, `android:weightSum` defines the maximum weight sum, and is calculated as the sum of the `layout_weight` of all the children if not specified explicitly.

Let's consider an example with a `LinearLayout` with horizontal orientation and 3 `ImageViews` inside it. Now we want these `ImageViews` always to take equal space. To acheive this, you can set the `layout_weight` of each `ImageView` to 1 and the `weightSum` will be calculated to be equal to 3 as shown in the comment.
```xml
	<LinearLayout
    android:layout_width="wrap_content"
    android:layout_height="wrap_content"
    <!-- android:weightSum="3" -->
    android:orientation="horizontal"
    android:layout_gravity="center">

   <ImageView
       android:layout_height="wrap_content"       
       android:layout_weight="1"
       android:layout_width="0dp"/>
  .....
```
`weightSum` is useful for having the layout rendered correctly for any device, which will not happen if you set width and height directly.

Result:
![[Pasted image 20211022185134.png]]