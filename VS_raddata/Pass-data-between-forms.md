---
title: "Pass data between forms"
ms.custom: na
ms.date: 10/07/2016
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
ms.assetid: 78bf038b-9296-4fbf-b0e8-d881d1aff0df
caps.latest.revision: 14
manager: ghogen
translation.priority.ht: 
  - de-de
  - es-es
  - fr-fr
  - it-it
  - ja-jp
  - ko-kr
  - ru-ru
  - zh-cn
  - zh-tw
translation.priority.mt: 
  - cs-cz
  - pl-pl
  - pt-br
  - tr-tr
---
# Pass data between forms
This walkthrough provides step-by-step instructions for passing data from one form to another. Using the customers and orders tables from Northwind, one form allows users to select a customer, and a second form displays the selected customer's orders. This walkthrough shows how to create a method on the second form that receives data from the first form.  
  
> [!NOTE]
>  This walkthrough demonstrates only one way to pass data between forms. There are other options for passing data to a form, including creating a second constructor to receive data, or creating a public property that can be set with data from the first form.  
  
 Tasks illustrated in this walkthrough include:  
  
-   Creating a new **Windows Application** project.  
  
-   Creating and configuring a dataset with the [Data Source Configuration Wizard](../VS_raddata/media/Data-Source-Configuration-Wizard.png).  
  
-   Selecting the control to be created on the form when dragging items from the **Data Sources** window. For more information, see [Set the control to be created when dragging from the Data Sources window](../VS_raddata/Set-the-control-to-be-created-when-dragging-from-the-Data-Sources-window.md).  
  
-   Creating a data-bound control by dragging items from the **Data Sources** window onto a form.  
  
-   Creating a second form with a grid to display data.  
  
-   Creating a TableAdapter query to fetch orders for a specific customer.  
  
-   Passing data between forms.  
  
## Prerequisites  
 In order to complete this walkthrough, you need:  
  
-   Access to the Northwind sample database. For more information, see [How to: Install Sample Databases](../VS_raddata/How-to--Install-Sample-Databases.md).  
  
## Create the Windows Application  
  
#### To create the new Windows project  
  
1.  From the **File** menu, create a new project.  
  
2.  Name the project `PassingDataBetweenForms`.  
  
3.  Select **Windows Forms Application**, and click **OK**. For more information, see [Client Applications](../Topic/Developing%20Client%20Applications%20with%20the%20.NET%20Framework.md).  
  
     The **PassingDataBetweenForms** project is created, and added to **Solution Explorer**.  
  
## Create the data source  
  
#### To create the data source  
  
1.  On the **Data** menu, click **Show Data Sources**.  
  
2.  In the **Data Sources** window, select **Add New Data Source** to start the **Data Source Configuration** wizard.  
  
3.  Select **Database** on the **Choose a Data Source Type** page, and then click **Next**.  
  
4.  On the **Choose a database model** page, verify that **Dataset** is specified, and then click **Next**.  
  
5.  On the **Choose your Data Connection** page, do one of the following:  
  
    -   If a data connection to the Northwind sample database is available in the drop-down list, select it.  
  
    -   Select **New Connection** to launch the **Add/Modify Connection** dialog box.  
  
6.  If your database requires a password and if the option to include sensitive data is enabled, select the option and then click **Next**.  
  
7.  On the **Save connection string to the Application Configuration file** page, click **Next**.  
  
8.  On the **Choose your Database Objects** page, expand the **Tables** node.  
  
9. Select the **Customers** and **Orders** tables, and then click **Finish**.  
  
     The **NorthwindDataSet** is added to your project, and the **Customers** and **Orders** tables appear in the **Data Sources** window.  
  
## Create the first form (Form1)  
 You can create a data-bound grid (a <xref:System.Windows.Forms.DataGridView?qualifyHint=False> control), by dragging the **Customers** node from the **Data Sources** window onto the form.  
  
#### To create a data-bound grid on the form  
  
-   Drag the main **Customers** node from the **Data Sources** window onto **Form1**.  
  
     A <xref:System.Windows.Forms.DataGridView?qualifyHint=False> and a tool strip (<xref:System.Windows.Forms.BindingNavigator?qualifyHint=False>) for navigating records appear on **Form1**. A [NorthwindDataSet](../VS_raddata/Dataset-tools-in-Visual-Studio.md), [CustomersTableAdapter](../VS_raddata/TableAdapter-Overview.md), <xref:System.Windows.Forms.BindingSource?qualifyHint=False>, and <xref:System.Windows.Forms.BindingNavigator?qualifyHint=False> appear in the component tray.  
  
## Create the second form (Form2)  
  
#### To create a second form to pass the data to  
  
1.  From the **Project** menu, choose **Add Windows Form**.  
  
2.  Leave the default name of **Form2**, and click **Add**.  
  
3.  Drag the main **Orders** node from the **Data Sources** window onto **Form2**.  
  
     A <xref:System.Windows.Forms.DataGridView?qualifyHint=False> and a tool strip (<xref:System.Windows.Forms.BindingNavigator?qualifyHint=False>) for navigating records appear on **Form2**. A [NorthwindDataSet](../VS_raddata/Dataset-tools-in-Visual-Studio.md), [CustomersTableAdapter](../VS_raddata/TableAdapter-Overview.md), <xref:System.Windows.Forms.BindingSource?qualifyHint=False>, and <xref:System.Windows.Forms.BindingNavigator?qualifyHint=False> appear in the component tray.  
  
4.  Delete the **OrdersBindingNavigator** from the component tray.  
  
     The **OrdersBindingNavigator** disappears from **Form2**.  
  
## Add a TableAdapter query to Form2 to load orders for the selected customer on Form1  
  
#### To create a TableAdapter query  
  
1.  Double-click the **NorthwindDataSet.xsd** file in **Solution Explorer**.  
  
2.  Right-click the **OrdersTableAdapter**, and select **Add Query**.  
  
3.  Leave the default option of **Use SQL statements**, and then click **Next**.  
  
4.  Leave the default option of **SELECT which returns rows**, and then click **Next**.  
  
5.  Add a WHERE clause to the query, to return `Orders` based on the `CustomerID`. The query should be similar to the following:  
  
    ```  
    SELECT OrderID, CustomerID, EmployeeID, OrderDate, RequiredDate, ShippedDate, ShipVia, Freight, ShipName, ShipAddress, ShipCity, ShipRegion, ShipPostalCode, ShipCountry  
    FROM Orders   
    WHERE CustomerID = @CustomerID  
    ```  
  
    > [!NOTE]
    >  Verify the correct parameter syntax for your database. For example, in Microsoft Access, the WHERE clause would look like: `WHERE CustomerID = ?`.  
  
6.  Click **Next**.  
  
7.  For the **Fill a DataTableMethod Name**, type `FillByCustomerID`.  
  
8.  Clear the **Return a DataTable** option, and then click **Next**.  
  
9. Click **Finish**.  
  
## Create a method on Form2 to pass data to  
  
#### To create a method to pass data to  
  
1.  Right-click **Form2**, and select **View Code** to open **Form2** in the **Code Editor**.  
  
2.  Add the following code to **Form2** after the `Form2_Load` method:  
  
     [!CODE [VbRaddataDisplaying#1](../CodeSnippet/VS_Snippets_VBCSharp/VbRaddataDisplaying#1)]  
  
## Create a method on Form1 to pass data and display Form2  
  
#### To create a method to pass data to Form2  
  
1.  In **Form1**, right-click the Customer data grid, and then click **Properties**.  
  
2.  In the **Properties** window, click **Events**.  
  
3.  Double-click the **CellDoubleClick** event.  
  
     The code editor appears.  
  
4.  Update the method definition to match the following sample:  
  
     [!CODE [VbRaddataDisplaying#2](../CodeSnippet/VS_Snippets_VBCSharp/VbRaddataDisplaying#2)]  
  
## Run the Application  
  
#### To run the application  
  
-   Press F5 to run the application.  
  
-   Double-click a customer record in **Form1** to open **Form2** with that customer's orders.  
  
## Next Steps  
 Depending on your application requirements, there are several steps you may want to perform after passing data between forms. Some enhancements you could make to this walkthrough include:  
  
-   Editing the dataset, to add or remove database objects. For more information, see [Create and configure datasets](../VS_raddata/Create-and-configure-datasets-in-Visual-Studio.md).  
  
-   Adding functionality to save data back to the database. For more information, see [Save data back to the database](../VS_raddata/Save-data-back-to-the-database.md).  
  
## See Also  
 [Bind Windows Forms controls to data in Visual Studio](../VS_raddata/Bind-Windows-Forms-controls-to-data-in-Visual-Studio.md)