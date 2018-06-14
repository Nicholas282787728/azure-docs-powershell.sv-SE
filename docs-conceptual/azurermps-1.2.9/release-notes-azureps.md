---
title: Ändringslogg för Azure PowerShell | Microsoft Docs
description: Det här är en historik över de ändringar som gjorts i den senaste versionen av Azure PowerShell.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.workload: ''
ms.date: 05/18/2017
ms.openlocfilehash: 91d97260568a36e1135196899503fb0c8e1c6731
ms.sourcegitcommit: c98e3a21037ebd82936828bcb544eed902b24212
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/08/2018
ms.locfileid: "34853023"
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