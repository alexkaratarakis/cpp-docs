---
title: "Linker Tools Warning LNK4254"
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
ms.topic: error-reference
ms.assetid: 6f41dfb3-ca21-40d3-bac7-b637e578efa4
caps.latest.revision: 9
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
# Linker Tools Warning LNK4254
section 'section1' (offset) merged into 'section2' (offset) with different attributes  
  
 The contents of one section were merged into another, but the attributes of the two sections are different. Your program may give unexpected results. For example, data you wanted to be read only may now be in a writable section.  
  
 To resolve LNK4254, modify or remove the merge request.  
  
 When targeting x86 machines and Windows CE targets (ARM, MIPS, SH4, and Thumb) with Visual C++, the .CRT section is read-only. If your code depends on previous behavior (.CRT sections are read/write), you could see unexpected behavior.  
  
 For more information, see,  
  
-   [/MERGE (Combine Sections)](../VS_visualcpp/-MERGE--Combine-Sections-.md)  
  
-   [comment (C/C++)](../VS_visualcpp/comment--C-C---.md)  
  
## Example  
 The following sample generates LNK4254.  
  
```  
// LNK4254.cpp  
// compile with: /W1 /link /WX  
// LNK4254 expected  
#pragma comment(linker, "/merge:.data=.text")  
int main() {}  
```