
# Rapport

##### 1 - Activities

Creating a second activity was done through right-clicking the app-folder, clicking New -> Activity -> Empty activity.
This results in the creation of an activity that resembles the first main activity.

```
public class MainActivity2 extends AppCompatActivity {

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main2);
    }
}
```

One can navigate to the second activity through the click of a button.

![](clickme.png)


##### 2 - Fragment

In the second activity I placed a fragment which will contain a future element.

![](fragment.png)

This fragment has a similar structure of code to an activity but with some variation to their functionality.
While they're still able to be utilized in a similar manner, the approach to certain things differs.
For example, when I wanted to load a url I were unable to do so unless I utilized the following code.

```
    public void onViewCreated(View view, Bundle savedInstanceState) {
        super.onViewCreated(view, savedInstanceState);
        WebView my_WebView = view.findViewById(R.id.webview_gif);
        my_WebView.loadUrl("file:///android_asset/hello.gif"); // presents gif
    }
```

I believe there are other ways to display what I strove to display, but this worked for me.
An alternative to displaying the gif through this could be to display an internal html with the gif as an element.

Something I wanted to do was to overlay a string on top of the gif where I greeted the person.
This would be done through a textinput above the button and the value of the id would be brought to the fragment where the presented text would be modified per input.

You are then greeted by the following gif

![](/app/src/main/assets/hello.gif)

Source: Movie - Forrest Gump (1994)