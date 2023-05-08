# HeroIcons

[heroicons](https://heroicons.com/) port to Flutter. This package renders the icons as SVG 
pictures.

This package is a modified clone of the https://pub.dev/packages/heroicons package, with the removal of the icons constants list. The purpose of this modification is to reduce the package size, particularly for web applications. In order to achieve this, we have opted for SVG icons instead of font icons such as Font Awesome, Material Icons, etc., which add approximately 1.5 MB to the web build. By removing the constant list, we were able to reduce the size of the main.dart.js file by approximately 200 KB. Instead, we simply enter the icon name as a string. To use this package, copy/paste the desired icon from https://heroicons.com/.


## Usage

```dart
class MyExampleWidget extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return HeroIcon(
      'calendar',
      style: HeroIconStyle.outline, // Outlined icons are used by default.
      color: Colors.red,
      size: 30,
    );
  }
}
```

## Install

Add `heroicons` package into your `pubspec.yaml`.

```yaml
dependencies:
  heroicons: # Latest version
```

You can also run `flutter pub add heroicons` to quickly add latest version from your CLI.

## Development

Fetch new icons and organize into `assets/`

```
dart tool/fetch_icons.dart
```

Run source code generation to create `heroicons.dart` file with enum entry for every icon.

```
dart tool/generator.dart
```


## License
MIT License

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software with the following conditions:

1. The above copyright notice and this permission notice shall be included in all 
copies or substantial portions of the Software.

2. The software is provided "as is", without warranty of any kind, express or implied, 
including but not limited to the warranties of merchantability, fitness for a particular 
purpose and noninfringement. In no event shall the authors or copyright holders be liable 
for any claim, damages or other liability, whether in an action of contract, tort or 
otherwise, arising from, out of or in connection with the software or the use or other 
dealings in the software.
