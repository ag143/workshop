- Text.replace
    - replace first 6 letter of column [SSN]
`Text.Replace([SSN], Text.Start([SSN],6), "xxx-xx")`

[Table.ReplaceValue(table as table, oldValue as any, newValue as any, replacer as function, columnsToSearch as list)](https://docs.microsoft.com/en-us/powerquery-m/table-replacevalue)