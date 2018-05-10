---
title: Ändringslogg för Azure PowerShell | Microsoft Docs
description: Det här är en historik över de ändringar som gjorts i den senaste versionen av Azure PowerShell.
services: azure
author: sdwheeler
ms.author: sewhee
manager: carmonm
ms.service: azure-powershell
ms.product: azure
ms.devlang: powershell
ms.topic: conceptual
ms.workload: ''
ms.date: 05/18/2017
ms.openlocfilehash: 5fe7591855577e083aad5923aed37b18d0b2a40c
ms.sourcegitcommit: 37bfbf11fd0967a8e7977c692ab829d286baf88a
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/08/2018
---
# <a name="release-notes"></a>Viktig information

Det här är en lista över ändringar som har gjorts i Azure PowerShell i den här versionen.

## <a name="version-129"></a>Version 1.2.9

Ändringar i den här versionen

* Modulen AzureRm.AzureStackAdmin
    + Ändringar i cmdleten Add-AzureRmResourceProviderRegistration för stöd av delning av admin och klient för Azure Resource Manager. En ny parameter, -ResourceManagerType, har lagts till.
    + Parametrarna -AdminUri, -ApiVersion, -SubscriptionId och -Token har tagits bort från varje cmdlet. Vi har förvarnat om att dessa parametrar kommer att bli inaktuella och nu har de tagits bort.
* Modulen AzureStackStorage
    + Nya cmdletar har lagts till för behållarmigreringsscenarier.
    + Cmdletar som refererar till interna komponenter och underliggande funktioner har tagits bort.
* AzureRM.BootStrapper
    + En ny modul har skapats för att hantera versioner av Azure PowerShell-cmdletar med hjälp av versionsprofiler