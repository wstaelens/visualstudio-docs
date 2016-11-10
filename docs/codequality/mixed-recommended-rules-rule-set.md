---
title: "Mixed Recommended Rules rule set"
ms.custom: na
ms.date: "10/14/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: na
ms.suite: na
ms.technology: 
  - "vs-devops-test"
ms.tgt_pltfrm: na
ms.topic: "article"
ms.assetid: c3186b5b-0149-4a75-826e-e3539e4e703f
caps.latest.revision: 3
ms.author: "susanno"
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
# Mixed Recommended Rules rule set
The Microsoft Mixed Recommended Rules focus on the most common and critical problems in your C++ projects that support the Common Language Runtime, including potential security holes, application crashes, and other important logic and design errors. You should include this rule set in any custom rule set you create for your C++ projects that support the Common Language Runtime. This ruleset is designed to be configured with the Visual Studio Professional edition and higher.  
  
|Rule|Description|  
|----------|-----------------|  
|[C6001](../codequality/c6001.md)|Using Uninitialized Memory|  
|[C6011](../codequality/c6011.md)|Dereferencing Null Pointer|  
|[C6029](../codequality/c6029.md)|Use Of Unchecked Value|  
|[C6031](../codequality/c6031.md)|Return Value Ignored|  
|[C6053](../codequality/c6053.md)|Zero Termination From Call|  
|[C6054](../codequality/c6054.md)|Zero Termination Missing|  
|[C6059](../codequality/c6059.md)|Bad Concatenation|  
|[C6063](../codequality/c6063.md)|Missing String Argument To Format Function|  
|[C6064](../codequality/c6064.md)|Missing Integer Argument To Format Function|  
|[C6066](../codequality/c6066.md)|Missing Pointer Argument To Format Function|  
|[C6067](../codequality/c6067.md)|Missing String Pointer Argument To Format Function|  
|[C6101](../codequality/c6101.md)|Returning uninitialized memory|  
|[C6200](../codequality/c6200.md)|Index Exceeds Buffer Maximum|  
|[C6201](../codequality/c6201.md)|Index Exceeds Stack Buffer Maximum|  
|[C6214](../codequality/c6214.md)|Invalid Cast HRESULT To BOOL|  
|[C6215](../codequality/c6215.md)|Invalid Cast BOOL To HRESULT|  
|[C6216](../codequality/c6216.md)|Invalid Compiler-Inserted Cast BOOL To HRESULT|  
|[C6217](../codequality/c6217.md)|Invalid HRESULT Test With NOT|  
|[C6220](../codequality/c6220.md)|Invalid HRESULT Compare To -1|  
|[C6226](../codequality/c6226.md)|Invalid HRESULT Assignment To -1|  
|[C6230](../codequality/c6230.md)|Invalid HRESULT Use As Boolean|  
|[C6235](../codequality/c6235.md)|Non-Zero Constant With Logical-Or|  
|[C6236](../codequality/c6236.md)|Logical-Or With Non-Zero Constant|  
|[C6237](../codequality/c6237.md)|Zero With Logical-And Loses Side Effects|  
|[C6242](../codequality/c6242.md)|Local Unwind Forced|  
|[C6248](../codequality/c6248.md)|Creating Null DACL|  
|[C6250](../codequality/c6250.md)|Unreleased Address Descriptors|  
|[C6255](../codequality/c6255.md)|Unprotected Use Of Alloca|  
|[C6258](../codequality/c6258.md)|Using Terminate Thread|  
|[C6259](../codequality/c6259.md)|Dead Code In Bitwise-Or Limited Switch|  
|[C6260](../codequality/c6260.md)|Use Of Byte Arithmetic|  
|[C6262](../codequality/c6262.md)|Excessive Stack Usage|  
|[C6263](../codequality/c6263.md)|Using Alloca In Loop|  
|[C6268](../codequality/c6268.md)|Missing Parentheses In Cast|  
|[C6269](../codequality/c6269.md)|Pointer Dereference Ignored|  
|[C6270](../codequality/c6270.md)|Missing Float Argument To Format Function|  
|[C6271](../codequality/c6271.md)|Extra Argument To Format Function|  
|[C6272](../codequality/c6272.md)|Non-Float Argument To Format Function|  
|[C6273](../codequality/c6273.md)|Non-Integer Argumen To Format Function|  
|[C6274](../codequality/c6274.md)|Non-Character Argument To Format Function|  
|[C6276](../codequality/c6276.md)|Invalid String Cast|  
|[C6277](../codequality/c6277.md)|Invalid CreateProcess Call|  
|[C6278](../codequality/c6278.md)|Array-New Scalar-Delete Mismatch|  
|[C6279](../codequality/c6279.md)|Scalar-New Array-Delete Mismatch|  
|[C6280](../codequality/c6280.md)|Memory Allocation-Deallocation Mismatch|  
|[C6281](../codequality/c6281.md)|Bitwise Relation Precedence|  
|[C6282](../codequality/c6282.md)|Assignment Replaces Test|  
|[C6283](../codequality/c6283.md)|Primitive Array-New Scalar-Delete Mismatch|  
|[C6284](../codequality/c6284.md)|Invalid Object Argument To Format Function|  
|[C6285](../codequality/c6285.md)|Logical-Or Of Constants|  
|[C6286](../codequality/c6286.md)|Non-Zero Logical-Or Losing Side Effects|  
|[C6287](../codequality/c6287.md)|Redundant Test|  
|[C6288](../codequality/c6288.md)|Mutual Inclusion Over Logical-And Is False|  
|[C6289](../codequality/c6289.md)|Mutual Exclusion Over Logical-Or Is True|  
|[C6290](../codequality/c6290.md)|Logical-Not Bitwise-And Precedence|  
|[C6291](../codequality/c6291.md)|Logical-Not Bitwise-Or Precedence|  
|[C6292](../codequality/c6292.md)|Loop Counts Up From Maximum|  
|[C6293](../codequality/c6293.md)|Loop Counts Down From Minimum|  
|[C6294](../codequality/c6294.md)|Loop Body Never Executed|  
|[C6295](../codequality/c6295.md)|Infinite Loop|  
|[C6296](../codequality/c6296.md)|Loop Only Executed Once|  
|[C6297](../codequality/c6297.md)|Result Of Shift Cast To Larger Size|  
|[C6299](../codequality/c6299.md)|Bitfield To Boolean Comparison|  
|[C6302](../codequality/c6302.md)|Invalid Character String Argument To Format Function|  
|[C6303](../codequality/c6303.md)|Invalid Wide Character String Argument To Format Function|  
|[C6305](../codequality/c6305.md)|Mismatched Size And Count Use|  
|[C6306](../codequality/c6306.md)|Incorrect Variable Argument Function Call|  
|[C6308](../codequality/c6308.md)|Realloc Leak|  
|[C6310](../codequality/c6310.md)|Illegal Exception Filter Constant|  
|[C6312](../codequality/c6312.md)|Exception Continue Execution Loop|  
|[C6314](../codequality/c6314.md)|Bitwise-Or Precedence|  
|[C6317](../codequality/c6317.md)|Not Not Complement|  
|[C6318](../codequality/c6318.md)|Exception Continue Search|  
|[C6319](../codequality/c6319.md)|Ignored By Comma|  
|[C6324](../codequality/c6324.md)|String Copy Instead Of String Compare|  
|[C6328](../codequality/c6328.md)|Potential Argument Type Mismatch|  
|[C6331](../codequality/c6331.md)|VirtualFree Invalid Flags|  
|[C6332](../codequality/c6332.md)|VirtualFree Invalid Parameter|  
|[C6333](../codequality/c6333.md)|VirtualFree Invalid Size|  
|[C6335](../codequality/c6335.md)|Leaking Process Handle|  
|[C6381](../codequality/c6381.md)|Shutdown Information Missing|  
|[C6383](../codequality/c6383.md)|Element-Count Byte-Count Buffer Overrun|  
|[C6384](../codequality/c6384.md)|Pointer Size Division|  
|[C6385](../codequality/c6385.md)|Read Overrun|  
|[C6386](../codequality/c6386.md)|Write Overrun|  
|[C6387](../codequality/c6387.md)|Invalid Parameter Value|  
|[C6388](../codequality/c6388.md)|Invalid Parameter Value|  
|[C6500](../codequality/c6500.md)|Invalid Attribute Property|  
|[C6501](../codequality/c6501.md)|Conflicting Attribute Property Values|  
|[C6503](../codequality/c6503.md)|References Cannot Be Null|  
|[C6504](../codequality/c6504.md)|Null On Non-Pointer|  
|[C6505](../codequality/c6505.md)|MustCheck On Void|  
|[C6506](../codequality/c6506.md)|Buffer Size On Non-Pointer Or Array|  
|[C6507](assetId:///18f88cd1-d035-4403-a6a4-12dd0affcf21)|Null Mismatch At Dereference Zero|  
|[C6508](../codequality/c6508.md)|Write Access On Constant|  
|[C6509](../codequality/c6509.md)|Return Used On Precondition|  
|[C6510](../codequality/c6510.md)|Null Terminated On Non-Pointer|  
|[C6511](../codequality/c6511.md)|MustCheck Must Be Yes Or No|  
|[C6513](../codequality/c6513.md)|Element Size Without Buffer Size|  
|[C6514](../codequality/c6514.md)|Buffer Size Exceeds Array Size|  
|[C6515](../codequality/c6515.md)|Buffer Size On Non-Pointer|  
|[C6516](../codequality/c6516.md)|No Properties On Attribute|  
|[C6517](../codequality/c6517.md)|Valid Size On Non-Readable Buffer|  
|[C6518](../codequality/c6518.md)|Writable Size On Non-Writable Buffer|  
|[C6519](assetId:///2b6326b0-0539-4d26-8fb1-720114933232)|Invalid annotation: value of the 'NeedsRelease' property must be Yes or No|  
|[C6521](assetId:///e98d0ae3-6f13-47b2-9a15-15d4055af9ef)|Invalid Size String Dereference|  
|[C6522](../codequality/c6522.md)|Invalid Size String Type|  
|[C6523](assetId:///11397a31-b224-46b0-afb7-d49ca576a3bb)|Invalid Size String Parameter|  
|[C6525](../codequality/c6525.md)|Invalid Size String Unreachable Location|  
|[C6526](assetId:///59c590c7-0098-4166-a1ac-87f324596002)|Invalid Size String Buffer Type|  
|[C6527](../codequality/c6527.md)|Invalid annotation: 'NeedsRelease' property may not be used on values of void type|  
|[C6530](../codequality/c6530.md)|Unrecognized Format String Style|  
|[C6540](../codequality/c6540.md)|The use of attribute annotations on this function will invalidate all of its existing __declspec annotations|  
|[C6551](../codequality/c6551.md)|Invalid size specification: expression not parsable|  
|[C6552](../codequality/c6552.md)|Invalid Deref= or Notref=: expression not parsable|  
|[C6701](../codequality/c6701.md)|The value is not a valid Yes/No/Maybe value|  
|[C6702](../codequality/c6702.md)|The value is not a string value|  
|[C6703](../codequality/c6703.md)|The value is not a number|  
|[C6704](../codequality/c6704.md)|Unexpected Annotation Expression Error|  
|[C6705](../codequality/c6705.md)|Expected number of arguments for annotation does not match actual number of arguments for annotation|  
|[C6706](../codequality/c6706.md)|Unexpected Annotation Error for annotation|  
|[C6995](../codequality/c6995.md)|Failed to save XML Log file|  
|[C26100](../codequality/c26100.md)|Race condition|  
|[C26101](../codequality/c26101.md)|Failing to use interlocked operation properly|  
|[C26110](../codequality/c26110.md)|Caller failing to hold lock|  
|[C26111](../codequality/c26111.md)|Caller failing to release lock|  
|[C26112](../codequality/c26112.md)|Caller cannot hold any lock|  
|[C26115](../codequality/c26115.md)|Failing to release lock|  
|[C26116](../codequality/c26116.md)|Failing to acquire or to hold lock|  
|[C26117](../codequality/c26117.md)|Releasing unheld lock|  
|[C26140](../codequality/c26140.md)|Concurrency SAL annotation error|  
|[C28020](../codequality/c28020.md)|The expression is not true at this call|  
|[C28021](../codequality/c28021.md)|The parameter being annotated must be a pointer|  
|[C28022](../codequality/c28022.md)|The function class(es) on this function do not match the function class(es) on the typedef used to define it.|  
|[C28023](../codequality/c28023.md)|The function being assigned or passed should have a _Function_class\_ annotation for at least one of the class(es)|  
|[C28024](../codequality/c28024.md)|The function pointer being assigned to is annotated with the function class, which is not contained in the function class(es) list.|  
|[C28039](../codequality/c28039.md)|The type of actual parameter should exactly match the type|  
|[C28112](../codequality/c28112.md)|A variable which is accessed via an Interlocked function must always be accessed via an Interlocked function.|  
|[C28113](../codequality/c28113.md)|Accessing a local variable via an Interlocked function|  
|[C28125](../codequality/c28125.md)|The function must be called from within a try/except block|  
|[C28137](../codequality/c28137.md)|The variable argument should instead be a (literal) constant|  
|[C28138](../codequality/c28138.md)|The constant argument should instead be variable|  
|[C28159](../codequality/c28159.md)|Consider using another function instead.|  
|[C28160](../codequality/c28160.md)|Error annotation|  
|[C28163](../codequality/c28163.md)|The function should never be called from within a try/except block|  
|[C28164](../codequality/c28164.md)|The argument is being passed to a function that expects a pointer to an object (not a pointer to a pointer)|  
|[C28182](../codequality/c28182.md)|Dereferencing NULL pointer. The pointer contains the same NULL value as another pointer did.|  
|[C28183](../codequality/c28183.md)|The argument could be one value, and is a copy of the value found in the pointer|  
|[C28193](../codequality/c28193.md)|The variable holds a value that must be examined|  
|[C28196](../codequality/c28196.md)|The requirement is not satisfied. (The expression does not evaluate to true.)|  
|[C28202](../codequality/c28202.md)|Illegal reference to non-static member|  
|[C28203](../codequality/c28203.md)|Ambiguous reference to class member.|  
|[C28205](../codequality/c28205.md)|_Success\_ or _On_failure\_ used in an illegal context|  
|[C28206](../codequality/c28206.md)|Left operand points to a struct, use '->'|  
|[C28207](../codequality/c28207.md)|Left operand is a struct, use '.'|  
|[C28209](../codequality/c28209.md)|The declaration for symbol has a conflicting declaration|  
|[C28210](../codequality/c28210.md)|Annotations for the __on_failure context must not be in explicit pre context|  
|[C28211](../codequality/c28211.md)|Static context name expected for SAL_context|  
|[C28212](../codequality/c28212.md)|Pointer expression expected for annotation|  
|[C28213](../codequality/c28213.md)|The _Use_decl_annotations\_ annotation must be used to reference, without modification, a prior declaration.|  
|[C28214](../codequality/c28214.md)|Attribute parameter names must be p1...p9|  
|[C28215](../codequality/c28215.md)|The typefix cannot be applied to a parameter that already has a typefix|  
|[C28216](../codequality/c28216.md)|The checkReturn annotation only applies to postconditions for the specific function parameter.|  
|[C28217](../codequality/c28217.md)|For function, the number of parameters to annotation does not match that found at file|  
|[C28218](../codequality/c28218.md)|For function paramteer, the annotation's parameter does not match that found at file|  
|[C28219](../codequality/c28219.md)|Member of enumeration expected for annotation the parameter in the annotation|  
|[C28220](../codequality/c28220.md)|Integer expression expected for annotation the parameter in the annotation|  
|[C28221](../codequality/c28221.md)|String expression expected for the parameter in the annotation|  
|[C28222](../codequality/c28222.md)|__yes, \__no, or \__maybe expected for annotation|  
|[C28223](../codequality/c28223.md)|Did not find expected Token/identifier for annotation, parameter|  
|[C28224](../codequality/c28224.md)|Annotation requires parameters|  
|[C28225](../codequality/c28225.md)|Did not find the correct number of required parameters in annotation|  
|[C28226](../codequality/c28226.md)|Annotation cannot also be a PrimOp (in current declaration)|  
|[C28227](../codequality/c28227.md)|Annotation cannot also be a PrimOp (see prior declaration)|  
|[C28228](../codequality/c28228.md)|Annotation parameter: cannot use type in annotations|  
|[C28229](../codequality/c28229.md)|Annotation does not support parameters|  
|[C28230](../codequality/c28230.md)|The type of parameter has no member.|  
|[C28231](../codequality/c28231.md)|Annotation is only valid on array|  
|[C28232](../codequality/c28232.md)|pre, post, or deref not applied to any annotation|  
|[C28233](../codequality/c28233.md)|pre, post, or deref applied to a block|  
|[C28234](../codequality/c28234.md)|__at expression does not apply to current function|  
|[C28235](../codequality/c28235.md)|The function cannot stand alone as an annotation|  
|[C28236](../codequality/c28236.md)|The annotation cannot be used in an expression|  
|[C28237](../codequality/c28237.md)|The annotation on parameter is no longer supported|  
|[C28238](../codequality/c28238.md)|The annotation on parameter has more than one of value, stringValue, and longValue. Use paramn=xxx|  
|[C28239](../codequality/c28239.md)|The annotation on parameter has both value, stringValue, or longValue; and paramn=xxx. Use only paramn=xxx|  
|[C28240](../codequality/c28240.md)|The annotation on parameter has param2 but no param1|  
|[C28241](../codequality/c28241.md)|The annotation for function on parameter is not recognized|  
|[C28243](../codequality/c28243.md)|The annotation for function on parameter requires more dereferences than the actual type annotated allows|  
|[C28244](../codequality/c28244.md)|The annotation for function has an unparseable parameter/external annotation|  
|[C28245](../codequality/c28245.md)|The annotation for function annotates 'this' on a non-member-function|  
|[C28246](../codequality/c28246.md)|The parameter annotation for function does not match the type of the parameter|  
|[C28250](../codequality/c28250.md)|Inconsistent annotation for function: the prior instance has an error.|  
|[C28251](../codequality/c28251.md)|Inconsistent annotation for function: this instance has an error.|  
|[C28252](../codequality/c28252.md)|Inconsistent annotation for function: parameter has another annotations on this instance.|  
|[C28253](../codequality/c28253.md)|Inconsistent annotation for function: parameter has another annotations on this instance.|  
|[C28254](../codequality/c28254.md)|dynamic_cast<>() is not supported in annotations|  
|[C28262](../codequality/c28262.md)|A syntax error in the annotation was found in function, for annotation|  
|[C28263](../codequality/c28263.md)|A syntax error in a conditional annotation was found for Intrinsic annotation|  
|[C28264](assetId:///bf6ea983-a06e-4752-a042-747a7dbf338c)|Result lists values must be constants.|  
|[C28267](../codequality/c28267.md)|A syntax error in the annotations was found annotation in the function.|  
|[C28272](../codequality/c28272.md)|The annotation for function, parameter when examining is inconsistent with the function declaration|  
|[C28273](../codequality/c28273.md)|For function, the clues are inconsistent with the function declaration|  
|[C28275](../codequality/c28275.md)|The parameter to _Macro_value\_ is null|  
|[C28279](../codequality/c28279.md)|For symbol, a 'begin' was found without a matching 'end'|  
|[C28280](../codequality/c28280.md)|For symbol, an 'end' was found without a matching 'begin'|  
|[C28282](../codequality/c28282.md)|Format Strings must be in preconditions|  
|[C28285](../codequality/c28285.md)|For function, syntax error in parameter|  
|[C28286](../codequality/c28286.md)|For function, syntax error near the end|  
|[C28287](../codequality/c28287.md)|For function, syntax Error in _At\_() annotation (unrecognized parameter name)|  
|[C28288](../codequality/c28288.md)|For function, syntax Error in _At\_() annotation (invalid parameter name)|  
|[C28289](../codequality/c28289.md)|For function: ReadableTo or WritableTo did not have a limit-spec as a parameter|  
|[C28290](../codequality/c28290.md)|the annotation for function contains more Externals than the actual number of parameters|  
|[C28291](../codequality/c28291.md)|post null/notnull at deref level 0 is meaningless for function.|  
|[C28300](../codequality/c28300.md)|Expression operands of incompatible types for operator|  
|[C28301](../codequality/c28301.md)|No annotations for first declaration of function.|  
|[C28302](../codequality/c28302.md)|An extra _Deref\_ operator was found on annotation.|  
|[C28303](../codequality/c28303.md)|An ambiguous _Deref\_ operator was found on annotation.|  
|[C28304](../codequality/c28304.md)|An improperly placed _Notref\_ operator was found applied to token.|  
|[C28305](../codequality/c28305.md)|An error while parsing a token was discovered.|  
|[C28306](../codequality/c28306.md)|The annotation on parameter is obsolescent|  
|[C28307](../codequality/c28307.md)|The annotation on parameter is obsolescent|  
|[C28350](../codequality/c28350.md)|The annotation describes a situation that is not conditionally applicable.|  
|[C28351](../codequality/c28351.md)|The annotation describes where a dynamic value (a variable) cannot be used in the condition.|  
|[CA1001](../codequality/ca1001--types-that-own-disposable-fields-should-be-disposable.md)|Types that own disposable fields should be disposable|  
|[CA1009](../codequality/ca1009--declare-event-handlers-correctly.md)|Declare event handlers correctly|  
|[CA1016](../codequality/ca1016--mark-assemblies-with-assemblyversionattribute.md)|Mark assemblies with AssemblyVersionAttribute|  
|[CA1033](../codequality/ca1033--interface-methods-should-be-callable-by-child-types.md)|Interface methods should be callable by child types|  
|[CA1049](../codequality/ca1049--types-that-own-native-resources-should-be-disposable.md)|Types that own native resources should be disposable|  
|[CA1060](../codequality/ca1060--move-p-invokes-to-nativemethods-class.md)|Move P/Invokes to NativeMethods class|  
|[CA1061](../codequality/ca1061--do-not-hide-base-class-methods.md)|Do not hide base class methods|  
|[CA1063](../codequality/ca1063--implement-idisposable-correctly.md)|Implement IDisposable correctly|  
|[CA1065](../codequality/ca1065--do-not-raise-exceptions-in-unexpected-locations.md)|Do not raise exceptions in unexpected locations|  
|[CA1301](../codequality/ca1301--avoid-duplicate-accelerators.md)|Avoid duplicate accelerators|  
|[CA1400](../codequality/ca1400--p-invoke-entry-points-should-exist.md)|P/Invoke entry points should exist|  
|[CA1401](../codequality/ca1401--p-invokes-should-not-be-visible.md)|P/Invokes should not be visible|  
|[CA1403](../codequality/ca1403--auto-layout-types-should-not-be-com-visible.md)|Auto layout types should not be COM visible|  
|[CA1404](../codequality/ca1404--call-getlasterror-immediately-after-p-invoke.md)|Call GetLastError immediately after P/Invoke|  
|[CA1405](../codequality/ca1405--com-visible-type-base-types-should-be-com-visible.md)|COM visible type base types should be COM visible|  
|[CA1410](../codequality/ca1410--com-registration-methods-should-be-matched.md)|COM registration methods should be matched|  
|[CA1415](../codequality/ca1415--declare-p-invokes-correctly.md)|Declare P/Invokes correctly|  
|[CA1821](../codequality/ca1821--remove-empty-finalizers.md)|Remove empty finalizers|  
|[CA1900](../codequality/ca1900--value-type-fields-should-be-portable.md)|Value type fields should be portable|  
|[CA1901](../codequality/ca1901--p-invoke-declarations-should-be-portable.md)|P/Invoke declarations should be portable|  
|[CA2002](../codequality/ca2002--do-not-lock-on-objects-with-weak-identity.md)|Do not lock on objects with weak identity|  
|[CA2100](../codequality/ca2100--review-sql-queries-for-security-vulnerabilities.md)|Review SQL queries for security vulnerabilities|  
|[CA2101](../codequality/ca2101--specify-marshaling-for-p-invoke-string-arguments.md)|Specify marshaling for P/Invoke string arguments|  
|[CA2108](../codequality/ca2108--review-declarative-security-on-value-types.md)|Review declarative security on value types|  
|[CA2111](../codequality/ca2111--pointers-should-not-be-visible.md)|Pointers should not be visible|  
|[CA2112](../codequality/ca2112--secured-types-should-not-expose-fields.md)|Secured types should not expose fields|  
|[CA2114](../codequality/ca2114--method-security-should-be-a-superset-of-type.md)|Method security should be a superset of type|  
|[CA2116](../codequality/ca2116--aptca-methods-should-only-call-aptca-methods.md)|APTCA methods should only call APTCA methods|  
|[CA2117](../codequality/ca2117--aptca-types-should-only-extend-aptca-base-types.md)|APTCA types should only extend APTCA base types|  
|[CA2122](../codequality/ca2122--do-not-indirectly-expose-methods-with-link-demands.md)|Do not indirectly expose methods with link demands|  
|[CA2123](../codequality/ca2123--override-link-demands-should-be-identical-to-base.md)|Override link demands should be identical to base|  
|[CA2124](../codequality/ca2124--wrap-vulnerable-finally-clauses-in-outer-try.md)|Wrap vulnerable finally clauses in outer try|  
|[CA2126](../codequality/ca2126--type-link-demands-require-inheritance-demands.md)|Type link demands require inheritance demands|  
|[CA2131](../codequality/ca2131--security-critical-types-may-not-participate-in-type-equivalence.md)|Security critical types may not participate in type equivalence|  
|[CA2132](../codequality/ca2132--default-constructors-must-be-at-least-as-critical-as-base-type-default-constructors.md)|Default constructors must be at least as critical as base type default constructors|  
|[CA2133](../codequality/ca2133--delegates-must-bind-to-methods-with-consistent-transparency.md)|Delegates must bind to methods with consistent transparency|  
|[CA2134](../codequality/ca2134--methods-must-keep-consistent-transparency-when-overriding-base-methods.md)|Methods must keep consistent transparency when overriding base methods|  
|[CA2137](../codequality/ca2137--transparent-methods-must-contain-only-verifiable-il.md)|Transparent methods must contain only verifiable IL|  
|[CA2138](../codequality/ca2138--transparent-methods-must-not-call-methods-with-the-suppressunmanagedcodesecurity-attribute.md)|Transparent methods must not call methods with the SuppressUnmanagedCodeSecurity attribute|  
|[CA2140](../codequality/ca2140--transparent-code-must-not-reference-security-critical-items.md)|Transparent code must not reference security critical items|  
|[CA2141](../codequality/ca2141-transparent-methods-must-not-satisfy-linkdemands.md)|Transparent methods must not satisfy LinkDemands|  
|[CA2146](../codequality/ca2146--types-must-be-at-least-as-critical-as-their-base-types-and-interfaces.md)|Types must be at least as critical as their base types and interfaces|  
|[CA2147](../codequality/ca2147--transparent-methods-may-not-use-security-asserts.md)|Transparent methods may not use security asserts|  
|[CA2149](../codequality/ca2149--transparent-methods-must-not-call-into-native-code.md)|Transparent methods must not call into native code|  
|[CA2200](../codequality/ca2200--rethrow-to-preserve-stack-details.md)|Rethrow to preserve stack details|  
|[CA2202](../codequality/ca2202--do-not-dispose-objects-multiple-times.md)|Do not dispose objects multiple times|  
|[CA2207](../codequality/ca2207--initialize-value-type-static-fields-inline.md)|Initialize value type static fields inline|  
|[CA2212](../codequality/ca2212--do-not-mark-serviced-components-with-webmethod.md)|Do not mark serviced components with WebMethod|  
|[CA2213](../codequality/ca2213--disposable-fields-should-be-disposed.md)|Disposable fields should be disposed|  
|[CA2214](../codequality/ca2214--do-not-call-overridable-methods-in-constructors.md)|Do not call overridable methods in constructors|  
|[CA2216](../codequality/ca2216--disposable-types-should-declare-finalizer.md)|Disposable types should declare finalizer|  
|[CA2220](../codequality/ca2220--finalizers-should-call-base-class-finalizer.md)|Finalizers should call base class finalizer|  
|[CA2229](../codequality/ca2229--implement-serialization-constructors.md)|Implement serialization constructors|  
|[CA2231](../codequality/ca2231--overload-operator-equals-on-overriding-valuetype.equals.md)|Overload operator equals on overriding ValueType.Equals|  
|[CA2232](../codequality/ca2232--mark-windows-forms-entry-points-with-stathread.md)|Mark Windows Forms entry points with STAThread|  
|[CA2235](../codequality/ca2235--mark-all-non-serializable-fields.md)|Mark all non-serializable fields|  
|[CA2236](../codequality/ca2236--call-base-class-methods-on-iserializable-types.md)|Call base class methods on ISerializable types|  
|[CA2237](../codequality/ca2237--mark-iserializable-types-with-serializableattribute.md)|Mark ISerializable types with SerializableAttribute|  
|[CA2238](../codequality/ca2238--implement-serialization-methods-correctly.md)|Implement serialization methods correctly|  
|[CA2240](../codequality/ca2240--implement-iserializable-correctly.md)|Implement ISerializable correctly|  
|[CA2241](../codequality/ca2241--provide-correct-arguments-to-formatting-methods.md)|Provide correct arguments to formatting methods|  
|[CA2242](../codequality/ca2242--test-for-nan-correctly.md)|Test for NaN correctly|