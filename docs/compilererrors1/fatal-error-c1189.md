---
title: "Fatal Error C1189"
ms.custom: na
ms.date: "10/14/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: na
ms.suite: na
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: na
ms.topic: "error-reference"
f1_keywords: 
  - "C1189"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "C1189"
ms.assetid: 2e5c8a78-edd4-411c-b619-558a96be148a
caps.latest.revision: 13
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
# Fatal Error C1189
\#error : user supplied error message  
  
 C1189 is generated by the `#error` directive. The developer who codes the directive specifies the text of the error message. For more information, see [#error Directive (C/C++)](../c/sharperror-directive--c-c---.md).  
  
 The following sample generates C1189. In the sample, the developer issues a custom error message because the `_WIN32` identifier is not defined:  
  
```  
// C1189.cpp  
#undef _WIN32  
#if !defined(_WIN32)  
#error _WIN32 must be defined   // C1189  
#endif  
```  
  
 You might also see this error if you build an ATL project by using the **/robust** MIDL compiler option. Use the **/robust** switch to build only [!INCLUDE[win2kfamily](../compilererrors1/includes/win2kfamily_md.md)] and later versions of Windows. To correct this error, use one of the following procedures:  
  
-   Change this line in the dlldatax.c file:  
  
```  
#define _WIN32_WINNT 0x0400   // for WinNT 4.0 or Windows 95 with DCOM  
```  
  
 to:  
  
```  
#define _WIN32_WINNT 0x0500   // for WinNT 4.0 or Windows 95 with DCOM  
```  
  
-   Use the **Advanced** property page in the **MIDL** property page folder to remove the **/robust** switch and then specify the **/no_robust** switch. For more information, see [MIDL Property Pages: Advanced](../ide/midl-property-pages--advanced.md).  
  
## See Also  
 [#define Directive (C/C++)](../c/sharpdefine-directive--c-c---.md)