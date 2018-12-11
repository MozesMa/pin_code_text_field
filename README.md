# pin_code_text_field

It's a Flutter widget for entering pin code. Suitable for use cases such as login and OTP.

# Usage
## API
| name | type | default | description |
| --- | --- | --- | --- |
| maxLength | int | 4 | The total length of pin number & the number of pin boxes |
| hideCharacter | bool | false | Show or hide the pin code |
| highlight | bool | false | highlight the focused pin box |
| highlightColor | Color | | Set color of the focused pin box |
| pinBoxDecoration | BoxDecoration| | Customization for the individual pin boxes. |
| pinTextStyle | TextStyle | | TextStyle for styling pin characters |
| maskCharacter | String | "\u25CF" | Special character to mask the pin code. Will only work if `hideCharacter` is set to true |
| pinBoxHeight | double | 70.0 | Height of pin boxes |
| pinBoxWidth | double | 70.0 | Width of pin boxes |
| onDone | void Function(String) | | Callback when the max length of pin code is reached. |

## Example
```dart

class MyHomePageState extends State<MyHomePage> {
  TextEditingController controller = TextEditingController();
  String thisText = "234235";

  @override
  Widget build(BuildContext context) {
    return Scaffold(
      appBar: AppBar(
        title: Text("TEXT"),
      ),
      body: Container(
        child: Column(
          children: <Widget>[
            PinCodeTextField(
              controller: controller,
              hideCharacter: true,
              highlight: true,
              highlightColor: Colors.blue,
              maxLength: 5,
              maskCharacter: "☆",
              pinTextStyle: TextStyle(fontSize: 30.0),
            ),
            RaisedButton(
              onPressed: () {
                setState(() {
                  this.thisText = controller.text;
                });
              },
            ),
            Text(thisText)
          ],
        ),
      ),
    );
  }
}


```

## Wishlist
1. Localization (L-R, R-L)
2. Highlight properties

Star 🌟 to show support!

<img src="https://raw.githubusercontent.com/LiewJunTung/Pin-Code-Text-Field/master/image/phoneusage.gif" alt="pin usage" width="250"/>
<img src="https://raw.githubusercontent.com/LiewJunTung/Pin-Code-Text-Field/master/image/ipad.gif" alt="pin usage" width="500"/>

## More information
[documentation](https://flutter.io/).
