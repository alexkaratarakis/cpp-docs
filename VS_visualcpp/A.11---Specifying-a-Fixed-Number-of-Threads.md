---
title: "A.11   Specifying a Fixed Number of Threads"
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
ms.assetid: 1d06b142-4c35-44b8-994b-20f2aed5462b
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
# A.11   Specifying a Fixed Number of Threads
Some programs rely on a fixed, prespecified number of threads to execute correctly.  Because the default setting for the dynamic adjustment of the number of threads is implementation-defined, such programs can choose to turn off the dynamic threads capability and set the number of threads explicitly to ensure portability. The following example shows how to do this using `omp_set_dynamic` ([Section 3.1.7](../VS_visualcpp/3.1.7-omp_set_dynamic-Function.md) on page 39), and `omp_set_num_threads` ([Section 3.1.1](../VS_visualcpp/3.1.1-omp_set_num_threads-Function.md) on page 36):  
  
```  
omp_set_dynamic(0);  
omp_set_num_threads(16);  
#pragma omp parallel shared(x, npoints) private(iam, ipoints)  
{  
    if (omp_get_num_threads() != 16)   
      abort();  
    iam = omp_get_thread_num();  
    ipoints = npoints/16;  
    do_by_16(x, iam, ipoints);  
}  
```  
  
 In this example, the program executes correctly only if it is executed by 16 threads. If the implementation is not capable of supporting 16 threads, the behavior of this example is implementation-defined.  
  
 Note that the number of threads executing a parallel region remains constant during a parallel region, regardless of the dynamic threads setting. The dynamic threads mechanism determines the number of threads to use at the start of the parallel region and keeps it constant for the duration of the region.