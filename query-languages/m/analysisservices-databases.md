---
title: "AnalysisServices.Databases | Microsoft Docs"
ms.date: 4/16/2018
ms.prod: power-query
ms.reviewer: owend
ms.topic: reference
author: minewiskan
ms.author: owend
manager: kfile
---
# AnalysisServices.Databases
<code>AnalysisServices.Databases(**server** as text, optional **options** as nullable record) as table</code>

## About
Returns databases on an Analysis Services instance, <code>server</code>. An optional record parameter, <code>options</code>, may be provided to specify additional properties. The record can contain the following fields: 
* <code>TypedMeasureColumns</code> : A logical value indicating if the types specified in the multidimensional or tabular model will be used for the types of the added measure columns. When set to false, the type &quot;number&quot; will be used for all measure columns. The default value for this option is false. 
* <code>Culture</code> : A culture name specifying the culture for the data. This corresponds to the &#39;Locale Identifier&#39; connection string property.
* <code>CommandTimeout</code> : A duration which controls how long the server-side query is allowed to run before it is canceled. The default value is driver-dependent.
* <code>ConnectionTimeout</code> : A duration which controls how long to wait before abandoning an attempt to make a connection to the server. The default value is driver-dependent.
* <code>SubQueries</code> : A number (0, 1 or 2) that sets the value of the &quot;SubQueries&quot; property in the connection string. This controls the behavior of calculated members on subselects or subcubes. (The default value is 2).
* <code>Implementation</code>