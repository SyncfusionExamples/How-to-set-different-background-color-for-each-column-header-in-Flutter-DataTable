# How to set different background color for each column header in Flutter DataTable (SfDataGrid)?.

In this article, we will show you how to set different background color for each column header in [Flutter DataTable](https://www.syncfusion.com/flutter-widgets/flutter-datagrid).

Initialize the [SfDataGrid](https://pub.dev/documentation/syncfusion_flutter_datagrid/latest/datagrid/SfDataGrid-class.html) widget with all the necessary properties. The [GridColumn.label](https://pub.dev/documentation/syncfusion_flutter_datagrid/latest/datagrid/GridColumn/label.html) is used to display the desired widget in a column header. Under the label property of [GridColumn](https://pub.dev/documentation/syncfusion_flutter_datagrid/latest/datagrid/GridColumn-class.html), the corresponding header widget is loaded. Therefore, you can set a different background color for the loaded widget in each column header.

```dart
 @override
  Widget build(BuildContext context) {
    return Scaffold(
      appBar: AppBar(
        title: const Text('Syncfusion Flutter DataGrid'),
      ),
      body: SfDataGrid(
        source: employeeDataSource,
        columnWidthMode: ColumnWidthMode.fill,
        columns: <GridColumn>[
          GridColumn(
              columnName: 'id',
              label: Container(
                  color: Colors.red,
                  padding: const EdgeInsets.all(16.0),
                  alignment: Alignment.center,
                  child: const Text(
                    'ID',
                  ))),
          GridColumn(
              columnName: 'name',
              label: Container(
                  color: Colors.green,
                  padding: const EdgeInsets.all(8.0),
                  alignment: Alignment.center,
                  child: const Text('Name'))),
          GridColumn(
              columnName: 'designation',
              label: Container(
                  color: Colors.blue,
                  padding: const EdgeInsets.all(8.0),
                  alignment: Alignment.center,
                  child: const Text(
                    'Designation',
                    overflow: TextOverflow.ellipsis,
                  ))),
          GridColumn(
              columnName: 'salary',
              label: Container(
                  color: Colors.pink,
                  padding: const EdgeInsets.all(8.0),
                  alignment: Alignment.center,
                  child: const Text('Salary'))),
        ],
      ),
    );
  }
```

You can download this example in [GitHub](https://github.com/SyncfusionExamples/How-to-set-different-background-color-for-each-column-header-in-Flutter-DataTable).