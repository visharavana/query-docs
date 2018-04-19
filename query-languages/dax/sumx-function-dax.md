---
title: "SUMX Function (DAX) | Microsoft Docs"
ms.prod: dax
ms.date: 4/13/2018
ms.reviewer: owend
ms.topic: reference
author: minewiskan
ms.author: owend
manager: kfile
---
# SUMX Function (DAX)
Returns the sum of an expression evaluated for each row in a table.  
  
## Syntax  
  
```  
SUMX(<table>, <expression>)  
```  
  
#### Parameters  
  
|Term|Definition|  
|--------|--------------|  
|**table**|The table containing the rows for which the expression will be evaluated.|  
|**expression**|The expression to be evaluated for each row of the table.|  
  
## Return Value  
A decimal number.  
  
## Remarks  
The SUMX function takes as its first argument a table, or an expression that returns a table. The second argument is a column that contains the numbers you want to sum, or an expression that evaluates to a column.  
  
Only the numbers in the column are counted. Blanks, logical values, and text are ignored.  
  
To see some more complex examples of SUMX in formulas, see [ALL Function &#40;DAX&#41;](all-function-dax.md) and [CALCULATETABLE Function &#40;DAX&#41;](calculatetable-function-dax.md).  
  
## Example  
The following example first filters the table, InternetSales, on the expression, `ShippingTerritoryID = 5`, and then returns the sum of all values in the column, Freight. In other words, the expression returns the sum of freight charges for only the specified sales area.  
  
```  
=SUMX(FILTER(InternetSales, InternetSales[SalesTerritoryID]=5),[Freight])  
```  
If you do not need to filter the column, use the SUM function. The SUM function is similar to the Excel function of the same name, except that it takes a column as a reference.  
  
## See Also  
[SUM Function &#40;DAX&#41;](sum-function-dax.md)  
[Statistical Functions &#40;DAX&#41;](statistical-functions-dax.md)  
  