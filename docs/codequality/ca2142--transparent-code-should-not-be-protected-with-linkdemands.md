---
title: "CA2142: Transparent code should not be protected with LinkDemands"
ms.custom: na
ms.date: "10/14/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: na
ms.suite: na
ms.technology: 
  - "vs-devops-test"
ms.tgt_pltfrm: na
ms.topic: "article"
f1_keywords: 
  - "CA2142"
ms.assetid: 6dc59053-5dd9-4583-bf10-5f339107e59f
caps.latest.revision: 10
ms.author: "douge"
manager: "douge"
translation.priority.ht: 
  - "cs-cz"
  - "de-de"
  - "es-es"
  - "fr-fr"
  - "it-it"
  - "ja-jp"
  - "ko-kr"
  - "pl-pl"
  - "pt-br"
  - "ru-ru"
  - "tr-tr"
  - "zh-cn"
  - "zh-tw"
---
# CA2142: Transparent code should not be protected with LinkDemands
|||  
|-|-|  
|TypeName|TransparentMethodsShouldNotBeProtectedWithLinkDemands|  
|CheckId|CA2142|  
|Category|Microsoft.Security|  
|Breaking Change|Breaking|  
  
## Cause  
 A transparent method requires a \<xref:System.Security.Permissions.SecurityAction> or other security demand.  
  
## Rule Description  
 This rule fires on transparent methods which require LinkDemands to access them. Security transparent code should not be responsible for verifying the security of an operation, and therefore should not demand permissions. Because transparent methods are supposed to be security neutral, they should not be making any security decisions. Additionally, safe critical code, which does make security decisions, should not be relying on transparent code to have previously made such a decision.  
  
## How to Fix Violations  
 To fix a violation of this rule, remove the link demand on the transparent method or mark the method with \<xref:System.Security.SecuritySafeCriticalAttribute> attribute if it is performing security checks, such as security demands.  
  
## When to Suppress Warnings  
 Do not suppress a warning from this rule.  
  
## Example  
 In the following example, the rule fires on the method because the method is transparent and is marked with a LinkDemand \<xref:System.Security.PermissionSet> that contains an \<xref:System.Security.Permissions.SecurityAction>.  
  
 [!code[FxCop.Security.CA2142.TransparentMethodsShouldNotBeProtectedWithLinkDemands#1](../codequality/codesnippet/CSharp/ca2142--transparent-code-should-not-be-protected-with-linkdemands_1.cs)]  
  
 Do not suppress a warning from this rule.