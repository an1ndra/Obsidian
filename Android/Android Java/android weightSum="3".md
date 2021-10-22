Per documentation, `android:weightSum` defines the maximum weight sum, and is calculated as the sum of the `layout_weight` of all the children if not specified explicitly.

Let's consider an example with a `LinearLayout` with horizontal orientation and 3 `ImageViews` inside it. Now we want these `ImageViews` always to take equal space. To acheive this, you can set the `layout_weight` of each `ImageView` to 1 and the `weightSum` will be calculated to be equal to 3 as shown in the comment.
```xml
```xml
 <LinearLayout
                android:layout_width="500dp"
                android:layout_height="20dp" >

                <TextView
                    android:layout_width="0dp"
                    android:layout_height="match_parent"
                    android:layout_weight="3"
                    android:background="@android:color/holo_green_light"
                    android:gravity="center"
                    android:text="30%"
                    android:textColor="@android:color/white" >
                </TextView>

                <TextView
                    android:layout_width="0dp"
                    android:layout_height="match_parent"
                    android:layout_weight="2"
                    android:background="@android:color/holo_blue_bright"
                    android:gravity="center"
                    android:text="20%"
                    android:textColor="@android:color/white" >
                </TextView>

                <TextView
                    android:layout_width="0dp"
                    android:layout_height="match_parent"
                    android:layout_weight="5"
                    android:background="@android:color/holo_orange_dark"
                    android:gravity="center"
                    android:text="50%"
                    android:textColor="@android:color/white" >
                </TextView>
 </LinearLayout>
```