---
title: "XML descendant elements cannot be selected from type &#39;type&#39;"
ms.custom: na
ms.date: 10/01/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 560a3370-f24d-4ca3-93b1-39aabe13c238
caps.latest.revision: 7
manager: douge
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
# XML descendant elements cannot be selected from type &#39;type&#39;
An XML descendant has been referenced for an object that is not of type <xref:System.Xml.Linq.XElement?qualifyHint=False>, <xref:System.Xml.Linq.XDocument?qualifyHint=False>, or `IEnumerable(Of XElement)`. For more information, see [XML Descendant Axis Property](../Topic/XML%20Descendant%20Axis%20Property%20\(Visual%20Basic\).md).  
  
```vb#  
' Generates an error.  
Dim var = "sample text"...<childElement>  
```  
  
 **Error ID:** BC36809  
  
### To correct this error  
  
-   Ensure that the object of which you are referencing a descendant element is strongly typed as <xref:System.Xml.Linq.XElement?qualifyHint=False>, <xref:System.Xml.Linq.XDocument?qualifyHint=False>, or `IEnumerable(Of XElement)`. Following is an example:  
  
    ```vb#  
    Dim elem As XElement = <root>  
                            <child />  
                           </root>  
    Dim var = elem...<child>  
    ```  
  
## See Also  
 [XML Descendant Axis Property](../Topic/XML%20Descendant%20Axis%20Property%20\(Visual%20Basic\).md)   
 [XML Axis Properties](../Topic/XML%20Axis%20Properties%20\(Visual%20Basic\).md)   
 [XML](../Topic/XML%20in%20Visual%20Basic.md)