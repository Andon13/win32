---
title: NM\_CLICK (toolbar) notification code
description: Sent by a toolbar control when the user clicks an item with the left mouse button. This notification code is sent in the form of a WM\_NOTIFY message.
ms.assetid: 'fa43c9bc-db2a-4460-b193-2b4694d06d83'
keywords: ["NM_CLICK (toolbar) notification code Windows Controls"]
topic_type:
- apiref
api_name:
- NM_CLICK
api_location:
- Commctrl.h
api_type:
- HeaderDef
---

# NM\_CLICK (toolbar) notification code

Sent by a toolbar control when the user clicks an item with the left mouse button. This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.


```C++
NM_CLICK

    lpnm = (LPNMMOUSE) lParam;
```



## Parameters

<dl> <dt>

*lParam* 
</dt> <dd>

Pointer to an [**NMMOUSE**](nmmouse.md) structure that contains additional information about this notification. The **dwItemSpec** member contains the index of the section that was clicked.

</dd> </dl>

## Return value

Return **TRUE** to indicate that the mouse click was handled and suppress default processing by the system. Return **FALSE** to allow default processing of the click.

## Remarks

Clicking an item with the left mouse button causes the toolbar to send a [**WM\_COMMAND**](https://msdn.microsoft.com/library/windows/desktop/ms647591) message with the [BN\_CLICKED](bn-clicked.md) notification code to the parent window. The NM\_CLICK notification is sent after the **WM\_COMMAND** message.

## Requirements



|                                     |                                                                                       |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Minimum supported client<br/> | Windows�Vista \[desktop apps only\]<br/>                                        |
| Minimum supported server<br/> | Windows Server�2003 \[desktop apps only\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



�

�




