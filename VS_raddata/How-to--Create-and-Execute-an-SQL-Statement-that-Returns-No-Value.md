---
title: "How to: Create and Execute an SQL Statement that Returns No Value"
ms.custom: na
ms.date: 10/01/2016
ms.devlang: 
  - VB
  - CSharp
  - C++
  - aspx
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 612d3046-0cfa-4d90-be6e-c4d6bcbd5aee
caps.latest.revision: 23
manager: ghogen
robots: noindex,nofollow
translation.priority.ht: 
  - cs-cz
  - de-de
  - es-es
  - fr-fr
  - it-it
  - ja-jp
  - ko-kr
  - pl-pl
  - pt-br
  - ru-ru
  - tr-tr
  - zh-cn
  - zh-tw
---
# How to: Create and Execute an SQL Statement that Returns No Value
To execute an SQL statement that returns no value, you can run a TableAdapter query that is configured to run an SQL statement (for example, `CustomersTableAdapter.UpdateTableData(CustomersDataTable)`).  
  
 If your application does not use TableAdapters, call the `ExecuteNonQuery` method on a command object, setting its `CommandType` property to <xref:System.Data.CommandType?qualifyHint=False>. ("Command object" refers to the specific command for the [.NET Framework Data Provider](../Topic/.NET%20Framework%20Data%20Providers.md) your application is using. For example, if your application is using the .NET Framework Data Provider for SQL Server, the command object would be <xref:System.Data.SqlClient.SqlCommand?qualifyHint=False>.)  
  
 The following examples show how to execute SQL statements that return no value from a database using either TableAdapters or command objects. For more information on querying with TableAdapters and commands, see [Fill datasets by using TableAdapters](../VS_raddata/Fill-datasets-by-using-TableAdapters.md).  
  
## Executing SQL Statements that Return No Values Using a TableAdapter  
 This example shows how to create a TableAdapter query using the [Editing TableAdapters](../VS_raddata/Editing-TableAdapters.md), and then it provides information on how to declare an instance of the TableAdapter and execute the query.  
  
 > [!NOTE]
>  Your computer might show different names or locations for some of the Visual Studio user interface elements in the following instructions. The Visual Studio edition that you have and the settings that you use determine these elements. For more information, see [Personalizing the  IDE](../VS_IDE/Personalizing-the-Visual-Studio-IDE.md).  
  
#### To create an SQL statement that returns no value using a TableAdapter  
  
1.  Open a dataset in the **Dataset Designer**. For more information, see [How to: Open a Dataset in the Dataset Designer](../Topic/How%20to:%20Open%20a%20Dataset%20in%20the%20Dataset%20Designer.md).  
  
2.  If you do not already have one, create a TableAdapter. For more information on creating TableAdapters, see [Create and configure TableAdapters](../VS_raddata/Create-and-configure-TableAdapters.md).  
  
3.  If you already have a query on your TableAdapter that uses an SQL statement that returns no value, then skip to the next procedure, "To declare an instance of the TableAdapter and execute the query." Otherwise, continue with step 4 to create a new query that returns no value.  
  
4.  Right-click the TableAdapter that you want, and use the shortcut menu to add a query.  
  
     The **TableAdapter Query Configuration Wizard** opens.  
  
5.  Leave the default value of **Use SQL statements**, and then click **Next**.  
  
6.  Choose the **UPDATE**, **INSERT** or **DELETE** option, and then click **Next**.  
  
7.  Type your SQL statement, or use the **Query Builder** to assist with creating one, and then click **Next**.  
  
8.  Provide a name for the query.  
  
9. Complete the wizard; the query is added to the TableAdapter.  
  
10. Build your project.  
  
#### To declare an instance of the TableAdapter and execute the query  
  
