## Angular 2 Data Table Bootstrap 4

A simple Angular 2 data table, with built-in solutions for features including:

* pagination
* sorting
* row selection (single/multi)
* expandable rows
* column resizing
* selecting visible columns

The component can be used not just with local data, but remote resources too: for example if the sorting and paging happen in the database.

The templates use bootstrap 4 CSS class names, so the component requires a bootstrap .css file to be present in the application using it.

The templates use Font Awesome CSS class names, so the component requires Font Awesome to be present in the application using it.

## Installing:
`npm install ng2-datatable-bootstrap4 --save`

## Usage:

### Custom Sorting

To make use of custom sort functionality, one must add a `[customSort]` binding to the data-table (if necessary for the default sort) or to the data-column (if necessary to sort that column). One must still specify the `[sortBy]` binding and specify the primary property of the bound data set that is being sorted, as this is fundamental to maintaining sort order (ASC or DESC).

The `[customSort]` binding must bind to a function that implements the function signature defined by `DataTableSortCallback`. This function is the same as any standard JS Array.sort() callback, and in fact is actually passed to array.sort() when sorting occurs.
 
If custom sort is not required, then only the `[sortBy]` binding is necessary.

#### Licensing
MIT License


#### ISSUES

- <tbody> tag is repeated unnecessarily - [tbody definition](https://www.w3schools.com/tags/tag_tbody.asp)
- Given a structure like:

```
            <data-table-column
                [header]="'Primary Outlet'"
                [sortable]="true"
                [resizable]="true"
                [property]="'primaryOutletName'"
            >
                <ng-template #dataTableCell let-item="item">
                    {{ item.primaryOutletName }}
                </ng-template>
            </data-table-column>
```

edit
The column is only sortable if the property is in single quotes - removing these means that the row is not sortable - why?
