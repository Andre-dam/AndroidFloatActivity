<img src="https://github.com/Andre-dam/AndroidFloatActivity-tutorial/blob/master/sample.gif" width="300">

# AndroidFloatingActivity-tutorial

This is a simple, minimalist, easy-to-use Floating Activity class.


## Setup
1 - The first step is to import the FloatingActivity class, to keep it simple just create a new class in you project, name it FloatingActivity and paste the code inside, after that make your Activity extends that class.
```Kotlin
class MyActivity: FloatingActivity(){
  ...
}
```
2 - Then, add the following atributes to your Activity theme:
```xml
        <item name="android:windowAnimationStyle">@null</item>
        <item name="android:windowIsTranslucent">true</item>
        <item name="android:windowBackground">@android:color/transparent</item>
        <item name="android:windowContentOverlay">@null</item>
        <item name="android:windowNoTitle">true</item>
        <item name="android:windowIsFloating">false</item>
        <item name="android:backgroundDimEnabled">true</item>
```
> *Note: the backgroundDimEnabled attribute changes between darker and lighter background.*

## Usage
After setting up everything, just call setContentView method passing your layout, vertical and horizontal padding values:
```Kotlin
  fun setContentView(layoutResID: Int, verticalDP: Int, horizontalDP: Int)
```
> *Note: the padding value defines the amount of screen your activity will occupy.
Example:
```Kotlin
class MyActivity: FloatingActivity(){
    override fun onCreate(savedInstanceState: Bundle?) {
        super.onCreate(savedInstanceState)
        setContentView(R.layout.activity_main,20,8)
    }
    ...
}
```

