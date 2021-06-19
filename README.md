# flutter_about_page

Create an awesome About Page for your Flutter App in 2 minutes<br>
This package is highly inspired from <a href="https://github.com/medyo/android-about-page">android_about_page</a><br>

<img src="https://raw.githubusercontent.com/npsulav/npsulav/main/Flutter%20About%20Page.png" width="80%" alt="Flutter About Page Cover"/>

# Setup

Import the flutter_about_page package.
```dart
import "package:flutter_about_page/flutter_about_page.dart";
```

And Initialize the AboutPage object.
```dart
AboutPage ab = AboutPage();
// You can also set Custom Font Family for description and list items
ab.customStyle(descFontFamily: "Roboto",listTextFontFamily: "RobotoMedium");
```

# Usage

1. Set Image
```dart
ab.setImage("assets/logo.png")
```

2. Set Description
```dart ab.setDescription("lorem ipsum")```

3. Add predefined Social network
The library has already some predefined social networks like :<br>

<li>Facebook<br>
<li>Twitter<br>
<li>Instagram<br>
<li>Youtube<br>
<li>PlayStore<br>

```dart
ab.addFacebook("sulav.parajuli.90"),
ab.addTwitter("sulav"),
ab.addYoutube("UCeVMnSShP_Iviwkknt83cww"),
ab.addPlayStore("com.tripline.radioapp"),
ab.addInstagram("sulav")
```

4. Add Email

```dart
ab.addEmail("lackminds20@gmail.com")
```

5. Add Website

```dart
ab.addWebsite("http://www.facebook.com")
```

6. Add custom Widget
```dart
      ab.addWidget(
            Text(
              "Version 1.2",
              style: TextStyle(
                  fontFamily: "RobotoMedium"
              ),
            ),
          )
  ```

  7. Add Custom List Item
  ```dart
  ab.addItemWidget(Icon(Icons.add), "Title")
  ```

  8. Complete Example
  ```dart

class Example extends StatelessWidget {
  @override
  Widget build(BuildContext context) {

    AboutPage ab = AboutPage();
    ab.customStyle(descFontFamily: "Roboto",listTextFontFamily: "RobotoMedium");

    return Scaffold(
      backgroundColor: Colors.white,
      appBar: AppBar(
        title: Text("About Page"),
        centerTitle: true,
      ),
      body: ListView(

        children: [

          ab.setImage("assets/logo.png"),
          ab.addDescription(" Nullam elit magna, blandit vitae feugiat vel, "),
          ab.addWidget(
            Text(
              "Version 1.2",
              style: TextStyle(
                  fontFamily: "RobotoMedium"
              ),
            ),
          ),
          ab.addGroup("Connect with us"),
          ab.addEmail("lackminds20@gmail.com"),
          ab.addFacebook("sulav.parajuli.90"),
          ab.addTwitter("sulav"),
          ab.addYoutube("UCeVMnSShP_Iviwkknt83cww"),
          ab.addPlayStore("com.tripline.radioapp"),
          ab.addGithub("npsulav"),
          ab.addInstagram("sulav"),
          ab.addWebsite("http://www.facebook.com"),
          ab.addItemWidget(Icon(Icons.add), "title")

        ],
      )
    );
  }
}
  ```

