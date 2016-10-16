---
title: "Using Views"
ms.custom: na
ms.date: "10/14/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: na
ms.suite: na
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: na
ms.topic: "article"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "interacting with users and role of view class"
  - "drawing, data"
  - "rendering data"
  - "view classes, role in managing user interaction"
  - "CView class, view architecture"
  - "MFC, views"
  - "views, using"
  - "painting data"
  - "user input, interpreting through view class"
  - "view classes, role in displaying application data"
ms.assetid: dc3de6ad-5c64-4317-8f10-8bdcc38cdbd5
caps.latest.revision: 7
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
# Using Views
The view's responsibilities are to display the document's data graphically to the user and to accept and interpret user input as operations on the document. Your tasks in writing your view class are to:  
  
-   Write your view class's [OnDraw](../Topic/CView::OnDraw.md) member function, which renders the document's data.  
  
-   Connect appropriate Windows messages and user-interface objects such as menu items to message-handler member functions in the view class.  
  
-   Implement those handlers to interpret user input.  
  
 In addition, you may need to override other `CView` member functions in your derived view class. In particular, you may want to override [OnInitialUpdate](../Topic/CView::OnInitialUpdate.md) to perform special initialization for the view and [OnUpdate](../Topic/CView::OnUpdate.md) to do any special processing needed just before the view redraws itself. For multipage documents, you also must override [OnPreparePrinting](../Topic/CView::OnPreparePrinting.md) to initialize the Print dialog box with the number of pages to print and other information. For more information on overriding `CView` member functions, see class [CView](../mfcref/cview-class.md) in the *MFC Reference*.  
  
## What do you want to know more about?  
  
-   [Derived view classes available in MFC](../mfc/derived-view-classes-available-in-mfc.md)  
  
-   [Drawing in a view](../mfc/drawing-in-a-view.md)  
  
-   [Interpreting user input through a view](../mfc/interpreting-user-input-through-a-view.md)  
  
-   [The role of the view in printing](../mfc/role-of-the-view-in-printing.md)  
  
-   [Scrolling and scaling views](../mfc/scrolling-and-scaling-views.md)  
  
-   [Initializing and cleaning up documents and views](../mfc/initializing-and-cleaning-up-documents-and-views.md)  
  
## See Also  
 [Document/View Architecture](../mfc/document-view-architecture.md)   
 [CFormView Class](../mfcref/cformview-class.md)   
 [Record Views  (MFC Data Access)](../data/record-views---mfc-data-access-.md)   
 [Bypassing the Serialization Mechanism](../mfc/bypassing-the-serialization-mechanism.md)