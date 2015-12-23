# ExpandTextView
Android Expandable Expand TextView with RelativeLayout

ExpandTextView is an Android library that allows developers to easily create an TextView with RelativeLayout
which can expand/collapse just like the Google Play's app description.
Feel free to use it all you want in your Android apps provided that you cite this project.

Download
--------

Current version: [0.1.2]

Gradle:
```groovy
compile 'com.github.dubulee:expandtextview:0.1.2'
```

How to Use
------
Using the library is really simple.

The important thing to note is that the view Ids for TextView and ImageButton must be set to
"@id/expandable_text" and "@id/expand_collapse" respectively for this library to work.

Also, you can optionally set the following attributes in your layout xml file to customize the behavior
of the ExpandableTextView.

 * `maxCollapsedLines` (defaults to 8)
 The maximum number of text lines allowed to be shown when the TextView gets collapsed

 * `animDuration` (defaults to 300ms)
 Duration of the Animation for the expansion/collapse

 * `animAlphaStart` (defaults to 0.7f)
 Alpha value of the TextView when the animation starts
 (NOTE)
 Set this value to 1 if you want to disable the alpha animation.

 * `expandDrawable`
 Customize a drawable set to ImageButton to expand the TextView

 * `collapseDrawable`
 Customize a drawable set to ImageButton to collapse the TextView

```xml
  <!-- sample xml -->
  <com.github.dubu.expandabletextview.ExpandableTextView
        android:id="@+id/expand_text_view"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        expandTextView:animAlphaStart="1"
        expandTextView:maxCollapsedLines="4"
        expandTextView:animDuration="200"
        android:background="@android:color/white">

        <TextView
            android:id="@+id/expandable_text"
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:layout_marginLeft="10dp"
            android:layout_marginRight="10dp"
            android:layout_marginTop="8dp"
            android:textColor="@android:color/black"
            android:textSize="16sp"/>

        <RelativeLayout
            android:id="@+id/expand_collapse"
            android:layout_width="match_parent"
            android:layout_height="100dp"
            android:layout_margin="16dp"
            android:background="@android:color/holo_orange_light">
            
            <!-- Something Design -->
        </RelativeLayout>
    </com.github.dubu.expandabletextview.ExpandableTextView>
```

Welcome the pull request
-------------------------

License
-------------------------
Copyright 2015 DUBULEE

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

       http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.
