# ShakeMe - Shake your widget by using this

flutter_shakemywidget - Enables you to shake any widget with property of shake count with duration. You can use any widget to shake

![image description](https://github.com/dheeraj-bhadoria/Flutter-shake-my-widget/blob/main/shakeme.gif)


## Platform Support

| Android | iOS | MacOS | Web | Linux | Windows |
| :-----: | :-: | :---: | :-: | :---: | :-----: |
|   ✔️    | ✔️  |  ✔️   | ✔️  |  ✔️   |   ✔️    |


##Use this package as a library

Depend on it

Run this command:

With Dart:

```yaml

    $ dart pub add flutter_shakemywidget

```

With Flutter:

```yaml

$ flutter pub add flutter_shakemywidget

```

This will add a line like this to your package's pubspec.yaml (and run an implicit dart pub get):

```yaml

    dependencies:
    flutter_shakemywidget: ^1.0.4+1

```


Alternatively, your editor might support dart pub get or flutter pub get. Check the docs for your editor to learn more.
Import it

Now in your Dart code, you can use:

```dart

import 'package:flutter_shakemywidget/flutter_shakemywidget.dart';

```

## Example

```dart

  import 'package:flutter_shakemywidget/flutter_shakemywidget.dart';

  @override
  Widget build(BuildContext context) {
    return Scaffold(
      appBar: AppBar(
        title: Text(widget.title),
      ),
      body: Center(
        child: Container(
          width: 400,
          height: 400,
          color: Colors.red,
          child: Center(
            child: Column(
              crossAxisAlignment: CrossAxisAlignment.center,
              children: [
                InkWell(
                  child: Text("Shake Me", style: TextStyle(color: Colors.black),),
                  onTap: (){
                    // Shake the widget by following code
                    shakeKey.currentState?.shake();
                  },
                ),
                ShakeMe(
                  // 4. pass the GlobalKey as an argument
                  key: shakeKey,
                  // 5. configure the animation parameters
                  shakeCount: 3,
                  shakeOffset: 10,
                  shakeDuration: Duration(milliseconds: 500),
                  // 6. Add the child widget that will be animated
                  child: Text(
                    'Invalid credentials',
                    textAlign: TextAlign.center,
                    style: TextStyle(
                        color: Colors.white,
                        fontSize: 20,
                        fontWeight: FontWeight.bold),
                  ),
                )
              ],
            ),
          ),
        ),
      ), // This trailing comma makes auto-formatting nicer for build methods.
    );
  }
```


## License

MIT License

Copyright (c) 2022 Dheeraj Singh Bhadoria

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.