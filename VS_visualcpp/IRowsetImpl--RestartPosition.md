---
title: "IRowsetImpl::RestartPosition"
ms.custom: na
ms.date: 10/03/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 14de66ef-8d2c-4404-adb6-3f6c74ac6cf1
caps.latest.revision: 8
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
# IRowsetImpl::RestartPosition
Repositions the next fetch position to its initial position; that is, its position when the rowset was first created.  
  
## Syntax  
  
```  
  
      STDMETHOD( RestartPosition )(  
   HCHAPTER /* hReserved */   
);  
```  
  
#### Parameters  
 See [IRowset::RestartPosition](https://msdn.microsoft.com/en-us/library/ms712877.aspx) in the *OLE DB Programmer's Reference*.  
  
## Remarks  
 The rowset position is undefined until **GetNextRow** is called. You can move backwards in a rowet by calling [RestartPosition](#vcrefirowsetimplrestartposition) and then fetching or scrolling backwards.  
  
## Requirements  
 **Header:** atldb.h  
  
## See Also  
 [IRowsetImpl Class](../VS_visualcpp/IRowsetImpl-Class.md)