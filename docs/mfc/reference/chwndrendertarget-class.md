---
title: "CHwndRenderTarget Class | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: ""
ms.topic: "reference"
f1_keywords: 
  - "CHwndRenderTarget"
  - "afxrendertarget/CHwndRenderTarget"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "CHwndRenderTarget class"
ms.assetid: aa65b69f-7202-46ea-af81-ef325da0b840
caps.latest.revision: 17
author: "mikeblome"
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
# CHwndRenderTarget Class
A wrapper for ID2D1HwndRenderTarget.  
  
## Syntax  
  
```  
class CHwndRenderTarget : public CRenderTarget;  
```  
  
## Members  
  
### Public Constructors  
  
|Name|Description|  
|----------|-----------------|  
|[CHwndRenderTarget::CHwndRenderTarget](#chwndrendertarget)|Constructs a CHwndRenderTarget object from HWND.|  
  
### Public Methods  
  
|Name|Description|  
|----------|-----------------|  
|[CHwndRenderTarget::Attach](#attach)|Attaches existing render target interface to the object|  
|[CHwndRenderTarget::CheckWindowState](#checkwindowstate)|Indicates whether the HWND associated with this render target is occluded.|  
|[CHwndRenderTarget::Create](#create)|Creates a render target associated with the window|  
|[CHwndRenderTarget::Detach](#detach)|Detaches render target interface from the object|  
|[CHwndRenderTarget::GetHwnd](#gethwnd)|Returns the HWND associated with this render target.|  
|[CHwndRenderTarget::GetHwndRenderTarget](#gethwndrendertarget)|Returns ID2D1HwndRenderTarget interface.|  
|[CHwndRenderTarget::ReCreate](#recreate)|Re-creates a render target associated with the window|  
|[CHwndRenderTarget::Resize](#resize)|Changes the size of the render target to the specified pixel size|  
  
### Public Operators  
  
|Name|Description|  
|----------|-----------------|  
|[CHwndRenderTarget::operator ID2D1HwndRenderTarget*](#operator_id2d1hwndrendertarget_star)|Returns ID2D1HwndRenderTarget interface.|  
  
### Protected Data Members  
  
|Name|Description|  
|----------|-----------------|  
|[CHwndRenderTarget::m_pHwndRenderTarget](#m_phwndrendertarget)|A pointer to an ID2D1HwndRenderTarget object.|  
  
## Inheritance Hierarchy  
 [CObject](../../mfc/reference/cobject-class.md)  
  
 [CRenderTarget](../../mfc/reference/crendertarget-class.md)  
  
 [CHwndRenderTarget](../../mfc/reference/chwndrendertarget-class.md)  
  
## Requirements  
 **Header:** afxrendertarget.h  
  
##  <a name="attach"></a>  CHwndRenderTarget::Attach  
 Attaches existing render target interface to the object  
  
```  
void Attach(ID2D1HwndRenderTarget* pTarget);
```  
  
### Parameters  
 `pTarget`  
 Existing render target interface. Cannot be NULL  
  
##  <a name="checkwindowstate"></a>  CHwndRenderTarget::CheckWindowState  
 Indicates whether the HWND associated with this render target is occluded.  
  
```  
D2D1_WINDOW_STATE CheckWindowState() const;  
```  
  
### Return Value  
 A value that indicates whether the HWND associated with this render target is occluded.  
  
##  <a name="chwndrendertarget"></a>  CHwndRenderTarget::CHwndRenderTarget  
 Constructs a CHwndRenderTarget object from HWND.  
  
```  
CHwndRenderTarget(HWND hwnd = NULL);
```  
  
### Parameters  
 `hwnd`  
 The HWND associated with this render target  
  
##  <a name="create"></a>  CHwndRenderTarget::Create  
 Creates a render target associated with the window  
  
```  
BOOL Create(HWND hWnd);
```  
  
### Parameters  
 `hWnd`  
 The HWND associated with this render target  
  
### Return Value  
 If the method succeeds, it returns TRUE. Otherwise, it returns FALSE  
  
##  <a name="detach"></a>  CHwndRenderTarget::Detach  
 Detaches render target interface from the object  
  
```  
ID2D1HwndRenderTarget* Detach();
```  
  
### Return Value  
 Pointer to detached render target interface.  
  
##  <a name="gethwnd"></a>  CHwndRenderTarget::GetHwnd  
 Returns the HWND associated with this render target.  
  
```  
HWND GetHwnd() const;  
```  
  
### Return Value  
 The HWND associated with this render target.  
  
##  <a name="gethwndrendertarget"></a>  CHwndRenderTarget::GetHwndRenderTarget  
 Returns ID2D1HwndRenderTarget interface.  
  
```  
ID2D1HwndRenderTarget* GetHwndRenderTarget();
```  
  
### Return Value  
 Pointer to an ID2D1HwndRenderTarget interface or NULL if object is not initialized yet.  
  
##  <a name="m_phwndrendertarget"></a>  CHwndRenderTarget::m_pHwndRenderTarget  
 A pointer to an ID2D1HwndRenderTarget object.  
  
```  
ID2D1HwndRenderTarget* m_pHwndRenderTarget;  
```  
  
##  <a name="operator_id2d1hwndrendertarget_star"></a>  CHwndRenderTarget::operator ID2D1HwndRenderTarget*  
 Returns ID2D1HwndRenderTarget interface.  
  
```  
operator ID2D1HwndRenderTarget*();
```   
  
### Return Value  
 Pointer to an ID2D1HwndRenderTarget interface or NULL if object is not initialized yet.  
  
##  <a name="recreate"></a>  CHwndRenderTarget::ReCreate  
 Re-creates a render target associated with the window  
  
```  
BOOL ReCreate(HWND hWnd);
```  
  
### Parameters  
 `hWnd`  
 The HWND associated with this render target  
  
### Return Value  
 If the method succeeds, it returns TRUE. Otherwise, it returns FALSE.  
  
##  <a name="resize"></a>  CHwndRenderTarget::Resize  
 Changes the size of the render target to the specified pixel size  
  
```  
BOOL Resize(const CD2DSizeU& size);
```  
  
### Parameters  
 `size`  
 The new size of the render target in device pixels  
  
### Return Value  
 If the method succeeds, it returns TRUE. Otherwise, it returns FALSE.  
  
## See Also  
 [Classes](../../mfc/reference/mfc-classes.md)
