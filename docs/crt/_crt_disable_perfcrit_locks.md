---
title: "_CRT_DISABLE_PERFCRIT_LOCKS"
ms.custom: na
ms.date: "10/14/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: na
ms.suite: na
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: na
ms.topic: "article"
f1_keywords: 
  - "_CRT_DISABLE_PERFCRIT_LOCKS"
  - "CRT_DISABLE_PERFCRIT_LOCKS"
dev_langs: 
  - "C++"
  - "C"
helpviewer_keywords: 
  - "CRT_DISABLE_PERFCRIT_LOCKS constant"
  - "_CRT_DISABLE_PERFCRIT_LOCKS constant"
ms.assetid: 36cc2d86-cdb1-4b2b-a03c-c0d3818e7c6f
caps.latest.revision: 4
ms.author: "corob"
manager: "ghogen"
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
# _CRT_DISABLE_PERFCRIT_LOCKS
Disables performance-critical locking in I/O operations.  
  
## Syntax  
  
```  
#define _CRT_DISABLE_PERFCRIT_LOCKS  
```  
  
## Remarks  
 Defining this symbol can improve performance in single-threaded I/O-bound programs by forcing all I/O operations to assume a single-threaded I/O model. For more information, see [Multithreaded Libraries Performance](../crt/multithreaded-libraries-performance.md).  
  
## See Also  
 [Global Constants](../crt/global-constants.md)