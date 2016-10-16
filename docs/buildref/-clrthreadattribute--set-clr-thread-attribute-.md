---
title: "-CLRTHREADATTRIBUTE (Set CLR Thread Attribute)"
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
  - "VC.Project.VCLinkerTool.CLRThreadAttribute"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "/CLRTHREADATTRIBUTE linker option"
  - "-CLRTHREADATTRIBUTE linker option"
ms.assetid: 4907e9ef-5031-446c-aecf-0a0b32fae1e8
caps.latest.revision: 14
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
# /CLRTHREADATTRIBUTE (Set CLR Thread Attribute)
Explicitly specify the threading attribute for the entry point of your CLR program.  
  
## Syntax  
  
```  
/CLRTHREADATTRIBUTE:{STA|MTA|NONE}  
```  
  
#### Parameters  
 MTA  
 Applies the MTAThreadAttribute attribute to the entry point of your program.  
  
 NONE  
 Same as not specifying /CLRTHREADATTRIBUTE.  Lets the Common Language Runtime (CLR) set the default threading attribute.  
  
 STA  
 Applies the STAThreadAttribute attribute to the entry point of your program.  
  
## Remarks  
 Setting the thread attribute is only valid when building an .exe, as it affects the entry point of the main thread.  
  
 If you use the default entry point (main or wmain, for example) specify the threading model either by using /CLRTHREADATTRIBUTE or by placing the threading attribute (STAThreadAttribute or MTAThreadAttribute) on the default entry function.  
  
 If you use a non-default entry point, specify the threading model either by using /CLRTHREADATTRIBUTE or by placing the threading attribute on the non-default entry function, and then specify the non-default entry point with [/ENTRY](../buildref/-entry--entry-point-symbol-.md).  
  
 If the threading model specified in source code does not agree with the threading model specified with /CLRTHREADATTRIBUTE, the linker will ignore /CLRTHREADATTRIBUTE and apply the threading model specified in source code.  
  
 It will be necessary for you to use single-threading, for example, if your CLR program hosts a COM object that uses single-threading.  If your CLR program uses multi-threading, it cannot host a COM object that uses single-threading.  
  
### To set this linker option in the Visual Studio development environment  
  
1.  Open the project's **Property Pages** dialog box. For details, see [How to: Open Project Property Pages](../notintoc/how-to--open-project-property-pages.md).  
  
2.  Expand the **Configuration Properties** node.  
  
3.  Expand the **Linker** node.  
  
4.  Select the **Advanced** property page.  
  
5.  Modify the **CLR Thread Attribute** property.  
  
### To set this linker option programmatically  
  
1.  See \<xref:Microsoft.VisualStudio.VCProjectEngine.VCLinkerTool.CLRThreadAttribute*>.  
  
## See Also  
 [Setting Linker Options](../buildref/setting-linker-options.md)   
 [Linker Options](../buildref/linker-options.md)