---
title: Launch tenant attached CMPivot
titleSuffix: Configuration Manager
description: Launch CMPivot for Microsoft Intune tenant attached devices.
ms.date: 07/11/2022
ms.prod: configuration-manager
ms.technology: configmgr-core
ms.topic: conceptual
author: Banreet
ms.author: banreetkaur
manager: apoorvseth
ms.localizationpriority: high
ms.reviewer: mstewart,aaroncz 
ms.collection: tier3
---

# <a name="bkmk_cmpivot"></a> Tenant attach: Launch CMPivot from the admin center

*Applies to: Configuration Manager (current branch)* 

<!--6024392-->
Bring the power of on-premises [CMPivot](../core/servers/manage/cmpivot.md) to the Microsoft Intune admin center. Allow additional personas, like Helpdesk, to be able to initiate real-time queries from the cloud against an individual ConfigMgr managed device and return the results back to the admin center. This gives all the traditional benefits of CMPivot, which allows IT Admins and other designated personas the ability to quickly assess the state of devices in their environment and take action.

## Prerequisites

The following items are required to use CMPivot from the admin center:

- All of the prerequisites for [Tenant attach: ConfigMgr client details](client-details.md)
- Upgrade the target devices to the latest version of the Configuration Manager client.  
- Target clients require a minimum of PowerShell version 4.
- To gather data for the following entities, target clients require a minimum of PowerShell version 5.0:  
  - Administrators
  - Connection
  - IPConfig
  - SMBConfig

## Permissions

The user account needs the following permissions:

- The **Read** permission for the device's **Collection** in Configuration Manager.
- The **Run CMPivot** permission on the **Collection** in Configuration Manager
- An [Intune role](../../intune/fundamentals/role-based-access-control.md) assigned to the user <!--7980141-->


## <a name="bkmk_launch"></a> Launch CMPivot

1. In a browser, go to the [Microsoft Intune admin center](https://go.microsoft.com/fwlink/?linkid=2109431).
1. Select **Devices** then **All Devices**.
1. Select a device that is synced from Configuration Manager via [tenant attach](device-sync-actions.md).
1. Select **CMPivot**.
1. Type your query in the script pane, then select **Run**.

## Close CMPivot

To close CMPivot and return to the device information, use the `X` icon in the top right of CMPivot.

   :::image type="content" source="media/6024392-close-cmpivot.png" alt-text="Close CMPivot with the X icon in Microsoft Intune admin center" lightbox="media/6024392-close-cmpivot.png":::

## Next steps

- For query examples, see [CMPivot sample scripts](cmpivot-samples-attached.md).
- For information about CMPivot entities, operators, and functions, see [CMPivot usage overview](cmpivot-overview-attached.md).
- [Troubleshoot CMPivot](troubleshoot-cmpivot.md) for devices uploaded to the admin center.