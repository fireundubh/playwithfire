<!-- TITLE: Database Function Reference -->

If you want to see more resources like this, [become a Patreon supporter!](https://www.patreon.com/fireundubh) 

# Database
## Methods

### GetColumnData

No description entered

#### **Syntax**

`local columnData = Database.GetColumnData(tableName, columnIdx)`

#### **Parameters**

* `tableName`: A string indicating the name of the loaded table
* `columnIdx`: A number indicating the column to retrieve

#### **Return value**

`table`


### GetColumnInfo

No description entered

#### **Syntax**

`local columnInfo = Database.GetColumnInfo(tableName, columnIdx)`

#### **Parameters**

* `tableName`: A string indicating the name of the loaded table
* `columnIdx`: A number indicating the column to retrieve

#### **Return value**

`table`


### GetTableInfo

No description entered

#### **Syntax**

`local tableInfo = Database.GetTableInfo(tableName)`

#### **Parameters**

`tableName`: A string indicating the name of the loaded table

#### **Return value**

`table`


### GetTableLine

No description entered

#### **Syntax**

`local tableLine = Database.GetTableLine(tableName, lineIdx)`

#### **Parameters**

* `tableName`: A string indicating the name of the loaded table
* `lineIdx`: A number indicating the line to retrieve

#### **Return value**

`table`


### LoadTable

No description entered

#### **Syntax**

`local table = Database.LoadTable(tableName)`

#### **Parameters**

`tableName`: A string indicating the name of the table to load

#### **Return value**

`table`