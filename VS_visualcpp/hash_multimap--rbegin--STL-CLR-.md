---
title: "hash_multimap::rbegin (STL-CLR)"
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
ms.topic: reference
H1: hash_multimap::rbegin (STL/CLR)
ms.assetid: f5ce0614-3c73-4cec-9fa2-efadf0fd36c7
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
# hash_multimap::rbegin (STL-CLR)
Designates the beginning of the reversed controlled sequence.  
  
## Syntax  
  
```  
reverse_iterator rbegin();  
```  
  
## Remarks  
 The member function returns a reverse iterator that designates the last element of the controlled sequence, or just beyond the beginning of an empty sequence. Hence, it designates the `beginning` of the reverse sequence. You use it to obtain an iterator that designates the `current` beginning of the controlled sequence seen in reverse order, but its status can change if the length of the controlled sequence changes.  
  
## Example  
  
```  
// cliext_hash_multimap_rbegin.cpp   
// compile with: /clr   
#include <cliext/hash_map>   
  
typedef cliext::hash_multimap<wchar_t, int> Myhash_multimap;   
int main()   
    {   
    Myhash_multimap c1;   
    c1.insert(Myhash_multimap::make_value(L'a', 1));   
    c1.insert(Myhash_multimap::make_value(L'b', 2));   
    c1.insert(Myhash_multimap::make_value(L'c', 3));   
  
// display contents " [a 1] [b 2] [c 3]"   
    for each (Myhash_multimap::value_type elem in c1)   
        System::Console::Write(" [{0} {1}]", elem->first, elem->second);   
    System::Console::WriteLine();   
  
// inspect first two items in reversed sequence   
    Myhash_multimap::reverse_iterator rit = c1.rbegin();   
    System::Console::WriteLine("*rbegin() = [{0} {1}]",   
        rit->first, rit->second);   
    ++rit;   
    System::Console::WriteLine("*++rbegin() = [{0} {1}]",   
        rit->first, rit->second);   
    return (0);   
    }  
  
```  
  
  **[a 1] [b 2] [c 3]**  
**\*rbegin() = [c 3]**  
**\*++rbegin() = [b 2]**   
## Requirements  
 **Header:** <cliext/hash_map>  
  
 **Namespace:** cliext  
  
## See Also  
 [hash_multimap (STL/CLR)](../VS_visualcpp/hash_multimap--STL-CLR-.md)   
 [hash_multimap::begin (STL/CLR)](../VS_visualcpp/hash_multimap--begin--STL-CLR-.md)   
 [hash_multimap::end (STL/CLR)](../VS_visualcpp/hash_multimap--end--STL-CLR-.md)   
 [hash_multimap::rend (STL/CLR)](../VS_visualcpp/hash_multimap--rend--STL-CLR-.md)