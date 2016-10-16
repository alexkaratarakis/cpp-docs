---
title: "Linkage in Names with Block Scope"
ms.custom: na
ms.date: "10/14/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: na
ms.suite: na
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: na
ms.topic: "language-reference"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "scope [C++], linkage rules"
  - "linkage [C++], scope linkage rules"
  - "names [C++], scope linkage rules"
  - "block scope [C++]"
  - "external linkage, scope linkage rules"
ms.assetid: 73efa91a-f761-47f7-bbd9-9f9e3508e218
caps.latest.revision: 8
ms.author: "mblome"
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
# Linkage in Names with Block Scope
The following linkage rules apply to names with block scope (local names):  
  
-   Names declared as `extern` have external linkage unless they were previously declared as **static**.  
  
-   All other names with block scope have no linkage.  
  
## See Also  
 [Program and Linkage](../cpp/program-and-linkage---c---.md)