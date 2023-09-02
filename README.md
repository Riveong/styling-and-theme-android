# styling-and-theme-android
styling and theme implementation (android w xml)  
previously we implemented layouting thingy, now we are gonna make style and theme!  

### styling  
so here I was thinking about life, then I remember that CSS exists among html. in xml we could do the same thing!  
here's the idea:  
- Change the description to kinda gray color
- padding (ofc)
- I want the style to be reuseable

so how do we do that?  
we could make template on *res > values > themes > themes.xml*  
```xml
<style name="textcontent">
        <item name="android:padding">20dp</item>
</style>
```
the code above made theme style for textcontent globally.  
while the code below made theme for submissive textcontent specifically.
```xml
<style name="textcontent.submissive">
        <item name="android:textColor">@color/colorSubtitle</item>
</style>
```

 This also means that textcontent.submissive inherits the style from textcontent.
![](https://media.discordapp.net/attachments/1023598916857499680/1147612353257558136/image.png?width=964&height=676)  
### color theme  
we also could make color scheme for our app  
declare them on *res > values > colors.xml*  
here's the example of color declaration  
```xml
<?xml version="1.0" encoding="utf-8"?>
<resources>
    <color name="black">#FF000000</color>
    <color name="white">#FFFFFFFF</color>
    <color name="gray">#607D8B</color>
    <color name="gray_light">#B0BEC5</color>
    <color name="gray_dark">#455A64</color>
    <color name="orange">#FF5722</color>
    <color name="orange_light">#FFAB91</color>
    <color name="orange_dark">#E64A19</color>
    <color name="colorSubtitle">#757575</color>
    <color name="blue_light">#428EFF</color>
    <color name="blue_dark">#1044FF</color>
</resources>
```
don't forget to put them to themes.xml too!  
```xml
    <style name="Base.Theme.Layouting" parent="Theme.Material3.DayNight">
        <!-- Customize your light theme here. -->
        <!-- <item name="colorPrimary">@color/my_light_primary</item> -->
        <item name="colorPrimary">@color/blue_light</item>
        <item name="colorOnPrimary">@color/white</item>


        <item name="colorSecondary">@color/blue_dark</item>
        <item name="colorOnSecondary">@color/black</item>




    </style>
```


```
        <item name="colorPrimary">@color/blue_light</item>
        <item name="colorOnPrimary">@color/white</item>
```
these lines would also change your primary color to bluelight and white  
here's the example of the changes  
![](https://media.discordapp.net/attachments/1023598916857499680/1147613830088753244/image.png?width=296&height=676)
