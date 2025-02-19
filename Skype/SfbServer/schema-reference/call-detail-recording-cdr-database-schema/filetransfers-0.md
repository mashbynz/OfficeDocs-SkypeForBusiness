---
title: "FileTransfers table in Skype for Business Server 2015"
ms.reviewer: 
ms.author: serdars
author: SerdarSoysal
manager: serdars
ms.date: 7/15/2015
audience: ITPro
ms.topic: article
ms.service: skype-for-business-server
f1.keywords:
- NOCSH
ms.localizationpriority: medium
ms.assetid: 5368e67c-d8a9-43a1-9472-a839950dedb3
description: "Each record represents one file transfer session."
---

# FileTransfers table in Skype for Business Server 2015
 
Each record represents one file transfer session.
  
|**Column**|**Data Type**|**Key/Index**|**Details**|
|:-----|:-----|:-----|:-----|
|**SessionIdTime** <br/> |datetime  <br/> |Primary, Foreign  <br/> |Time of session request. Used with **SessionIdSeq** to uniquely identify a session. For more information, see the [Dialogs table in Skype for Business Server 2015](dialogs.md). <br/> |
|**SessionIdSeq** <br/> |int  <br/> |Primary, Foreign  <br/> |ID number to identify the session. Used with **SessionIdTime** to uniquely identify a session. For more information, see the [Dialogs table in Skype for Business Server 2015](dialogs.md). <br/> |
|**File Name** <br/> |nvarchar(256)  <br/> ||Name of the file.  <br/> |
|**FileIdentity** <br/> |uniqueidentifier  <br/> ||Unique identifier to distinguish between file transfers involving the same file name.  <br/> |
|**Cookie** <br/> |nvarchar(128)  <br/> |Primary  <br/> |Used to identify every follow-up message as being associated with this one.  <br/> |
|**Accept** <br/> |bit  <br/> ||Can be TRUE or NULL. If TRUE, then Reject and Cancel will be NULL.  <br/> |
|**Reject** <br/> |bit  <br/> ||Can be TRUE or NULL. If TRUE, then Accept and Cancel will be NULL.  <br/> |
|**Cancel** <br/> |bit  <br/> ||Can be TRUE or NULL. If TRUE, then Accept and Reject will be NULL.  <br/> |
|**LastModifiedTime** <br/> |Datetime  <br/> ||For internal use by the Monitoring service.  <br/> This field was introduced in Skype for Business Server 2015.  <br/> |
   

