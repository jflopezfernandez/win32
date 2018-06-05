---
Description: Sent by the default context menu implementation to get the verb for the given command ID in the context menu.
title: DFM\_GETVERB message
ms.technology: desktop
ms.prod: windows
ms.author: windowssdkdev
ms.topic: article
ms.date: 05/31/2018
---

# DFM\_GETVERB message

Sent by the default context menu implementation to get the verb for the given command ID in the context menu.


```C++

                DFM_GETVERB 

    wParam = (WPARAM)(int) idCmd,cchMax;

    lParam = (LPARAM)(LPTSTR) pszText;

            
```



## Parameters

<dl> <dt>

*idCmd\_cchMax* \[in\]
</dt> <dd>

The low-order word of this parameter holds the command ID. The high-order word holds the number of characters in the *pszText* buffer.

</dd> <dt>

*pszText* \[out\]
</dt> <dd>

A pointer to a null-terminated string that contains the verb text.

</dd> </dl>

## Remarks

This message is sent to either the callback function or the callback object depending on how the default context menu object is constructed. There are two APIs for its construction, [**CDefFolderMenu\_Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2), [**SHCreateDefaultContextMenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu).

[**DFM\_INVOKECOMMANDEX**](dfm-invokecommandex.md) is an extended version of this message and provides more information to the callback. Use **DFM\_INVOKECOMMANDEX** if the additional information provided by that interface is needed in your implementation.

## Requirements



|                                     |                                                                                     |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Minimum supported client<br/> | Windows Vista \[desktop apps only\]<br/>                                      |
| Minimum supported server<br/> | Windows Server 2008 \[desktop apps only\]<br/>                                |
| Header<br/>                   | <dl> <dt>Shlobj.h</dt> </dl> |
| Unicode and ANSI names<br/>   | **DFM\_GETVERBW** (Unicode) and **DFM\_GETVERBA** (ANSI)<br/>                 |



 

 



