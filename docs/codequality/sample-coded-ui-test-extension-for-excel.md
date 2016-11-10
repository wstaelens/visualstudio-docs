---
title: "Sample Coded UI Test Extension for Excel"
ms.custom: na
ms.date: "10/14/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: na
ms.suite: na
ms.technology: 
  - "vs-devops-test"
ms.tgt_pltfrm: na
ms.topic: "article"
helpviewer_keywords: 
  - "coded UI tests, extensions for Excel"
ms.assetid: 451e4d14-7fac-42f9-af56-2bdc8414c6c7
caps.latest.revision: 13
ms.author: "mlearned"
manager: "douge"
translation.priority.ht: 
  - "de-de"
  - "es-es"
  - "fr-fr"
  - "it-it"
  - "ja-jp"
  - "ko-kr"
  - "ru-ru"
  - "zh-cn"
  - "zh-tw"
translation.priority.mt: 
  - "cs-cz"
  - "pl-pl"
  - "pt-br"
  - "tr-tr"
---
# Sample Coded UI Test Extension for Excel
The extension component of the sample runs in the [!INCLUDE[vsprvs](../codequality/includes/vsprvs_md.md)] Coded UI Test process and is somewhat hierarchical with the `ExtensionPackage` class at the base. The `TechnologyManager`, `ActionFilter`, and `PropertyProvider` classes are at the next level, with the control elements at the top level.  
  
 ![Excel Test Extension Architecture](../codequality/media/excel_extarch.png "Excel_ExtArch")  
Excel Extension Architecture  
  
## Extension Points  
 These classes represent the extension points that are implemented in the sample to enable coded UI testing for [!INCLUDE[ofprexcel](../codequality/includes/ofprexcel_md.md)].  
  
### ExtensionPackage  
 Inherited from the \<xref:Microsoft.VisualStudio.TestTools.UITest.Extension.UITestExtensionPackage> class, this is the entry point for the coded UI testing extension. Implementing this abstract class gives the coded UI testing framework internal access to your custom UI test technology manager, UI test property provider, and UI test action filter for testing the new UI. For more information, see [ExtensionPackage Class](../codequality/sample-excel-extension--extensionpackage-class.md).  
  
### TechnologyManager  
 Inherited from the \<xref:Microsoft.VisualStudio.TestTools.UITest.Extension.UITechnologyManager> class, this class provides a technology manager for test recording and playback. For more information, see [TechnologyManager Class](../codequality/sample-excel-extension--technologymanager-class.md).  
  
### ActionFilter  
 Inherited from the \<xref:Microsoft.VisualStudio.TestTools.UITest.Common.UITestActionFilter> class, this class provides a base class for aggregating similar test action results into a single test result. For more information, see [ActionFilter Class](../codequality/sample-excel-extension--actionfilter-class.md).  
  
### Technology Elements  
 A base class inherited from the \<xref:Microsoft.VisualStudio.TestTools.UITest.Extension.UITechnologyElement> class provides the foundation for the technology elements in your UI tests that can be recorded and played back. For more information, see [Element Classes](../codequality/sample-excel-extension--element-classes.md).  
  
### PropertyProvider  
 Inherited from the \<xref:Microsoft.VisualStudio.TestTools.UITesting.UITestPropertyProvider> class, this class provides a base class for supporting the properties of UI elements for test recording and playback. For more information, see [PropertyProvider Class](../codequality/sample-excel-extension--propertyprovider-class.md).  
  
## See Also  
 \<xref:Microsoft.VisualStudio.TestTools.UITesting.UITestPropertyProvider>   
 \<xref:Microsoft.VisualStudio.TestTools.UITest.Extension.UITechnologyElement>   
 \<xref:Microsoft.VisualStudio.TestTools.UITest.Common.UITestActionFilter>   
 \<xref:Microsoft.VisualStudio.TestTools.UITest.Extension.UITestExtensionPackage>   
 [ExtensionPackage Class](../codequality/sample-excel-extension--extensionpackage-class.md)   
 [TechnologyManager Class](../codequality/sample-excel-extension--technologymanager-class.md)   
 [ActionFilter Class](../codequality/sample-excel-extension--actionfilter-class.md)   
 [Element Classes](../codequality/sample-excel-extension--element-classes.md)   
 [PropertyProvider Class](../codequality/sample-excel-extension--propertyprovider-class.md)