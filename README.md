# collection_ext

[![Check Status][check-badge]][github-runs]
[![Code Coverage][codecov-badge]][codecov]
[![MIT][license-badge]][license]

A set of extension functions for [Dart] collections, designed in the purpose of making it easier to write functional-style, concise dart codes.

Working on `Iterable` for example, with `collection_ext`, we can write:

```dart
iterable
  .forEachIndexed((i, x) => /* use index i & element x */)
```

instead of:

```dart
var i = 0;
for (var x in iterable) {
  // use index i & element x
  i++;
}
```

:point_right: See [API Docs] for more details

## Usage

Import all extension functions at once:

```dart
import 'package:collection_ext/all.dart';

Column(
  children: getItems()
    .nonNull
    .mapIndexed((i, item) => Text("#$i ${item.title}"))
    .asList(),
)
```

Or you can import the needed module only, for example:

```dart
import 'package:collection_ext/iterables.dart';

final sum = [2, 4, 6].foldRight(0, (acc, x) => acc + x);
```


[Dart]: https://dart.dev
[github-runs]: https://github.com/xinthink/dart_collection_ext/actions
[check-badge]: https://github.com/xinthink/dart_collection_ext/workflows/check/badge.svg
[codecov-badge]: https://codecov.io/gh/xinthink/dart_collection_ext/branch/master/graph/badge.svg
[codecov]: https://codecov.io/gh/xinthink/dart_collection_ext
[license-badge]: https://img.shields.io/github/license/xinthink/dart_collection_ext
[license]: https://raw.githubusercontent.com/xinthink/dart_collection_ext/master/LICENSE
[API Docs]: https://xinthink.github.io/dart_collection_ext/api/index.html
