---
title: "HStringReference Class"
ms.custom: na
ms.date: 10/07/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: reference
ms.assetid: 9bf823b1-17eb-4ac4-8c5d-27d27c7a4150
caps.latest.revision: 3
manager: ghogen
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
# HStringReference Class
Represents an HSTRING that is created from an existing string.  
  
## Syntax  
  
```cpp  
class HStringReference;  
```  
  
## Remarks  
 The lifetime of the backing buffer in the new HSTRING is not managed by the Windows Runtime. The caller allocates a source string on the stack frame to avoid a heap allocation and to eliminate the risk of a memory leak. Also, the caller must ensure that source string remains unchanged during the lifetime of the attached HSTRING. For more information, see [WindowsCreateStringReference function](assetId:///0361bb7e-da49-4289-a93e-de7aab8712ac).  
  
## Members  
  
### Public Constructors  
  
|Name|Description|  
|----------|-----------------|  
|[HStringReference::HStringReference Constructor](../VS_visualcpp/HStringReference--HStringReference-Constructor.md)|Initializes a new instance of the HStringReference class.|  
  
### Members  
  
|Member|Description|  
|------------|-----------------|  
|[HStringReference::CopyTo Method](../VS_visualcpp/HStringReference--CopyTo-Method.md)|Copies the current HStringReference object to an HSTRING object.|  
|[HStringReference::Get Method](../VS_visualcpp/HStringReference--Get-Method.md)|Retrieves the value of the underlying HSTRING handle.|  
  
### Public Operators  
  
|Name|Description|  
|----------|-----------------|  
|[HStringReference::Operator= Operator](../VS_visualcpp/HStringReference--Operator=-Operator.md)|Moves the value of another HStringReference object to the current HStringReference object.|  
|[HStringReference::Operator== Operator](../VS_visualcpp/HStringReference--Operator==-Operator.md)|Indicates whether the two parameters are equal.|  
|[HStringReference::Operator!= Operator](../VS_visualcpp/HStringReference--Operator!=-Operator.md)|Indicates whether the two parameters are not equal.|  
  
## Inheritance Hierarchy  
 `HStringReference`  
  
## Requirements  
 **Header:** corewrappers.h  
  
 **Namespace:** Microsoft::WRL::Wrappers  
  
## See Also  
 [Microsoft::WRL::Wrappers Namespace](../VS_visualcpp/Microsoft--WRL--Wrappers-Namespace.md)