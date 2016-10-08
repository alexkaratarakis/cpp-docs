---
title: "Support for Activation Contexts in the MFC Module State"
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
ms.assetid: 1e49eea9-3620-46dd-bc5f-d664749567c7
caps.latest.revision: 12
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
# Support for Activation Contexts in the MFC Module State
MFC creates an activation context using a manifest resource provided by the user module. For more information on how activation contexts are created, see the following topics:  
  
-   [Activation Contexts](http://msdn.microsoft.com/library/aa374153)  
  
-   [Application Manifests](http://msdn.microsoft.com/library/aa374191)  
  
-   [Assembly Manifests](http://msdn.microsoft.com/library/aa374219)  
  
## Remarks  
 When reading these Windows SDK topics, note that the MFC activation context mechanism resembles the Windows SDK activation context except that MFC does not use the Windows SDK Activation Context API.  
  
 Activation context works in MFC applications, user DLLs, and extension DLLs in the following ways:  
  
-   MFC applications use resource ID 1 for their manifest resource. In this case, the MFC does not create its own activation context, but uses the default application context.  
  
-   MFC user DLLs use resource ID 2 for their manifest resource. Here, MFC creates an activation context for each User DLL, so different user DLLs can use different versions of the same libraries (for example, the Common Controls library).  
  
-   MFC extension DLLs rely on their hosting applications or user DLLs to establish their activation context.  
  
 Although the activation context state can be modified using the processes described under [Using the Activation Context API](http://msdn.microsoft.com/library/aa376620), using the MFC activation context mechanism can be useful when developing DLL-based plug-in architectures where it is not easy (or not possible) to manually switch activation state before and after individual calls to external plug-ins.  
  
 The activation context is created in [AfxWinInit](../Topic/AfxWinInit.md). It is destroyed in the `AFX_MODULE_STATE` destructor. An activation context handle is kept in `AFX_MODULE_STATE`. (`AFX_MODULE_STATE` is described in [AfxGetStaticModuleState](../Topic/AfxGetStaticModuleState.md).)  
  
 The [AFX_MANAGE_STATE](../Topic/AFX_MANAGE_STATE.md) macro activates and deactivates the activation context. `AFX_MANAGE_STATE` is enabled for static MFC libraries, as well as MFC DLLs, to allow MFC code to execute in the proper activation context selected by the User DLL.  
  
## See Also  
 [Activation Contexts](http://msdn.microsoft.com/library/aa374153)   
 [Application Manifests](http://msdn.microsoft.com/library/aa374191)   
 [Assembly Manifests](http://msdn.microsoft.com/library/aa374219)   
 [AfxWinInit](../Topic/AfxWinInit.md)   
 [AfxGetStaticModuleState](../Topic/AfxGetStaticModuleState.md)   
 [AFX_MANAGE_STATE](../Topic/AFX_MANAGE_STATE.md)