1.  Declare an instance of the TableAdapter that contains the query you want to execute.  
  
    -   To create an instance using design-time tools, drag the TableAdapter that you want from the **Toolbox**. (Components in your project now appear in the **Toolbox** under a heading that matches your project name.) If the TableAdapter does not appear in the **Toolbox**, then you may need to build your project.  
  
         -or-  
  
    -   To create an instance in code, replace the following code with the names of your <xref:System.Data.DataSet?qualifyHint=False> and TableAdapter.  
  
         `Dim tableAdapter As New DataSetTableAdapters.TableAdapter`  
  
        > [!NOTE]
        >  TableAdapters are not actually located inside their associated dataset classes. Each dataset has a corresponding collection of TableAdapters in its own namespace. For example, if you have a dataset named `SalesDataSet`, there would be a `SalesDataSetTableAdapters` namespace that contains its TableAdapters.  
  
2.  Call your query as you would call any other method in code. Your query is a method on the TableAdapter. Replace the following code with the names of your TableAdapter and query. You also need to pass in any parameters required by your query. If you are not sure if your query requires parameters, or what parameters it requires, then check IntelliSense for the required signature of the query. Depending on whether your query takes parameters or not, the code would look similar to one of the following examples:  
  
     `TableAdapter.Query()`  
  
     `TableAdapter.Query(Parameters)`  
  
     Queries that we think of as returning no value actually do return a value — an integer containing the number of rows affected by the query. The complete code to declare an instance of a TableAdapter and execute a query should look similar to the following:  
  
     [!CODE [VbRaddataFillingAndExecuting#11](../CodeSnippet/VS_Snippets_VBCSharp/VbRaddataFillingAndExecuting#11)]  
  
## Executing SQL Statements that Return No Value Using a Command Object  
 The following example shows how to create a command and execute an SQL statement that returns no value. For information on setting and getting parameter values for a command, see [How to: Set and Get Parameters for Command Objects](../Topic/How%20to:%20Set%20and%20Get%20Parameters%20for%20Command%20Objects.md).  
  
 This example uses the <xref:System.Data.SqlClient.SqlCommand?qualifyHint=False> object and requires:  
  
-   References to the <xref:System?qualifyHint=False>, <xref:System.Data?qualifyHint=False>, and <xref:System.Xml?qualifyHint=False> namespaces.  
  
-   A data connection named `SqlConnection1`.  
  
-   A table named `Customers` in the data source that `SqlConnection1` connects to. (Otherwise, you need a valid SQL statement for your data source).  
  
#### To execute an SQL statement that returns no value using a DataCommand  
  
-   Add the following code to a method that you want to execute the SQL statement from. Call the `ExecuteNonQuery` method of a command to return no value (for example, <xref:System.Data.SqlClient.SqlCommand.ExecuteNonQuery?qualifyHint=True>).  
  
     [!CODE [VbRaddataFillingAndExecuting#12](../CodeSnippet/VS_Snippets_VBCSharp/VbRaddataFillingAndExecuting#12)]  
  
## .NET Framework Security  
 The application requires permission to access the database and execute the SQL statement.  
  
## See Also  
 <xref:System.Data.SqlClient.SqlCommand.ExecuteNonQuery?qualifyHint=True>   
 <xref:System.Data.OleDb.OleDbCommand.ExecuteNonQuery?qualifyHint=True>   
 <xref:System.Data.Odbc.OdbcCommand.ExecuteNonQuery?qualifyHint=True>   
 <xref:System.Data.OracleClient.OracleCommand.ExecuteNonQuery?qualifyHint=True>   
 [How to: Create TableAdapter Queries](../VS_raddata/How-to--Create-TableAdapter-Queries.md)   
 [How to: Edit TableAdapter Queries](../VS_raddata/How-to--Edit-TableAdapter-Queries.md)   
 [How to: Fill a dataset with data](../VS_raddata/How-to--Fill-a-dataset-with-data.md)   
 [Fill datasets by using TableAdapters](../VS_raddata/Fill-datasets-by-using-TableAdapters.md)   
 [How to: Set and Get Parameters for Command Objects](../Topic/How%20to:%20Set%20and%20Get%20Parameters%20for%20Command%20Objects.md)