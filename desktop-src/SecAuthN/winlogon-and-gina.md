---
Description: Winlogon, the GINA, and network providers are the parts of the interactive logon model.
ms.assetid: ea45cd5f-9cb0-41bb-99bf-f84781ae9604
title: Winlogon and GINA
ms.technology: desktop
ms.prod: windows
ms.author: windowssdkdev
ms.topic: article
ms.date: 05/31/2018
---

# Winlogon and GINA

[*Winlogon*](https://msdn.microsoft.com/031c898b-3b4d-4b29-811a-112da37b5e3d), the [*GINA*](https://msdn.microsoft.com/c9567a5b-bd56-4ae1-9eac-af0bb5a6842a), and network providers are the parts of the interactive logon model. The interactive logon procedure is normally controlled by Winlogon, MSGina.dll, and network providers. To change the interactive logon procedure, MSGina.dll can be replaced with a customized GINA DLL.

To work with Winlogon, the GINA, and network providers, you should have a firm knowledge of the Windows security architecture, especially with regard to [*tokens*](https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02), [*authentication packages*](https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02), and related matters.

> [!Note]  
> GINA DLLs are ignored in Windows Vista.

 

For information about specific functions and structures, see [Authentication Reference](authentication-reference.md). This reference section includes descriptions of the functions that a GINA DLL must implement, the Winlogon support functions that the GINA DLL can call, and the data structures used to pass information between Winlogon and the GINA.

Sample GINA code can be found in the Platform Software Development Kit (SDK) Security samples. The samples contain C code for implementing a GINA stub and a GINA hook. For more information about custom GINA DLL development, send an email message to: ginareqs@microsoft.com.

For information about the authentication model supported by Windows and for details about the [*Local Security Authority*](https://msdn.microsoft.com/65dd9a04-fc7c-4179-95ff-dac7dad4668f) (LSA) services and [*authentication package*](https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02) interfaces, see [LSA Authentication](lsa-authentication.md).

For information about the aspects of the Local Security Authority that relate to the administration of security policy, which includes trust relationships with other computers and domains, assignment of privileges, audit generation control, system accessibility, and other similar topics, see [LSA Policy](https://msdn.microsoft.com/16c0a7cb-77c9-4c2d-ba82-e7b8edfbb3a2).

For information about Winlogon and GINA, see the following topics.



| Topic                                                                              | Description                                                                                                                                                                                                                               |
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Winlogon](winlogon.md)                                                           | Winlogon provides a set of support functions for the GINA DLL.<br/>                                                                                                                                                                 |
| [GINA](gina.md)                                                                   | A GINA DLL provides customizable user identification and authentication procedures.<br/>                                                                                                                                            |
| [Terminal Services GINA Functions](terminal-services-gina-functions.md)           | When Terminal Services are enabled, the GINA must call Winlogon support functions to complete several tasks.<br/>                                                                                                                   |
| [Interaction with Network Providers](interaction-with-network-providers.md)       | You can configure a system to support zero or more network providers.<br/>                                                                                                                                                          |
| [Responsibilities and Features](responsibilities-and-features.md)                 | Each part of the interactive logon process has a set of responsibilities.<br/>                                                                                                                                                      |
| [Interaction Between Winlogon and GINA](interaction-between-winlogon-and-gina.md) | The state of Winlogon determines which GINA function is called to process any given [*secure attention sequence*](https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50) (SAS) event.<br/> |
| [Winlogon Notification Packages](winlogon-notification-packages.md)               | You can implement a notification package to monitor and respond to Winlogon events.<br/>                                                                                                                                            |



 

 

 



