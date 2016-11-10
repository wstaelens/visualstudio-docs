---
title: "&#39;Using&#39; must end with a matching &#39;End Using&#39;"
ms.custom: na
ms.date: 10/01/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 83269108-b169-40a6-bbcc-af1ac8fcfd67
caps.latest.revision: 8
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
# &#39;Using&#39; must end with a matching &#39;End Using&#39;
A `Using` statement occurs without a corresponding `End Using` statement.  
  
 An `End Using` statement must be used to end the `Using` block.  
  
 **Error ID:** BC36008  
  
### To correct this error  
  
1.  If this `Using` block is part of a set of nested `Using` blocks, make sure each block is properly terminated.  
  
2.  Add an `End Using` statement to the end of the `Using` block.  
  
## See Also  
 [Using Statement](../Topic/Using%20Statement%20\(Visual%20Basic\).md)   
 [How to: Dispose of a System Resource](../Topic/How%20to:%20Dispose%20of%20a%20System%20Resource%20\(Visual%20Basic\).md)