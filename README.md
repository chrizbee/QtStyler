## Basic Overview
**QtStyler** is a `QObject` class to style QtWidgets.
See [QtShowcase](https://github.com/chrizbee/QtShowcase) for an example and screenshots.

## Usage

To use `QtStyler` in your application simply clone this repository to your applications root folder.

```bash
cd YourApplication
git clone https://github.com/chrizbee/QtStyler
```

Additionally the project needs to be icluded from `YourApplication.pro`.

```qmake
include(QtStyler/qtstyler.pri)
```

The easiest way to use `QtStyler` is with a `QComboBox`.

```cpp
QtStyler *styler = new QtStyler(this);
QComboBox *combo = new QComboBox(this);
combo->addItems(styler->availableStyles());
combo->setCurrentText(styler->currentStyle());
connect(combo, &QComboBox::currentTextChanged, styler, &QtStyler::setStyle);
connect(styler, &QtStyler::styleChanged, combo, &QComboBox::setCurrentText);
```

## Built With

* [Qt5](https://www.qt.io/) - The UI framework used

## Versioning

We use [SemVer](http://semver.org/) for versioning.

## Authors

- [chrizbee](https://github.com/chrizbee)

See also the list of [contributors](https://github.com/chrizbee/QtStyler/contributors) who participated in this project.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
