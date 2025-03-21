We need to import a comma-separated values (CSV) file, we can Use the pandas library’s read_csv to load a local or hosted CSV file into a Pandas DataFrame, contents of the file before loading. It can be very helpful to see how a dataset is structured beforehand
and what parameters we need to set to load in the file. Second, read_csv has over 30 parameters and
therefore the documentation can be daunting. Fortunately, those parameters are mostly there to allow it
to handle a wide variety of CSV formats.
CSV files get their names from the fact that the values are literally separated by commas (e.g., one row
might be 2,"2015-01-01 00:00:00",0); however, it is common for “CSV” files to use other (termed
“TSVs”). pandas’ sep parameter allows us to define the delimiter used in the file. Although it is not
always the case, a common formatting issue with CSV files is that the first line of the file is used to
define column headers (e.g., integer, datetime, category in our solution). The header parameter
allows us to specify if or where a header row exists. If a header row does not exist, we set
header=None.
The read_csv function returns a Pandas DataFrame
