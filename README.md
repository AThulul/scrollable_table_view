<!-- 
This README describes the package. If you publish this package to pub.dev,
this README's contents appear on the landing page for your package.

For information about how to write a good package README, see the guide for
[writing package pages](https://dart.dev/guides/libraries/writing-package-pages). 

For general information about developing packages, see the Dart guide for
[creating packages](https://dart.dev/guides/libraries/create-library-packages)
and the Flutter guide for
[developing packages and plugins](https://flutter.dev/developing-packages). 
-->

This is a multi axis scrollable data table, that allows you to scroll on both the vertical and horizontal axis, with the header remaining static on the vertical axis. Please look at the demo below.

## Features
### Demo
![](https://github.com/herbertamukhuma/scrollable_table_view/blob/fd47a2acb0ce7d11c848035394650e7e465210df/assets/gifs/scrollable-table-view.gif)

This widget serves the same purpose as a DataTable, with the advantage that it can scroll in both the horizontal and vertical axis, while maintaining the vertical position of the header.

## Getting started

Simply add into your dependencies the following line.

```dart
dependencies:
  scrollable_table_view: ^0.0.2
```

## Usage

```dart
ScrollableTableView(
  columns: [
    "product_id",
    "product_name",
    "price",
  ].map((column) {
    return TableViewColumn(
      label: column,
    );
  }).toList(),
  rows: [
    ["PR1000", "Milk", "20.00"],
    ["PR1001", "Soap", "10.00"],
  ].map((record) {
    return TableViewRow(
      height: 60,
      cells: record.map((value) {
        return TableViewCell(
          child: Text(value),
        );
      }).toList(),
    );
  }).toList(),
);
```

## Additional information

GitHub Repo: https://github.com/herbertamukhuma/scrollable_table_view
