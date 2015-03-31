# Overview #
A set of drop-in replacements for JavaFX's TableColumn class, which provides a visual editor for users to create filtering.

<table>
<blockquote><tr>
<blockquote><td><img src='https://javafx-filterable-table-columns.googlecode.com/files/demo.png' /></td>
<td><img src='https://javafx-filterable-table-columns.googlecode.com/files/calendar-filter.png' /></td>
</blockquote></tr>
<tr>
<blockquote><td><img src='https://javafx-filterable-table-columns.googlecode.com/files/text-filter.png' /></td>
<td><img src='https://javafx-filterable-table-columns.googlecode.com/files/enum-filter.png' /></td>
<td><img src='https://javafx-filterable-table-columns.googlecode.com/files/number-filter.png' /></td>
</blockquote></tr>
</table></blockquote>

# Use #
### Preferred Method ###
The simplest way to use this library is to use the FilteredTableView class as a drop-in replacement for a TableView.

Then select the type of filtered column you wish to use as a drop-in replacement for the normal TableColumn class.  There are built-in column filters for the following Java types:
  * String
  * Boolean
  * Object Arrays / Enums
  * Calendar
  * Byte
  * Short
  * Integer
  * Long
  * Double
  * Float
  * BigInteger
  * BigDecimal

To react to changes in the table filter, add an EventHandler of type ColumnFilterEvent.FILTER\_CHANGED\_EVENT to your FilteredTableColumn.  You may also access the bound filtered columns on the table via exposed properties to see which columns are currently filtered, and to fetch the column filters.

Each returned filter has a Type and a Value.  You can use this information to determine how to filter properly filter the data in the ObservableList backing your TableView.


# Dependencies #
  * Java 1.7
  * JavaFX 2.2
  * SL4FJ http://www.slf4j.org/


# Misc #
Calendar widget code taken from Christian Schudt from http://myjavafx.blogspot.com/2012/01/javafx-calendar-control.html


# TODO #
  * Allow filters to be set programmatically